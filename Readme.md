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
		Remove do staged, que é quando eu faço git add no arquivo.
		
		*
		git reset --soft [passo a hash do arquivo anterior ao q eu quero deletar]
		Deleta do último commited até a hash que vc passar mas o arquivo fica em staged preparado para o commit de novo, ou seja, retorna o commit.
		
		*
		git reset --mixed [passo a hash do arquivo anterior ao q eu quero deletar]
		Deleta do último commited até a hash que vc passar mas o arquivo fica fica preparado para ir para o staged. Com isso, posso chamar o checkout para sobrepor minha alteração
		
		*
		git reset --hard [passo a hash do arquivo anterior ao q eu quero deletar]
		Mata o commit e qualque modificação, ou seja, mata o commit e volta para um ponto definido.
		
		
[GitHub]
	Estes são comandos de Git, utilizados no Git.CMD
	
		*
		Criar Repositório -> No próprio GitHub
		
		*
		O próprio GitHub te passa os comando para o CLI
		O nome 'origin' é um nome do repositório original que poderia ser substituido por qq nome.
		
		*
		git remote
		Mostra os repositórios disponíveis
		
		*
		git remote -v
		Mostra as opções do repositório
		
		*
		git push -u origin master
		Envia todos meus arquivos, as moficações para o repositório. O -u serve para trackear e não ter que digitar isso tudo de novo no próximo push. 
		origin -> pra onde vai. master -> de onde vem. Ou seja, vem do branch MASTER e vai pro ORIGIN.
		
		
		*
		git push origin master
		Envia para o repositório de para o ORIGIN para o MASTER
	
	
	[Branch]
		Branch é um ponteiro móvel que leva a um commit.
		Posso apontar um outro Branch para o mesmo commit, ou ter Branchs em commits diferentes
		
			* Vantagens
				Posso modificar meus arquivos sem alterar meu local principal, meu master
				Por exemplo, posso corrigir um Bug enquanto tem outras pessoas trabalhando no Branch Master
				Ele é facilmente desligável
				Posso ter multiplas pessoas trabalhando
				Evita conflito, pois cada branch não interfere em outro e o commit dele para o master entra somente no ponto de destino na linha do tempo, sem conflito com outros usuário, permite tbm a mescla de arquivos alterados.
				
				
		*
		git checkout -b "nome do branch"
		Cria um novo branch e me posiciona nele.
		
		*
		git branch
		Mostra os branch existentes e mostra o asterisco no branch onde estou no momento
		
		*
		git checkout "nome do branch"
		Mudo de branch
		
		*
		git branch -D "nome do branch"
		Deleta o branch indicado
		
	
	[Merge e Rebase]
		.União dos Branchs.Mescla de arquivos.
		
		[Merge]
			Mescla os arquivos
			Pró -> Operação não destrutiva
			Contra <- Commit extra no final do projeto, que serve para encerrar o ciclo dos branchs
			Contra <- Deixa o histórico poluído, deixando complicado de entender as ramificações
			* Ideal para times
		[Rebase]
			Pega tudo que estiver em outros branchs e adiciona na frente, cada um na frente do outro, no branch master, o que faz permanecer de forma linear, não gerando a confusao do merge e suas ramificações.
			Pró -> Evita commit extra
			Pró -> Histórico linear
			Contra <- Perde a ordem cronológica, pq o commit sempre entra no inicio da fila.
			* Ideal para uso onde tenho sincronicidade de entrega e delegação... uma entrega para outra delegação
		
		*
		git checkout "nome do branch"
		Muda de branch
		
		*
		git merge "nome do branch"
		Faz o merge do branch descrito para o atual.
		
		*
		git rebase "nome do branch"
		Faz o rebase do branch descrito para o atual.
		
	
	[Git Stash]
		Guarda o arquivo atual que ainda não foi commited num status paralelo, WIP - Working In Progress.
		Exemplo de uso: Digamos que eu precise ir para outro Branch, mas não quero commitar meus arquivos pq nao os terminei, então adiciono os arquivos ao git stath.
		
		*
		git stash
		Guarda a modificação do arquivo atual num status WIP.
		
		*
		git stash apply
		Aplica as mudanças que eu tinha guardado.
		
		*
		git stash list
		Lista meus arquivos no WIP.
		
		*
		git stash clear
		Limpa meus arquivos da lista do WIP.
		
		
	[Alias]
		Posso configurar atalhos no teclado, por exemplo, ao invés de passar git status, posso passar git seja
		
		*
		git config --global alias.s status
		Associa o s ao status, permitindo que eu passe apenas git s ao invés de git status.
		
	[Tag]
		Crio tags para faciliar minhas marcações. Por exemplo, ao final de uma alteração de um arquivo, ao encerrá-lo, posso marcar uma tag de fechamento para faciliar a localização posteriormente.
		
		*
		git tag -a 1.0.0 -m "Readme.md finalizado"
		Inferi a tag anotated, com um message ao arquivo atual.
		
		*
		git push origin master --tags
		Levo as tags para o GitHub, incrementando a aba RELEASE com a versão do arquivo que eu subi.
		
		*
		git tag
		Vejo todas as tags geradas.
		
		*
		
		
		
			
			
			
		
		
				
	
