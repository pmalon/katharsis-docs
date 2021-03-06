How to use Katharsis in your applications
=========================================

Katharsis provides means to easily expose resources over the REST interface. If you want to take a deeper look on the concepts behind Katharsis, this is page for you!


Requirements
------------

Below are listed dependencies used in Katharsis that project has to meet to be compatible with latest library version:

.. note::
  Katharsis library requires minimum Java 7 to build and run.


``katharsis-core``

.. code-block:: bash

  io.katharsis:katharsis-core:bundle:2.6.0
  +- org.reflections:reflections:jar:0.9.9:compile
  |  +- com.google.guava:guava:jar:15.0:compile
  |  +- org.javassist:javassist:jar:3.18.2-GA:compile
  |  \- com.google.code.findbugs:annotations:jar:2.0.1:compile
  +- net.jodah:typetools:jar:0.4.4:compile
  +- org.slf4j:slf4j-api:jar:1.7.13:compile
  +- com.fasterxml.jackson.core:jackson-databind:jar:2.6.3:compile
  |  \- com.fasterxml.jackson.core:jackson-core:jar:2.6.3:compile
  +- com.fasterxml.jackson.core:jackson-annotations:jar:2.6.3:compile


``katharsis-rs``

.. code-block:: bash

  io.katharsis:katharsis-rs:bundle:2.6.0
  +- io.katharsis:katharsis-core:jar:2.6.0:compile
  |  +- net.jodah:typetools:jar:0.4.4:compile
  |  +- org.slf4j:slf4j-api:jar:1.7.13:compile
  |  \- com.fasterxml.jackson.core:jackson-databind:jar:2.6.3:compile
  |     \- com.fasterxml.jackson.core:jackson-core:jar:2.6.3:compile
  +- com.fasterxml.jackson.core:jackson-annotations:jar:2.6.3:compile
  +- org.reflections:reflections:jar:0.9.9:compile
  |  +- com.google.guava:guava:jar:15.0:compile
  |  +- org.javassist:javassist:jar:3.18.2-GA:compile
  |  \- com.google.code.findbugs:annotations:jar:2.0.1:compile
  +- javax.ws.rs:javax.ws.rs-api:jar:2.0.1:compile
  +- javax.servlet:javax.servlet-api:jar:3.0.1:compile


``katharsis-servlet``

.. code-block:: bash

  io.katharsis:katharsis-servlet:bundle:2.6.0
  +- io.katharsis:katharsis-core:jar:2.6.0:compile
  |  +- net.jodah:typetools:jar:0.4.4:compile
  |  +- com.fasterxml.jackson.core:jackson-databind:jar:2.6.3:compile
  |  |  \- com.fasterxml.jackson.core:jackson-core:jar:2.6.3:compile
  |  \- com.fasterxml.jackson.core:jackson-annotations:jar:2.6.3:compile
  +- org.reflections:reflections:jar:0.9.9:compile
  |  +- org.javassist:javassist:jar:3.18.2-GA:compile
  |  \- com.google.code.findbugs:annotations:jar:2.0.1:compile
  +- com.google.guava:guava:jar:15.0:compile
  +- javax.servlet:javax.servlet-api:jar:3.0.1:provided
  +- org.slf4j:slf4j-api:jar:1.7.6:provided


``katharsis-spring``

.. code-block:: bash

  io.katharsis:katharsis-spring:bundle:2.6.0
  +- org.springframework.boot:spring-boot-starter-web:jar:1.3.1.RELEASE:compile
  |  ...
  +- org.springframework.boot:spring-boot-configuration-processor:jar:1.3.1.RELEASE:compile
  |  +- org.json:json:jar:20140107:compile
  |  \- org.springframework:spring-core:jar:4.2.4.RELEASE:compile
  |     \- commons-logging:commons-logging:jar:1.2:compile
  +- io.katharsis:katharsis-servlet:jar:2.6.0:compile
  |  +- io.katharsis:katharsis-core:jar:2.6.0:compile
  |  |  +- net.jodah:typetools:jar:0.4.4:compile
  |  |  \- org.slf4j:slf4j-api:jar:1.7.13:compile
  |  \- com.google.guava:guava:jar:15.0:compile
  +- org.reflections:reflections:jar:0.9.9:compile
  |  +- org.javassist:javassist:jar:3.18.2-GA:compile
  |  \- com.google.code.findbugs:annotations:jar:2.0.1:compile


``katharsis-vertx``

.. code-block:: bash

  +--- io.katharsis:katharsis-core:2.99.0-SNAPSHOT
  |    +--- org.projectlombok:lombok:1.16.8
  |    +--- net.jodah:typetools:0.4.4
  |    +--- org.slf4j:slf4j-api:1.7.13
  |    +--- com.fasterxml.jackson.core:jackson-databind:2.6.3
  |    |    +--- com.fasterxml.jackson.core:jackson-annotations:2.6.0 -> 2.6.3
  |    |    \--- com.fasterxml.jackson.core:jackson-core:2.6.3
  |    \--- com.fasterxml.jackson.core:jackson-annotations:2.6.3
  +--- io.vertx:vertx-core:3.2.1
  ...
  +--- io.vertx:vertx-web:3.2.1
  ...
  +--- org.reflections:reflections:0.9.9
  |    +--- com.google.guava:guava:15.0
  |    +--- org.javassist:javassist:3.18.2-GA
  |    \--- com.google.code.findbugs:annotations:2.0.1
  \--- org.slf4j:slf4j-api:1.7.13

  ``katharsis-client``

  .. code-block:: bash

  io.katharsis:katharsis-client:bundle:2.6.0
  +- io.katharsis:katharsis-core:jar:2.6.0:compile
  |  +- net.jodah:typetools:jar:0.4.4:compile
  |  +- org.slf4j:slf4j-api:jar:1.7.13:compile
  |  +- com.fasterxml.jackson.core:jackson-databind:jar:2.6.3:compile
  |  |  \- com.fasterxml.jackson.core:jackson-core:jar:2.6.3:compile
  |  \- com.fasterxml.jackson.core:jackson-annotations:jar:2.6.3:compile
  +- org.reflections:reflections:jar:0.9.9:compile
  |  +- com.google.guava:guava:jar:15.0:compile
  |  +- org.javassist:javassist:jar:3.18.2-GA:compile
  |  \- com.google.code.findbugs:annotations:jar:2.0.1:compile
  +- com.squareup.okhttp:okhttp:jar:2.7.5:compile
  |  \- com.squareup.okio:okio:jar:1.6.0:compile

Supported requests
------------------

Currently Katharsis covers most of the JSON API specification request types. The following table describes available requests that are currently accepted:

.. csv-table:: A summary of the supported requests
  :header:  HTTP method, Kind of request, Sample URL,  Multiplicity of resource

  GET,	resources, "http://host.local/tasks or http://host.local/tasks/1,2", multiple
  ,resource,	http://host.local/tasks/1,	single
  ,relationship,	http://host.local/tasks/1/relationships/project,	single
  ,field,	http://host.local/tasks/1/project,	single
  POST,	resource,	http://host.local/tasks,	single
  ,field,	http://host.local/tasks/1/project,	single
  ,relationship,	http://host.local/tasks/1/relationships/project,	single
  PATCH,	resource,	http://host.local/tasks/1,	single
  ,relationship,	http://host.local/tasks/1/relationships/project,	single
  DELETE,	resource,	http://host.local/tasks/1,	single
  ,relationship,	http://host.local/tasks/1/relationships/project,	single



