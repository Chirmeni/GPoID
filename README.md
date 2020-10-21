# GPoID-Paraminer
Gradual Patterns over Imprecise Data  pour les bases de données non temporelles

			 ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
				 README


			  Michaël Chirmeni Boujike
			 ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━


GPoID-ParaMiner est un algorithme générique et parallèle pour la fouille des motifs
graduels fréquents fermés dans les bases de données transactionnelles lorsque le 
seuil de gradualité est pris en compte.
Les seuils de gradualité considérés ici sont : 
 - le coefficiant de variation (cv);
 - l'écarttype (sd);
 - et l'écarttype des écart (st).


1 Démarrer rapidement
═════════════════════

 Télécharger GPoID-ParaMiner
──────────────────────

  lien:
  [https://github.com/Chirmeni/GPoID-Paraminer]


 Extraire le fichier archivé
────────────────────────────

  ╭────
  │ tar xzvf GPoID-ParaMiner-1.0.tgz
  ╰────


 Compiler GPoID-ParaMiner
─────────────────────────

  ╭────
  │ cd GPoID-ParaMiner
  │ ./configure 
  │ make
  │ make install 
  ╰────

  Va installer dans le repertoire par défaut /usr/local. Vous pouvez spécifier 
  différent repertoire d'installation avec –prefix:
  ╭────
  │ ./configure --prefix=<path/to/install_dir>
  ╰────

  Si vous ne souhaitez pas installer, le fichier exécutable de GPoID-Paraminer peut
  être trouvé dans <paraminer>/src/ directory.


 Exécution GPoID-ParaMiner
──────────────────────────

  ╭────
  │ ./paraminer_graduals <dataset_file> <minSupp> <k1> <k2> <gradual_threshold> -t <number_of_threads> > <output_file>
  ╰────
  where :
	- dataset_file : base de données numérique;
	- minSupp : support minimum;
	- k1 et k2 sont des constants;
	- gradual_threshold : seuil graduel sélectionné parmis cv, sd and st;
	- number_of_threads : nombre de threads;
	- output_file : fichier de sorti qui contient les motifs graduels fréquents.

Exemple :   
  ╭────
  │ ./paraminer_graduals test.dat 0.2 1 0 cv -t 2 > result.out
  ╰────  
  
  
 Auteurs et licence
═════════════════════

  Authors:
  • Michaël Chirmeni Boujike
  • Jerry Lonlac
  • Norbert Tsopze
  • Engelbert Mephu Nguifo
