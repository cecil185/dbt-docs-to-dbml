# dbt-erdiagram-generator
This is a simple packages built to autogenerate dbml files and render ERD diagrams for dbt. The code is create on a late friday, thus it could be optimized a bit. It is mainly for inspirations purpose. 

Data documentation often gets outdated. We thought that if you use dbt you have awesome autogenerated docs. From the docs all the data needed to create an ERD diagram should be present. Thus this little project came to life. 

There are some great ways to auto generate ERD diagrams. Thus, we just want to build a bridge between dbt and these tools. This is done by converting the dbt schema and catalog to a dbml files. From this dbml file a ERD diagram can be created with a tool like [dbdocs](https://dbdocs.io/) or [dbml-renderer](https://github.com/softwaretechnik-berlin/dbml-renderer). 

# Installation

1. Clone this repository to a folder and run:

```
pip install src/
```

or direct from git

```
pip install -U git+https://github.com/cecil185/dbt-docs-dml#subdirectory=src
```

2. Setup dbdocs cli for diagram creations. [Instructions here](https://dbdocs.io/docs)
3. Test dbterd with the following command:
```
dbterd tests/schema.yml tests/catalog.json test.dbml test True
```
# Usage
To use this packages on your own project run *dbterd* with the following parameters in order: 

1. Path to the dbt schema 
2. Path to the dbt catalog 
3. Path to store the dbml file
4. Name of the project on dbdocs.io
5. True or False if you want to vizualise the dbml file on dbdocs.io

# Tests


# To-Do
* Code cleanup 
* 