Relationships
-------------

One of the main features of JSON API and Katharsis is support of managing relations between resources. To achieve that, two steps are required:

* Add a field annotated with JsonApiToOne or JsonApiToMany (depending on multiplicity of the relation) which will represent a unidirectional relation.
* Add a repository which defines operations that can be made on models.


Models
------

There are several annotations which can be assigned to models. By default all fields of the model are reflected in JSON API communication except synthetic fields. The annotations described below should be associated with either a field or a getter.


JsonApiResource
~~~~~~~~~~~~~~~

It is the most important annotation which defines a resource. It requires type parameter to be defined that is used to form a URLs and type field in passed JSONs. According to JSON API standard, the name defined in type can be either plural or singular

The example below shows a sample class which contains a definition of a resource.

.. code-block:: java

  @JsonApiResource(type = "tasks")
  public class Task {
    // fields, getters and setters
  }


JsonApiId
~~~~~~~~~

Defines a field which will be used as an identifier of a resource.
Each resource requires this annotation to be present on a field which type implements ``Serializable`` or is of primitive type.

The example below shows a sample class which contains a definition of a field which contains an identifier.

.. code-block:: java

  @JsonApiResource(type = "tasks")
  public class Task {
    @JsonApiId
    private Long id;

    // fields, getters and setters
  }

JsonApiToOne
~~~~~~~~~~~~

Indicates an association to single value which needs to be handled by a separate ``RelationshipRepository``.
 A type of the field has to be a valid resource.

The example below shows a sample class which contains this kind of relationship.


.. code-block:: java

  @JsonApiResource(type = "tasks")
  public class Task {

    // ID field

    @JsonApiToOne
    private Project project;

    // fields, getters and setters
  }

JsonApiToMany
~~~~~~~~~~~~~

Indicates an association to many values which need to be handled by a separate ``RelationshipRepository``.
A type of the field has to be an ``Iterable`` or its derived classes (e.g.``List``) of valid resources.
By default, relationship is considered to be lazy, that is the relationship is not shown in the Top Level JSON.
To change that, pass parameter ``@JsonApiToMany(lazy = false)``.

The example below shows a sample class which contains this kind of relationship.

.. code-block:: java

  @JsonApiResource(type = "tasks")
  public class Task {

    // ID field

    @JsonApiToMany(lazy = false)
    private List<Project> projects;

    @JsonApiToMany // not shown in Top Level JSON
    private List<Log> logs;

    // fields, getters and setters
  }



JsonApiIncludeByDefault
~~~~~~~~~~~~~~~~~~~~~~~

Indicates additional resources that should be included by default (will be available
in included field of Top level JSON object) with every primary resource.
The field can be added to every relationship defined by ``JsonApiToOne`` or ``JsonApiToMany``.
Otherwise, ``ResourceException`` will be thrown at the initialization phrase.

The example below shows a sample model with this annotation.

.. code-block:: java

  @JsonApiResource(type = "tasks")
  public class Task {

    // ID field

    @JsonApiToOne
    @JsonApiIncludeByDefault
    private Project project;

    // fields, getters and setters
  }

JsonApiLookupIncludeAutomatically
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Field or getter annotated with ``JsonApiLookupIncludeAutomatically`` will be automatically populated by Katharsis on ``GET`` requests.
It can be added to every relationship defined by ``JsonApiToOne`` or ``JsonApiToMany``.

The example below shows a sample class which will always contain a relationship's resource.

.. code-block:: java

  @JsonApiResource(type = "tasks")
  public class Task {

    // ID field

    @JsonApiToOne
    @JsonApiLookupIncludeAutomatically
    private Project project;

    // fields, getters and setters
  }








JsonApiMetaInformation
~~~~~~~~~~~~~~~~~~~~~~~

Field or getter annotated with ``JsonApiMetaInformation`` are marked to carry a ``MetaInformation`` implementation.
See http://jsonapi.org/format/#document-meta for more information about meta data. Example:


.. code-block:: java
	
	@JsonApiResource(type = "projects")
	public class Project {
	
		...
	
		@JsonApiMetaInformation
		private ProjectMeta meta;
	
		public static class ProjectMeta implements MetaInformation {
	
			private String value;
	
			public String getValue() {
				return value;
			}
	
			public void setValue(String value) {
				this.value = value;
			}
		}
	}



JsonApiLinksInformation
~~~~~~~~~~~~~~~~~~~~~~~

Field or getter annotated with ``JsonApiLinksInformation`` are marked to carry a ``LinksInformation`` implementation.
See http://jsonapi.org/format/#document-links for more information about linking. Example:


.. code-block:: java
	
	@JsonApiResource(type = "projects")
	public class Project {
	
		...
	
		@JsonApiLinksInformation
		private ProjectLinks links;
	
		public static class ProjectLinks implements MetaInformation {
	
			private String value;
	
			public String getValue() {
				return value;
			}
	
			public void setValue(String value) {
				this.value = value;
			}
		}
	}





Repositories
------------

The model definition must have corresponding resource repository.
In addition, each relation also must have a corresponding repository.

Those repositories can be defined in one of the two ways:

* Implementing a repository interface:

  * ResourceRepositoryV2 for a resource
  * RelationshipRepositoryV2 for resource relationships

* Annotated with a repository annotation:

  * JsonApiResourceRepository for a resource
  * JsonApiRelationshipRepository for resource relationships
  
Both approaches have their merits. But note that the use of interfaces has
one main advantage over annotated repositories: the interfaces are  
supported by ``katharsis-client``. Applications may declare their own 
interfaces, extending the ones of Katharsis with type arguments
and additional actions. On the server side, repository interfaces
are implemented by the repository implementations. On the client side,
``katharsis-client`` can automatically create stubs to have 
type-safe access to remote repositories. More information is available
with the client documentation further down.


ResourceRepositoryV2
~~~~~~~~~~~~~~~~~~~~

Base repository which is used to operate on resources.
Each resource should have a corresponding repository implementation.
It consist of five basic methods which provide a CRUD for a resource and two parameters: the first is a type of a resource and the second is a type of the resource’s identifier.

The methods are as follows:

* ``findOne(ID id, QuerySpec querySpec)``
  Search one resource with a given ID. If a resource cannot be found, a ResourceNotFoundException exception should be thrown.
  It should return an entity with associated relationships.

* ``findAll(QuerySpec querySpec)``
  Search for all of the resources. An instance of QueryParams can be used if necessary.
  If no resources can be found an empty Iterable or null must be returned.
  It should return entities with associated relationships.

* ``findAll(Iterable<ID>ids, QuerySpec querySpec)``
  Search for resources constrained by a list of identifiers. An instance of QueryParams can be used if necessary.
  If no resources can be found an empty Iterable or null must be returned.
  It should return entities with associated relationships.

* ``save(S entity)``
  Saves a resource. It should not save relating relationships. A Returning resource must include assigned identifier created for the instance of resource.
  This method should be able to both create a new resource and update existing one.

* ``delete(ID id)``
  Removes a resource identified by id parameter.
  
The ResourceRepositoryBase is a base class that takes care of some boiler-plate, like implementing findOne with findAll. An
implementation can then look as simple as:

