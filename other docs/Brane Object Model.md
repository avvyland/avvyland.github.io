#Brane Object Model

The creation of virtual worlds in Avvyland involves two main components: 

 - 3D grid made of uniform cells

 - objects of different kinds

A user adds objects to the grid, configures them, and interacts with the built structures. The entire building process is regulated by Brane Object Model (BOM).

 > TERM:

 > Brane Object Model (BOM) is a unified logic underpinned by two principles:

 > 1. The entire Avvyland’s space is represented by a three-dimensional orthogonal grid composed of uniform cells

 > 2. Everything in the space is an object: Brane, user’s avatar, block, hyperlink, function, etc.

 > The BOM sets the rules for the whole lifecycle of an Avvyland’s virtual world: objects placing onto the grid and registering in the addressing system, configuration, interactions with each other, etc.

![bom](/bom.png

Now, let us consider the grid and the objects, their work principles and characteristics, and see how the virtual world is created of these two components using BOM principles.

Grid

The three-dimensional orthogonal grid is composed of uniform cells:
The smallest cell of the grid is 10*10 centimetres. Each cell has a unique address registered in the special storage in Avvyland’s database. Each object placed on the Brane occupies a certain number of neighbouring cells. This way, the grid’s cells form a unified addressing system. 

NOTE: 

The 10*10 cm cell is used as a standard unit of the current building space in Avvyland web application. The size of this space is set in the application’s Settings → Render distance. For example, the value 100 means that the building area is visible within a 10-meter radius from the center:

The cells can comprise objects of any type. 

Objects

The object is the main logical element in Avvyland. Any logical entities in Avvyland are represented as 3D objects of the following types: 

 - Blocks 

 - Structures

 - Players 

> TERM: 

> Block is an elementary object of Brane. It is a logical entity with an indefinite number of parameters which includes one or several logical units called blockcells. 

TERM: 

Structure is a compound object made of multiple items (blocks/objects/structures). Every structure is non-fungible; it can be copied only by its owner if they have all parts of the structure. Like blicks, structures can have an indefinite number of parameters.

TERM: 

Player is an active user of the Brane. The Player’s avatar is placed in the Brane and occupies certain cells just like any other object.

Users can purchase ready-made objects on marketplaces, pick them up from their Home Brane (if allowed), or create objects of their own. Avvyland enables users to do the latter via the following tools:

UCS – unified content system

DSL – domain-specific language

Now, let us consider each of these tools, see how they work, and what they can do.

Unified content system

Users can create new objects and modify the existing ones via the unified content system (UCS). 

TERM:

Unified content system (UCS) is a service that provides an intuitive 'wizard' (tool) for users to create or edit any content without coding: upload a blank 3D model (e.g., bought on marketplaces), modify it, and add the ready object in their Brane inventory.

Once a user has uploaded a 3D model, UCS pre-processes it and guides the user through several simple steps where the user can: 

add/edit textures 

add/edit effects (animation, etc) 

preview 

commit

Once this is done, the object is added to the system. Now, the user can own it and sell it either as a fungible unit or as an NFT one. 

UCS simplifies the procedure of content generation as it does not require any coding or design skills to create objects.

While user creates their content via the wizard’s simple interface, UCS implements several sophisticated tasks on the backend: 3D model optimization, automation of details visibility on different levels (the further the model, the fewer details are visible – to save resources), etc. 

NOTE:

This functionality is currently in the developmental stage and will be added to Avvyland system later.

Domain-specific language

Each object is a smart one – its appearance, properties, behaviour, and logic are configurable. Such a configuration is possible through domain-specific language (DSL). 

TERM:

Domain-specific language (DSL) is a declarative language of a high level. For the user’s convenience, DSL is implemented as a no-code visual programming language where all logical elements are visualized as simple blocks. To program an object in the desired way, the user selects the required operators and functions in the DSL’s intuitive interface. 

By arranging the programming blocks in DSL, the user creates sets of rules for each object. These rules are called handlers.

TERM:

Handler aka Smart contract is a rule applied to an object to program its appearance, properties, behaviour, and logic. Handlers allow blocks to change their current state when other objects are changed. 

Once configured in a certain way, a block can:

preliminarily approve or reject planned modification of other objects or objects of the scene

approve or reject other objects' placing into the Brane depending on the position and properties of those objects

modify properties of its own or of other objects within the Brane’s local time

generate other blocks and structures, generate or modify Actions

 > Example:

 > User adds a flower object into the soil object. There is also a water object in Brane’s inventory. Then, the user sets a condition using DSL:

 > `if water is added to the soil at least once a day or more frequently, the flower grows;

 > otherwise, the flower droops from drought.`

The condition is written in visualized operators that look like blocks. Once the condition is set, the flower behaves in accordance with the condition.

Such configurability makes it possible to create games based on Avvyland. 

NOTE:

This functionality is currently in the developmental stage and will be added to Avvyland system later.

All objects form an entire ecosystem inside the Avvyland universe. 

Now that we know how the grid and the objects work, let us see how they interact.

BOM in practice

All objects are arranged inside the grid, and such an arrangement is standardized. In this section, we will consider how this arrangement works in practice. 

Every cell on the grid has its unique address, i.e., coordinates. Objects are located on the Brane in accordance with the orientation of the cells.



Once a cell has been occupied by an object or its part, the object has its unique address identical to the cell’s coordinates. The address of each object is registered as an index in the address system in Avvyland’s storage. Now that the object has its unique address, these occupied cells cannot be filled by other objects at the same time. This approach allows to establish a consistent addressing system. 



When placed, objects enter into different relations with each other. These relations involve physics, properties, and hierarchy. In the objects' hierarchy, any object can be a parent or a child of another object. A parent object has properties of its children objects in its own properties.

Example:

A Brane itself is an object, its user has an Avvy which is an object as well – these two objects are in ownership.

A user adds a soil object on their Brane. Thus, the Brane and the soil are now in a belonging relationship. 

Then, the user plants a tulip flower into the soil. Thus, the soil and the tulip are now in a 'parent-child' relationship. 

Then, user moves the tulip through/on the brane (or changes its physical properties) – the belonging relationship has been changed.

Every action made on an object is also is registered in the blockchain as a transaction. Registration of transactions in the blockchain starts with a Brane creation: 



As the player’s avatar itself is an object, it occupies certain cells at a definite period. Like with objects of any other type, blockchain registers Avvy’s motion through the Brane, its current location, configuration, and status. 

Example

Three players gathered in the same square. As long as the square does not belong to any specific player, all three players will see each other Branes as nearby ones. The first and the second players connected to their Branes, and the third player open the list of nearby Branes and connected to the second player’s Brane. Thus, the second player will see the Avvy of the third player on their Brane in accordance with the third player’s location on the Brane.

A Brane can be placed in any physical space which is purchased by the Brane’s user. This will grant the user an exclusive privilege to make their Brane the only publicly visible Brane in this area.

 > Example 

  > An entrepreneur purchases the physical area next to the shopping mall and arranges their ad there. Then, no one else can make their Branes visible in that area. They still can place them as private ones, but other users will only see the entrepreneur’s Brane with the ad.

Summary

Brane Object Model (BOM) implies that all entities in Avvyland – blocks, structures, Branes, and Avvys – are 3D objects which are located in an orthogonal logical space in a structured way. 

A virtual world inside the Brane space is built like a constructor by filling the 3D grid with life-like objects from the Inventory. Composed of uniform cells, the grid forms the addressing system where every object has its unique address written in the storage as an index. Such standardization makes the processing of objects quick and easy.

Based on these BOM principles, we also developed intuitive no-code solutions for content creation: 

Objects can be created using a visual tool aka wizard called unified content system (UCS).

Properties, behaviour, and logic of objects are set in a service named domain-specific language (DSL). To simplify the configuration of the objects for users, DSL is implemented as a no-code visual programming tool where all operators look like blocks. 

All objects enter into different relations with each other. 

Any action performed with an object is registered in the blockchain as a separate transaction. The blockchain allows for the validation of transactions by different users and thus makes the building process transparent and reliable.