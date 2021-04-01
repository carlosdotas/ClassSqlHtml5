# ClassSqlHtml5
 Class que Implementa Sql em HTML5

## Funções Basicas 

	const db = new Sql({
		dbName:'Vendas',
		onExec:function(values){
			console.log(values);
		},
		onRead:function(values){
			console.log(values);
		}		
	});

	db.delTable({
		table:'produtos',
		onDelTable:function(value){
			console.log(value);
		}
	});

	db.insert({
		table:'produtos',
		values:{cod:'21',name:'Gelatina',preco:25.90},
		onInsert:function(value){
			console.log(value);
		}
	});

	db.update({
		table:'produtos',
		id:5,
		values:{cod:'25',name:'Gelatina2',preco:25.90},
		onUpdate:function(value){
			console.log(value);
		}	
	});

	db.read({
		table:'produtos',
		//id:10,
		//filtro:{cod:21},
		onRead:function(value){
			console.log(value);
		}
	});

	db.del({
		table:'produtos',
		id:4,
		onDel:function(value){
			console.log(value);
		}	
	});