.. code-block:: java

	public class ProjectRepository extends ResourceRepositoryBase<Project, String> {
	
		private Map<Long, Project> projects = new HashMap<>();
	
		public ProjectRepository() {
			super(Project.class);
			List<String> interests = new ArrayList<>();
			interests.add("coding");
			interests.add("art");
			save(new Project(1L, "Project A"));
			save(new Project(2L, "Project B"));
			save(new Project(3L, "Project C"));
		}
	
		@Override
		public synchronized void delete(String id) {
			projects.remove(id);
		}
	
		@Override
		public synchronized <S extends Project> S save(S project) {
			projects.put(project.getId(), project);
			return project;
		}
	
		@Override
		public synchronized ResourceList<Project> findAll(QuerySpec querySpec) {
			return querySpec.apply(projects.values());
		}
	}


RelationshipRepositoryV2
~~~~~~~~~~~~~~~~~~~~~~~~

Each relationship defined in Katharsis (annotation @JsonApiToOne and @JsonApiToMany) must have a relationship repository defined.

Base unidirectional repository responsible for operations on relations.
All of the methods in this interface have fieldName field as their last parameter to solve the problem of many relationships between the same resources.

* ``setRelation(T source, D_ID targetId, String fieldName)``
  Sets a resource defined by targetId to a field fieldName in an instance source. If no value is to be set, null value is passed.

* ``setRelations(T source, Iterable<D_ID> targetIds, String fieldName)``
  Sets resources defined by targetIds to a field fieldName in an instance source. This is a all-or-nothing operation, that is no partial relationship updates are passed. If no values are to be set, empty Iterable is passed.

* ``addRelations(T source, Iterable<D_ID> targetIds, String fieldName)``
  Adds relationships to a list of relationships.

* ``removeRelations(T source, Iterable<D_ID> targetIds, String fieldName)``
  Removes relationships from a list of relationships.

* ``findOneTarget(T_ID sourceId, String fieldName, QuerySpec querySpec)``
  Finds one field's value defined by fieldName in a source defined by sourceId.

* ``findManyTargets(T_ID sourceId, String fieldName, QuerySpec querySpec)``
  Finds an Iterable of field's values defined by fieldName in a source defined by sourceId .


This interface must be implemented to let Katharsis work correctly, some of the requests are processed using only this kind of repository.
As it can be seen above, there are two kinds of methods: for multiple and single relationships and it is possible to implement only one type of methods, e.g. singular methods.
Nevertheless, it should be avoided because of potential future problems when adding new fields of other sizes.

In many cases, relationship operations can be mapped back to resource repository operations. Making the need
for a custom relationship repository implementation redundant. A findManyTargets request might can be
served by filtering the target repository. Or a relationship can be set by invoking the save operation 
on either the source or target resource repository (usually you want to save on the single-valued side).
The ResourceRepositoryBase is a base class that takes care of exactly this. A repository
implementation then looks as simple as:


.. code-block:: java

	public class ProjectToTaskRepository extends RelationshipRepositoryBase<Project, Long, Task, Long> {
	
		public ScheduleToTaskRepository() {
			super(Project.class, Task.class);
		}
	}


For this to work, relations must be set up bidirectionally with the ``opposite`` attribute:

.. code-block:: java
	
	@JsonApiResource(type = "tasks")
	public class Task {
	
		@JsonApiToOne(opposite = "tasks")
		@JsonApiIncludeByDefault
		private Project project;
	
	    ...
	}




ResourceList
~~~~~~~~~~~~~~~~~~~~~~~~

ResourceRepositoryV2 and RelationshipRepositoryV2 return lists of type ResourceList. The ResourceList can carry, next
to the actual resources, also meta and links information:

* ``getLinks()``
	Gets the links information attached to this lists.
	
* ``getMeta()``
	Gets the meta information attached to this lists.

* ``getLinks(Class<L> linksClass)``
	Gets the links information of the given type attached to this lists. If the given type is not found, null is returned.

* ``getMeta(Class<M> metaClass)``
	Gets the meta information of the given type attached to this lists. If the given type is not found, null is returned.

Thhere is a default implementation named DefaultResourceList. To gain type-safety, improved readability and katharsis-client support,
application may provide a custom implementation extending ResourceListBase:

.. code-block:: java

	class ScheduleList extends ResourceListBase<Schedule, ScheduleListMeta, ScheduleListLinks> {

	}
	
	class ScheduleListLinks implements LinksInformation {

		public String name = "value";
		
		...
	}

	class ScheduleListMeta implements MetaInformation {

		public String name = "value";
		
		...
	}
	
This implementation can then be added to a repository interface declaration
and used by both servers and clients:

.. code-block:: java

	public interface ScheduleRepository extends ResourceRepositoryV2<Schedule, Long> {
	
		@Override
		public ScheduleList findAll(QuerySpec querySpec);
		
	}






Annotated repositories
~~~~~~~~~~~~~~~~~~~~~~

A resource repository can also be defined using the ``JsonApiResourceRepository`` or ``JsonApiRelationshipRepository`` annotations from ``io.katharsis.repository.annotations`` package.

Defining the repositories this way has two benefits:

* It's not necessary to define all of the methods i.e. read-only resources might have just reading methods defined
* Additional parameters can be added to the methods like authentication, request headers or cookies

Along with the required parameters for each methods (like the resource identifier in ``JsonApiFindOne``), the default supported type is QueryParams, which provides a set of parsed query parameters.
Each Katharsis integration provides different set of supported parameters.
This list can be found in JAX-RS and Servlet integration sections.

A list below defines a mapping of ``ResourceRepository`` methods to annotations:

* ``findOne(ID, QueryParams) -> JsonApiFindOne``

  The first parameter must be a resource's id. This method must return one resource.

* ``findAll(QueryParams) -> JsonApiFindAll``

  This method must return a list of resources.

* ``findAll(Iterable<ID>, QueryParams) -> JsonApiFindAllWithIds``

  The first parameter must be a list of resource ids. This method must return a list of resources.

* ``save(S) -> JsonApiSave``

  The first parameter must be a resource. This method must return one resource.

* ``delete(ID) -> JsonApiDelete``

  The first parameter must be a resource's id.


A list below defines a mapping of ``RelationshipRepository`` methods to annotations:

* ``setRelation(T, D_ID, String) -> JsonApiSetRelation``

  The requirements for the method parameters are as follows:

  #. Instance of a source resource
  #. Instance of a relationship to be set
  #. Relationship's field name

* ``setRelations(T, Iterable<D_ID>, String) -> JsonApiSetRelations``

  The requirements for the method parameters are as follows:

  #. Instance of a source resource
  #. ``Iterable`` of relationships to be set
  #. Relationship's field name

* ``addRelations(T, Iterable<D_ID>, String) -> JsonApiAddRelation``

  The requirements for the method parameters are as follows:

  #. Instance of a source resource
  #. Iterable of relationships to be add
  #. Relationship's field name

* ``removeRelations(T, Iterable<D_ID>, String) -> JsonApiRemoveRelation``

  The requirements for the method parameters are as follows:

  #. Instance of a source resource
  #. Iterable of relationships to be removed
  #. Relationship's field name

* ``findOneTarget(T_ID, String, QueryParams) -> JsonApiFindOneTarget``

  The requirements for the method parameters are as follows:

  #. An identifier of a source resource
  #. Relationship's field name
  #. The method has to return a resources.

