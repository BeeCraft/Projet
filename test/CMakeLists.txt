cmake_minimum_required(VERSION 2.6)

#Déclaration du nom du projet
project(MyProject)

#Génération de la liste des fichiers sources
#Le premier paramètre est le  type d'opération à exécuter. La variante GLOB_RECURSE cherche dans les sous-dossiers des dossiers spécifiés.
#Le second paramètre est le nom de la variable créée
#Chemin désignant où les fichiers vont être recherchés

file(
	GLOB_RECURSE
	source_files
)

#Déclaration de l'exécutable. On utilise la variable dynamique que nous venons de créer pour définir les fichiers sources
add_executable(
	my_exe
	test.cpp
)
