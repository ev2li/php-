# php-源码
php源码学习

b zend_compile
 p *compiler_globals.ast

p *(zend_ast_list*)compiler_globals.ast

p *((zend_ast_list*)compiler_globals.ast).child[0]

 p *(((zend_ast_list*)compiler_globals.ast).child[0]).child[0]
 
 p *((((zend_ast_list*)compiler_globals.ast).child[0]).child[0]).child[1]
 
 
 p *(((zend_ast_list*)compiler_globals.ast).child[0]).child[1]

 