* ``findManyTargets(T_ID, String, QueryParams) -> JsonApiFindManyTargets``

  The requirements for the method parameters are as follows:

  #. An identifier of a source resource
  #. Relationship's field name
  #. The method has to return an Iterable with resources.



Query parameters
----------------

Katharsis has defined set of query parameters which can be used by the framework during data retrieval and by a developer to perform other operations.
All of the types of parameters can be accessed with the either QueryParams or QuerySpec object in repository methods.


QuerySpec vs. QueryParams
~~~~~~~~~~~~~~~~~~~~~~~~~~~

QueryParams is the traditional query api of Katharsis. QuerySpec is a new API 
with the purpose of simplifying the implementation of repositories and offering 100% JSON API compliance
See the next section for more information about JSON API compliance.

QuerySpec is a drop-in replacement for QueryParams in annotated repositories.
``ResourceRepository`` and ``RelationshipRepository`` make use of QueryParams.
``ResourceRepositoryV2`` and ``RelationshipRepositoryV2`` make use of QuerySpec.

For the time being, both QueryParams and QuerySpec are fully supported. It is also possible
to mix the use of both classes to gradually move from QueryParams to QuerySpec. The next section
outlines the necessary changes in the setup procedure to gain JSON API compliance.


JSON API compliance
~~~~~~~~~~~~~~~~~~~~

The subsequent sections outline URL conventions to query resources.
QueryParams does not fully adhere to the JSON API specification and instead
provides a number of improvements over the specification. QuerySpec strives to offer both,
JSON API compliance and some more advanced URL patterns.

Most notably, QuerySpec supports the ordered sorting on multiple attributes 
by providing an ordered list of those sorted attributes. And QueryParams 
introduced support to not only sort and filter requested resources, but also included related resources.
Because of this, sort and filter parameters require an additional type passed in the parameter name.
With QuerySpec this type becomes optional and the requested (root) type is used by default. The
following two requests are equivalent:

``GET /tasks/?sort[tasks]=!shortName,name``

and more simply just:

``GET /tasks/?sort=-shortName,name``

In order to enable the JSON API compliant URL handling, a ``QuerySpecDeserializer`` instead of ``QueryParamsBuilder``
has to be provided when setting up Katharsis (see the corresponding documentation for the
various technology stacks). Typically the default implementation ``DefaultQuerySpecDeserializer``
is perfectly fine. In JAX-RS it looks like:

.. code-block:: java

	@ApplicationPath("/")
	public class MyApplication extends Application {
	
		@Override
		public Set<Object> getSingletons() {
			DefaultQuerySpecDeserializer querySpecDeserializer = new DefaultQuerySpecDeserializer();
			KatharsisFeature feature = new KatharsisFeature(new ObjectMapper(), querySpecDeserializer, serviceLocator);
			return Collections.singleton((Object)feature);
		}
	}
	
or just


.. code-block:: java

	@ApplicationPath("/")
	public class MyApplication extends Application {
	
		@Override
		public Set<Class<?>> getClasses() {
			return Collections.singleton(Katharsis.class);
		}
	}

	
Have a look at the examples. All of them are setup to use QuerySpec. 
	
``DefaultQuerySpecDeserializer`` provides some customization options:

* ``setDefaultLimit(Long)``
	Sets the page limit if none is specified by the request.
	
* ``setIgnoreUnknownAttributes(boolean)``
	DefaultQuerySpecDeserializer validates all passed parameters against the domain model and fails
	if one of the attributes is unknown. This flag allows to disable that check in case the should be necessary.




Filtering
~~~~~~~~~

Resource filtering can be achieved by providing parameters which start with ``filter``.
The format for filters: ``filter[ResourceType][property|operator]([property|operator])* = "value"``

QuerySpec examples:

* ``GET /tasks/?filter[name]=Super task``
* ``GET /tasks/?filter[name][EQ]=Super task``
* ``GET /tasks/?filter[tasks][name]=Super task``
* ``GET /tasks/?filter[tasks][name]=Super task&[tasks][dueDate]=2015-10-01``

QueryParams examples:

* ``GET /tasks/?filter[tasks][name]=Super task``
* ``GET /tasks/?filter[tasks][name]=Super task&[tasks][dueDate]=2015-10-01``
* ``GET /tasks/?filter[tasks][name][EQ]=Super task``
* ``GET /tasks/?filter[tasks][name][][$startWith]=Super&[tasks][name][][$endWith]=task``

QuerySpec uses the ``EQ`` operator if no operator was provided. Custom operators can be registered
with ``DefaultQuerySpecDeserializer.addSupportedOperator(..)``. The default operator can be 
overridden by setting ``DefaultQuerySpecDeserializer.setDefaultOperator(...)``.


Sorting
~~~~~~~

Sorting information for the resources can be achieved by providing ``sort`` parameter.
QuerySpec uses the standard JSON API format. The QueryParams format for sorting 
is:  ``sort[ResourceType][property|operator]([property|operator])* = "value"``.

QuerySpec examples:

* ``GET /tasks/?sort=name,-shortName`` 
* ``GET /tasks/?sort[projects]=name,-shortName&include=projects`` 
  
QueryParams examples:

* ``GET /tasks/?sort[tasks][name]=asc`` 
* ``GET /tasks/?sort[tasks][id]=desc`` 


Grouping
~~~~~~~~

.. note::

  Grouping itself is not specified by JSON API itself, but the keyword and format it reserved for today and future use in Katharsis.

Grouping information for the resources can be achieved by providing ``group`` parameter.
The format for grouping: ``group[ResourceType] = "property(.property)*"``

Examples:

* ``GET /tasks/?group[tasks]=name``
* ``GET /tasks/?group[users]=name.firstName&include[projects]=team``

Pagination
~~~~~~~~~~

Pagination for the repositories can be achieved by providing ``page`` parameter.
The format for pagination: ``page[offset|limit] = "value", where value is an integer``

Example:

* ``GET /tasks/?page[offset]=0&page[limit]=10``


