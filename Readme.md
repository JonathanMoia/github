Bem vindo!
==========
Este é um repositório teste para verificar como o  Git funciona.
==================================================================

[Git]
	Estes são comandos de Git, utilizados no Git.CMD

		*
		git init
		Inicializa um diretório Git na pasta
		
		*
		git status
		Verifica o status do Branch
		
		*
		git add Arquivo.js
		Adiciona o arquivo ao Branch, mas sem commit
		
		*
		git commit -m "Mensagem de alteração do arquivo"
		Commit do arquivo e passa mensagem de log
		
		*
		git commit -am "mensagem"
		Adiciona todos os arquivos alterados e comenta
		
		*
		git log
		Me mostra os logs de alteração dos arquivos		
		
		*
		git log --decorate
		Mostra o log com informação de troca de branch, etc
		
		*
		git log --author="Rafael"
		Mostra logs de author específico
		
		*
		git shortlog
		Mostra logs dos authors e suas alterações
		
		*
		git shortlog -sn
		Mostra somatória de alterações dos authors
		
		*
		git log --graph
		Mostra o repositório de forma grafica
		
		*
		git show 7f39ed4536436bb3d804de19d8b947c262c8ddcc
		Passar a hash para ver exatamento a alteração feita no arqivo
		
		*
		git diff
		Mostra a diferença do arquivo que estou mexendo antes de eu fazer commit
		
		*
		git diff --name-only
		Diz somente o nome do arquivo modificado
		
		*
		git checkout Nomedoarquivo.extencao
		Carrega um arquivo do git pra sua maquina, pode sobrepor um arquivo
		
		*
		git reset HEAD
		Remove do staged, que é quando eu faço git add no arquivo
		
		*
		git reset --soft [passo a hash do arquivo anterior ao q eu quero deletar]
		Deleta do último commited até a hash que vc passar mas o arquivo fica em staged preparado para o commit de novo
		
		*
		git reset --mixed [passo a hash do arquivo anterior ao q eu quero deletar]
		Deleta do último commited até a hash que vc passar mas o arquivo fica fica preparado para ir para o staged. Com isso, posso chamar o checkout para sobrepor minha alteração
		
		*
		git reset --hard [passo a hash do arquivo anterior ao q eu quero deletar]
		Mata o commit e qualque modificação
		
		
[GitHub]
	Estes são comandos de Git, utilizados no Git.CMD
	
		*