Note that JSON API specifies first, previous, next and last links (see http://jsonapi.org/format/#fetching-pagination).
Katharsis provides support to compute those pagination links. For this two work, a repository
has to return meta and links information implementing PagedMetaInformation resp. PagedLinksInformation.
With PagedMetaInformation the repository can let Katharsis know about the total number of (potentially filtered)
resources. Katharsis then fills in PagedLinksInformation with the corresponding links.



Sparse Fieldsets
~~~~~~~~~~~~~~~~

Information about fields to include in the response can be achieved by providing ``fields`` parameter.
QuerySpec follows again the JSON API specification. QueryParams makes use of this format: ``fields[ResourceType] = "property(.property)*"``.

QuerySpec examples:

* ``GET /tasks/?fields=name``
* ``GET /tasks/?fields[projects]=name,description&include=projects``

QueryParams examples:

* ``GET /tasks/?fields[tasks][]=name&fields[tasks][]=dueDate``
* ``GET /tasks/?fields[users]=name.surname&include[tasks]=author``



Inclusion of Related Resources
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Information about relationships to include in the response can be achieved by providing ``include`` parameter.
The format for fields: ``include[ResourceType] = "property(.property)*"``

Examples:

* ``GET /tasks/?include[tasks]=project``
* ``GET /tasks/1/?include[tasks]=project``
* ``GET /tasks/?include[tasks]=author``
* ``GET /tasks/?include[tasks][]=author&include[tasks][]=comments``
* ``GET /tasks/?include[projects]=task&include[tasks]=comments``
* ``GET /tasks/?include[projects]=task&include=comments`` (QuerySpec example)



QuerySpec API
~~~~~~~~~~~~~~~~~~~~~~~~

The use of QuerySpec eases the implementation of repositories with a slightly different API compared
to QueryParams. QueryParams holds parameters for all requested resource types (root and included relations)
simultaneously. A QuerySpec holds only the the parameters for a single resource type. A repository
is invoked with the QuerySpec for the requested root type. Because of this, it gives
direct access to sorting, filtering, pagination and inclusion parameters for the requested
root resource. If related resources are included in the request, their QuerySpecs 
can be obtained by calling ``QuerySpec.getRelatedSpec(Class)`` on the root QuerySpec. Next to that,
QuerySpec simplifies filter handling with a new filter API based on ``FilterSpec`` that should be a 
good match for most use cases. Compared to QueryParams it takes care of distinguishing attributes 
from operators in a String like ``tasks[title][EQ]=myTitle`` and marshals parameter values from Strings 
to the corresponding attribute type.  

The API looks like (further setters available as well):

.. code-block:: java

	public class QuerySpec {
		public <T> List<T> apply(Iterable<T> resources){...}
	
		public Long getLimit() {...}
	
		public long getOffset() {...}
	
		public List<FilterSpec> getFilters() {...}
	
		public List<SortSpec> getSort() {...}
	
		public List<IncludeFieldSpec> getIncludedFields() {...}
	
		public List<IncludeRelationSpec> getIncludedRelations() {...}
	
		public QuerySpec getQuerySpec(Class<?> resourceClass) {...}
		
		...	
	}


QuerySpec provides a method ``apply`` that allows in-memory sorting, filtering and paging
on any ``java.util.Collection``. It is useful for testing and on smaller datasets to keep
the implementation of a repository as simple as possible. It returns a ResourceList
that carries a PagedMetaInformation that lets Katharsis automatically compute pagination links.



Error Handling
--------------

Processing errors in Katharsis can be handled by throwing an exception and providing
a corresponding exception mapper which defines mapping to a proper JSON API error response.

Throwing an exception...
~~~~~~~~~~~~~~~~~~~~~~~~

Here is an example of throwing an Exception in the code:

.. code-block:: java

  if (somethingWentWrong()) {
    throw new SampleException("errorId", "Oops! Something went wrong.")
  }


Sample exception is nothing more than a simple runtime exception:

.. code-block:: java

  public class SampleException extends RuntimeException {

    private final String id;
    private final String title;

    public ExampleException(String id, String title) {
      this.id = id;
      this.title = title;
    }

    public String getId() {
      return id;
    }

    public String getTitle() {
      return title;
    }
  }


...and mapping it to JSON API response
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Class responsible for mapping the exception should:

* be annotated with ExceptionMapperProvider
* implement JsonApiExceptionMapper interface

Sample exception mapper:

.. code-block:: java

  @ExceptionMapperProvider
  public class SampleExceptionMapper implements JsonApiExceptionMapper<SampleException> {
    @Override
    public ErrorResponse toErrorResponse(SampleException exception) {
      return ErrorResponse.builder()
        .setStatus(HttpStatus.INTERNAL_SERVER_ERROR_500)
        .setSingleErrorData(ErrorData.builder()
          .setTitle(exception.getTitle())
          .setId(exception.getId())
          .build())
        .build();
    }
  }

Exception mapper classes will be scanned for and registered during application startup.
They should be located in your resource search package.

An exception should be mapped to an ErrorResponse object.
It consists of an HTTP status and ErrorData (which is consistent with JSON API error structure).

Note that the exception mapper is reponsible for providing the logging of exceptions with the
appropriate log levels. Also have a look at the subsequent section about the validation module that takes
care of JSR-303 bean validation exception mapping. 


Meta Information
----------------

.. note::
  With ResourceList and @JsonApiMetaInformation meta information can be returned directly. A MetaRepository implementation is no longer necessary.

There is a special interface which can be added to resource repositories to provide meta information: ``io.katharsis.repository.MetaRepository``.
It contains a single method ``MetaInformation getMetaInformation(Iterable<T> resources)`` which return meta information object that implements the marker ``interface io.katharsis.response.MetaInformation``.

If you want to add meta information along with the responses, all repositories (those that implement ``ResourceRepository`` and ``RelationshipRepository``) must implement ``MetaRepository``.

When using annotated versions of repositories, a method that returns a ``MetaInformation`` object should be annotated with ``JsonApiMeta`` and the first parameter of the method must be a list of resources.

Links Information
-----------------

.. note::
  With ResourceList and @JsonApiLinksInformation links information can be returned directly. A LinksRepository implementation is no longer necessary.

There is a special interface which can be added to resource repositories to provide links information: ``io.katharsis.repository.LinksRepository``.
It contains a single method ``LinksInformation getLinksInformation(Iterable<T> resources)`` which return links information object that implements the marker ``interface io.katharsis.response.LinksInformation``.

If you want to add meta information along with the responses, all repositories (those that implement ``ResourceRepository`` and ``RelationshipRepository``), must implement ``LinksRepository``.

When using annotated versions of repositories, a method that returns a ``LinksInformation`` object should be annotated with ``JsonApiLinks`` and the first parameter of the method has to be a list of resources.



JAX-RS integration
------------------

Katharsis allows integration with JAX-RS environments through the usage of JAX-RS specification. Under the hood there is a @PreMatching filter which checks each request for JSON API processing.

There are two ways to setup to integrate Katharsis into a JAX-RS application, depending on whether a dependency injection framework is in use.
In either case the instantiated ``KatharsisFeature`` has to be registered as a JAX-RS feature. 


Without Dependency Injection
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Have a look at the Dropwizard example to see how to setup Katharsis without dependency injection.

Katharsis require an instance of every resources repository it finds. To provide them, ``JsonServiceLocator`` interface has to be implemented. 
The created instance of ``JsonServiceLocator`` has to be provided to new instance of ``KatharsisFeature`` along with Jackson Databind ObjectMapper.

.. code-block:: java
	
	@ApplicationPath("/")
	public class MyApplication extends Application {
	
		@Override
		public Set<Object> getSingletons() {
			KatharsisFeature katharsisFeature = new KatharsisFeature(environment.getObjectMapper(),
	                new DefaultQuerySpecDeserializer(),
	                new SampleJsonServiceLocator());
			return Collections.singleton((Object)katharsisFeature);
		}
		
		@Override
		public Map<String, Object> getProperties() {
			Map<String, Object> map = new HashMap<>();
			map.put(KatharsisProperties.RESOURCE_SEARCH_PACKAGE, "com.myapplication.model")
			return map;
		}
	}

In order for Katharsis to find its resources and repository, the ``katharsis.config.core.resource.package`` configuration property must be passed
to JAX-RS. It allows configuring from which package should be searched to get models, repositories used by the core and exception mappers 
used to map thrown from repositories exceptions. Multiple packages can be passed by specifying a comma separated string 
of packages i.e. com.company.service.dto,com.company.service.repository. 



With Dependency Injection (CDI, Spring)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The setup is simplified if a dependency injection framework like CDI or Spring is available. In this case, Katharsis can lookup its repositories, modules,
etc. with that framework. To enable CDI support, add ``io.katharsis:katharsis-cdi`` to your classpath. Katharsis will then pickup the ``CdiServiceDiscovery`` implementation
and use it to discover its modules and repositories. An application then looks as simple as:

.. code-block:: java

	@ApplicationPath("/")
	public class WildflyApplication extends Application {
	
		@Override
		public Set<Class<?>> getClasses() {
			Set<Class<?>> set = new HashSet<>();
			set.add(KatharsisFeature.class);
			return set;
		}
	}


Have a look at the wildfly example. The Spring setup follows the same pattern with a ``SpringServiceDiscovery``
and is explained in a subsequent section.


Providing a configuration
~~~~~~~~~~~~~~~~~~~~~~~~~

There are three parameters that can be passed to the server to get the configuration.
All of them are defined in KatharsisProperties class:


* ``katharsis.config.core.resource.domain``

  Domain name as well as protocol and optionally port number used when building links objects in responses i.e. http://katharsis.io.
  The value must not end with ``/``. If the property is omitted, then they are extracted from the incoming request, which should work
  well for most use cases.

* ``katharsis.config.web.path.prefix`` (Optional)

  Default prefix of a URL path used in two cases:

  * When building ``links`` objects in responses
  * When performing method matching

  An example of a prefix ``/api/v1``.




Customizing KatharsisFeature 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

``KatharsisFeature`` has a number of  constructors and methods that allow to
customize its behavior. A more advanced setup may look like:

.. code-block:: java

	public class MyAdvancedKatharsisFeature implements Feature {
	
		@Inject
		private EntityManager em;
	
		@Inject
		private EntityManagerFactory emFactory;
	
		...
			
		@Override
		public boolean configure(FeatureContext featureContext) {
			featureContext.property(KatharsisProperties.RESOURCE_SEARCH_PACKAGE, ...);
			featureContext.property(KatharsisProperties.WEB_PATH_PREFIX, ...);
	
			// also map entities to JSON API resources (see further below)
			JpaModule jpaModule = new JpaModule(emFactory, em, transactionRunner);
			jpaModule.setRepositoryFactory(new ValidatedJpaRepositoryFactory());
	
			// JSON API compliant URL handling with QuerySpec
			DefaultQuerySpecDeserializer querySpecDeserializer = new DefaultQuerySpecDeserializer();
			
			// limit all incoming requests to 20 resources if not specified otherwise
			querySpecDeserializer.setDefaultLimit(20L);
			
			ServiceLocator serviceLocator = ...
			KatharsisFeature feature = new KatharsisFeature(new ObjectMapper(), querySpecDeserializer, serviceLocator);
			feature.addModule(jpaModule);
	
			featureContext.register(feature);
			return true;
		}
	}
	
Note that if the CDI or Spring integration is used, it will pickup any modules automatically.




Repository supported parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

JAX-RS integration allows a developer to pass the following types of parameters in repository methods:

* An instance of ``ContainerRequestContext``
* An instance of ``SecurityContext``
* A cookie. The parameter should be annotated with ``@CookieParam("cookie name")``.
  The type can be either ``Cookie``, ``String`` or any other type that Jackson can handle.
* A header. The parameter should be annotated with ``@HeaderParam("header name")``.
  The type can be either ``String`` or any other type that Jackson can handle.

Servlet integration
-------------------

There are two ways of integrating katharsis using Servlets:

* Adding an instance of ``AbstractKatharsisServlet``
* Adding an instance of ``AbstractKatharsisFilter``

Integrating using a Servlet
~~~~~~~~~~~~~~~~~~~~~~~~~~~

To integrate Katharsis using a servlet several steps are required.
The first one is to create a class that extends ``AbstractKatharsisServlet`` and will provide required configuration for the library.
The code below shows a sample implementation:

.. code-block:: java

  import io.katharsis.invoker.KatharsisInvokerBuilder;
  import io.katharsis.locator.JsonServiceLocator;
  import io.katharsis.locator.SampleJsonServiceLocator;

  import javax.servlet.ServletConfig;
  import javax.servlet.ServletException;

  public class SampleKatharsisServlet extends AbstractKatharsisServlet {

      private String resourceSearchPackage;
      private String resourceDefaultDomain;

      @Override
      public void init(ServletConfig servletConfig) throws ServletException {
          super.init(servletConfig);
          resourceSearchPackage = servletConfig
              .getInitParameter(KatharsisProperties.RESOURCE_SEARCH_PACKAGE);
          resourceDefaultDomain = servletConfig
              .getInitParameter(KatharsisProperties.RESOURCE_DEFAULT_DOMAIN);
      }

      /**
       * NOTE: A class extending this must provide a platform specific {@link JsonServiceLocator}
       *       instead of the (testing-purpose) {@link SampleJsonServiceLocator} below
       *       in order to provide advanced dependency injections for the repositories.
       */
      @Override
      protected KatharsisInvokerBuilder createKatharsisInvokerBuilder() {
          return new KatharsisInvokerBuilder()
              .resourceSearchPackage(resourceSearchPackage)
              .resourceDefaultDomain(resourceDefaultDomain)
              .jsonServiceLocator(new SampleJsonServiceLocator());
      }

  }

The newly created servlet must be added to the ``web.xml`` file or to another deployment descriptor.
The code below shows a sample ``web.xml`` file with a properly defined and configured servlet:

.. code-block:: java

  <web-app>
    <servlet>
      <servlet-name>SampleKatharsisServlet</servlet-name>
      <servlet-class>io.katharsis.servlet.SampleKatharsisServlet</servlet-class>
      <init-param>
        <param-name>katharsis.config.core.resource.package</param-name>
        <param-value>io.katharsis.servlet.resource</param-value>
      </init-param>
      <init-param>
        <param-name>katharsis.config.core.resource.domain</param-name>
        <param-value>http://localhost:8080</param-value>
      </init-param>
    </servlet>
    <servlet-mapping>
      <servlet-name>SampleKatharsisServlet</servlet-name>
      <url-pattern>/api/v1/ *</url-pattern>
    </servlet-mapping>
  </web-app>


Integrating using a filter
~~~~~~~~~~~~~~~~~~~~~~~~~~

To integrate Katharsis using a filter, several steps are required.
First, create a class that extends ``AbstractKatharsisFilter``, which will provide required configuration for the library.
The code below shows a sample implementation:

.. code-block:: java

  import io.katharsis.invoker.KatharsisInvokerBuilder;
  import io.katharsis.locator.JsonServiceLocator;
  import io.katharsis.locator.SampleJsonServiceLocator;

  import javax.servlet.FilterConfig;
  import javax.servlet.ServletException;

  public class SampleKatharsisFilter extends AbstractKatharsisFilter {

      private String resourceSearchPackage;
      private String resourceDefaultDomain;

      public void init(FilterConfig filterConfig) throws ServletException {
          super.init(filterConfig);
          resourceSearchPackage = filterConfig
              .getInitParameter(KatharsisProperties.RESOURCE_SEARCH_PACKAGE);
          resourceDefaultDomain = filterConfig
              .getInitParameter(KatharsisProperties.RESOURCE_DEFAULT_DOMAIN);
      }

      @Override
      public void init(FilterConfig filterConfig) throws ServletException {
          super.init(filterConfig);
          resourceSearchPackage = filterConfig
              .getInitParameter(KatharsisProperties.RESOURCE_SEARCH_PACKAGE);
          resourceDefaultDomain = filterConfig
              .getInitParameter(KatharsisProperties.RESOURCE_DEFAULT_DOMAIN);
      }

      /**
       * NOTE: A class extending this must provide a platform specific {@link JsonServiceLocator}
       *       instead of the (testing-purpose) {@link SampleJsonServiceLocator} below
       *       in order to provide advanced dependency injections for the repositories.
       */
      @Override
      protected KatharsisInvokerBuilder createKatharsisInvokerBuilder() {
          return new KatharsisInvokerBuilder()
              .resourceSearchPackage(resourceSearchPackage)
              .resourceDefaultDomain(resourceDefaultDomain)
              .jsonServiceLocator(new SampleJsonServiceLocator());
      }
  }

The newly created filter must be added to ``web.xml`` file or other deployment descriptor.
A code below shows a sample ``web.xml`` file with properly defined and configured filter

.. code-block:: xml

  <web-app>
    <filter>
      <filter-name>SampleKatharsisFilter</filter-name>
      <filter-class>io.katharsis.servlet.SampleKatharsisFilter</filter-class>
      <init-param>
        <param-name>katharsis.config.web.path.prefix</param-name>
        <param-value>/api/v1</param-value>
      </init-param>
      <init-param>
        <param-name>katharsis.config.core.resource.package</param-name>
        <param-value>io.katharsis.servlet.resource</param-value>
      </init-param>
      <init-param>
        <param-name>katharsis.config.core.resource.domain</param-name>
        <param-value>http://localhost:8080</param-value>
      </init-param>
    </filter>
    <filter-mapping>
      <filter-name>SampleKatharsisFilter</filter-name>
      <url-pattern>/api/v1/ *</url-pattern>
    </filter-mapping>
  </web-app>


Repository supported parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Servlet integration allows the following types of parameters in repository methods:

* An instance of ``ServletContext``
* An instance of ``HttpServletRequest``
* An instance of ``HttpServletResponse``


Spring integration
------------------

Katharsis provides a simple Spring Boot integration using the ``@Configuration`` annotated class ``KatharsisConfigV3``.
Using this class, the only thing needed to allow Katharsis process requests is parameter configuration.
An example ``application.properties`` file is presented below.

.. code-block:: bash

  katharsis.domainName=http://localhost:8080
  katharsis.pathPrefix=/api

Spring integration uses katharsis-servlet ``AbstractKatharsisFilter`` to fetch the requests. Similar to CDI, repositories
and modules are picked up from the Spring ApplicationContext with  ``SpringServiceDiscovery``.


Repository supported parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Spring integration allows a developer to pass all of the types supported by Spring which don't operate on the response.



Vertx integration
-----------------

Katharsis provides ``Handler`` that intercepts requests and delegates them to Katharsis.

.. code-block:: bash

  dependencies {
      compile 'io.katharsis:katharsis-vertx:<version>'
  }


Simple usage example that creates the handler:

.. code-block:: java

  KatharsisHandler katharsisGlue = KatharsisHandlerFactory.create(Main.class.getPackage().getName(), "/api");
  router.route("/api/*").handler(katharsisGlue);

Advanced usage that shows how you can inject custom parameters in Katharsis repository methods:

.. code-block:: java

  ParameterProviderFactory factory = new SpringParameterProviderFactory(Json.mapper, context);

  KatharsisHandler katharsisGlue = KatharsisHandlerFactory.create(Main.class.getPackage().getName(), "/api",
  Json.mapper, new CustomParameterProviderFactory(Json.mapper, context));
  router.route("/api/*").handler(katharsisGlue);


Client
-----------------

Since v2.6.0 there is a new Katharsis client support for Java projects to allow
communicating with JSON-API compliant servers. Two http client libraries are supported:

* `OkHttp <http://square.github.io/okhttp>`
  Library has been used to allow usage in both Android and server applications and services.

* `Apache Http Client <https://hc.apache.org/httpcomponents-client-ga/index.html>`
  Library widely used in the Java community.
  
Add one of those library to the classpath and Katharsis will pick it up automatically.
  
The client requires to define resources in the same manner as defined in the `Models`_ section.
To start using the client just create an instance of ``KatharsisClient`` and pass the service
URL and the location to the package where the models are defined.

The client has three main methods:

* ``KatharsisClient#getResourceRepository(Class)`` to obtain a resource repository stub from an existing repository interface.
* ``KatharsisClient#getQuerySpecRepository(Class)`` to obtain a generic resource repository stub from the provided resource type.
* ``KatharsisClient#getQuerySpecRepository(Class, Class)`` to obtain a generic relationship repository stub from the provided source and target resource types.

The interface of the repositories is as same as defined in `Repositories`_ section.

An example of the usage:

.. code-block:: java

  KatharsisClient client = new KatharsisClient("http://localhost:8080/api");
  ResourceRepositoryV2<Task, Long> taskRepo = client.getQuerySpecRepository(Task.class);
  List<Task> tasks = taskRepo.findAll(new QuerySpec(Task.class));

Have a look at, for example, the QuerySpecClientTest to see more examples of how it is used.


Enjoy.


Modules
-----------------

Katharsis has a module API that allows to extend the core functionality by third-party contributions.
The mentioned JPA module in the next section is an example for that. The API is similar in spirit
to the one of the ``https://github.com/FasterXML/jackson``. The main interface is ``Module`` with
a default implementation provided by ``SimpleModule``. A module has access to a ``ModuleContext``
that allows to register all kinds of extensions like new ``ResourceInformationBuilder``,
``ResourceLookup``, ``Filter``, ``ExceptionMapper`` and Jackson modules. It also gives access to the
``ResourceRegistry`` holding information about all the repositories registered to katharsis.
The ``JpaModule`` in ``katharsis-jpa`` provides a good, more advanced example of using the
module API.



Request Filtering
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The ``Filter`` interface provided by Katharsis allows to intercept incoming requests and do 
any kind of validation, changes, monitoring, transaction handling, etc. ``Filter`` can be 
hooked into Katharsis by setting up a module and registering the filter to the 
``ModuleContext``.

A request may span multiple repository accesses. To intercept the actual repository requests,
implement the ``RepositoryFilter`` interface. ``RepositoryFilter`` has a number of methods
that allow two intercept the repository request at different stages. Like ``Filter`` it can be 
hooked into Katharsis by setting up a module and registering the filter to the 
``ModuleContext``. 


JPA Module
-------------

The JPA module allows to automatically expose JPA entities as JSON API repositories. No implementation
or Katharsis-specific annotations are necessary.

The feature set includes:

- expose JPA entities to JSON API endpoints
- expose JPA relations as JSON API endpoints
- decide which entities to expose as endpoints
- sorting, filtering, paging, inclusion of related resources
- JPA filter API to modify the issued queries
- JPA Criteria API and QueryDSL support
- DTO mapping support
- support for computed attributes behaving like regular, persisted attributes.


JPA Setup
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To use the module, add a dependency to ``io.katharsis:katharsis-jpa`` and register the ``JpaModule`` 
to Katharsis. For example in the case of JAX-RS:

.. code-block:: java

	TransactionRunner transactionRunner = ...;
	JpaModule jpaModule = JpaModule.newServerModule(entityManagerFactory, entityManager, transactionRunner);
	jpaModule.setRepositoryFactory(new ValidatedJpaRepositoryFactory());
	
	KatharsisFeature feature = new KatharsisFeature(...);
	feature.addModule(jpaModule);
			

The JPA modules by default looks up the entityManagerFactory and obtains a list
of registered JPA entities. For each entity a instance of ``JpaEntityRepository``
is registered to Katharsis using the module API. Accordingly, every relation
is registered as ``JpaRelationshipRepository``. ``JpaModule.setRepositoryFactory``
allows to provide a factory to change or customized the used repositories.
To manually select the entities exposed to Katharsis use ``JpaModule.addEntityClass(...)`` 
and ``JpaModule.removeEntityClass(...)``. If no ``entityManagerFactory`` is provided
to newServerModule, then the registartion of entities is omitted and can be done
manually.
	
The transactionRunner needs to be implemented by the application to hook into the
transaction processing of the used environment (Spring, JEE, etc.). This might be
as simple as a Spring bean implementing ``TransactionRunner`` and adding a 
``@Transactional`` annotation. The JPA module makes sure that every call to a 
repository happens within such a transaction boundary.

To setup a Katharsis client with the JPA module use:


.. code-block:: java

	client = new KatharsisClient(getBaseUri().toString(), ...);

	JpaModule module = JpaModule.newClientModule(TestEntity.class.getPackage().getName());
	setupModule(module, false);
	client.addModule(module);
	
The JpaModule takes care of the lookup of the entities and registering them to Katharsis
with the provided package passed to ``newClientModule``.	

Have a look at https://github.com/katharsis-project/katharsis-framework/blob/develop/katharsis-jpa/src/test/java/io/katharsis/jpa/JpaQuerySpecEndToEndTest.java within the ``katharsis-jpa``
test cases to see how everything is used together with ``katharsis-client``.
The JPA modules further has a number of more advanced customization options that
are discussed in the subsequent sections.


Criteria API and QueryDSL
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The JPA module can work with two different query APIs, the default Criteria API
and QueryDSL. ``JpaModule.setQueryFactory`` allows
to choose between those two implementation. There is the ``JpaCriteriaQueryFactory``
and the ``QuerydslQueryFactory``. By default the Criteria API is used.
QueryDSL sits on top of JPQL and has to advantage of being easier to use. 


Customizing the JPA repository
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The setup page outlined the ``JpaRepositoryFactory`` that can be used to hook a custom JPA repository
implementations into the JPA module. The JPA module further provides a more
lightweight filter API to perform various changes to JPA repository requests:

``JpaModule.addFilter(new MyRepositoryFilter())``

A filter looks like:

.. code-block:: java

	public class MyRepositoryFilter extends JpaRepositoryFilterBase {

		boolean accept(Class<?> resourceType){...}

		<T, I extends Serializable> JpaEntityRepository<T, I> filterCreation(JpaEntityRepository<T, I> repository){...}
	
		QuerySpec filterQuerySpec(Object repository, QuerySpec querySpec){...}
		
		...
	}


The various filter methods allow a wide variety of customizations or also to replace the passed object in question.


DTO Mapping
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Mapping to DTO objects is supported with ``JpaModule.registerMappedEntityClass(...)``.
A mapper then can be provided that translates the Entity to a DTO class.
Such a mapper might be implemented manually or generated (mostly) automatically
with tools like MapStruct. If two mapped entities are registered, there
respective mapped relationships will be automatically registered as well. 

The mechanism is not limited to simple mappings, but can also introduce computed 
attributes like in the example depicted here:

.. code-block:: java

	JpaModule module = JpaModule.newServerModule(emFactory, em, transactionRunner);
				module.setQueryFactory(QuerydslQueryFactory.newInstance());
	QuerydslExpressionFactory<QTestEntity> basicComputedValueFactory = new QuerydslExpressionFactory<QTestEntity>() {

		@Override
		public Expression<String> getExpression(QTestEntity parent, JPAQuery<?> jpaQuery) {
			return parent.stringValue.upper();
		}
	};

	QuerydslQueryFactory queryFactory = (QuerydslQueryFactory) module.getQueryFactory();
	queryFactory.registerComputedAttribute(TestEntity.class, TestDTO.ATTR_COMPUTED_UPPER_STRING_VALUE,
		 String.class, basicComputedValueFactory);
	module.addMappedEntityClass(TestEntity.class, TestDTO.class, new TestDTOMapper(entityManager));
	
and

.. code-block:: java
	
	public class TestDTOMapper implements JpaMapper<TestEntity, TestDTO> {
	
		@Override
		public TestDTO map(Tuple tuple) {
			TestDTO dto = new TestDTO();
			TestEntity entity = tuple.get(0, TestEntity.class);
			dto.setId(entity.getId());
			dto.setStringValue(entity.getStringValue());
			dto.setComputedUpperStringValue(tuple.get("computedUpperStringValue", String.class));
			...
			return dto;
		}
		
		...
	
	}

Some of the regular entity attributes are mapped to the DTO. But there is also a 
``computedUpperStringValue`` attribute that is computed with an expression.
The expression can be written with the Criteria API or QueryDSL depending
on which query backend is in use.

Computed attributes are indistinguishable from regular, persisted entity attributes.
They can be used for selection, sorting and filtering. Both ``JpaCriteriaQueryFactory`` 
and ``QuerydslQueryFactory`` provide a ``registerComputedAttribute`` method to 
register an expression factory to create such computed attributes. The registration requires 
the target entity and a name. To make the computed attribute available
to consumers, the mapper class has access to it trough the provided 
tuple class. Have a look at https://github.com/katharsis-project/katharsis-framework/blob/develop/katharsis-jpa/src/test/java/io/katharsis/jpa/mapping/DtoMappingTest.java to see everything in use.

There is currently not yet any support for renaming of attribute. If attributes
are renamed on DTOs, the incoming QuerySpec has to be modified accordingly to
match again the entity attribute naming.



JSR 303 Validation Module
-------------------------

A ``ValidationModule`` provided by ``io.katharsis:katharsis-validation`` implements 
exception mappers for 'javax.validation.ValidationException' and 'javax.validation.ConstraintViolationException'.
Among others, it properly translates 'javax.validation.ConstraintViolation' instances to JSON API errors.
A JSON API error can, among others, contain a source pointer. This source pointer allows a clients/UI to
display the validation errors next to the corresponding input fields.


Tracing with Zipkin/Brave
-------------------------

A ``BraveModule`` provided by ``io.katharsis:katharsis-brave`` provides integration into
Zipkin/Brave to implement tracing for your repositories.  The module is applicable to 
both a Katharsis client or server.

The Katharsis client can make use of either HttpClient or OkHttp to issue HTTP requests.
Accordingly, a matching brave integration must be added to the classpath:

* ``io.zipkin.brave:brave-okhttp``
* ``io.zipkin.brave:brave-apache-http-interceptors``

The ``BraveModule`` then takes care of the integration and will create a client span
for each request.

On the server-side, ``BraveModule`` creates a local span for each accessed repository.
Every request triggers one or more repository accesses (depending on whether 
relations are included). Note however that ``BraveModule`` does not setup tracing
for incoming requests. That is the purpose of the JAX-RS/servlet integration of Brave.


