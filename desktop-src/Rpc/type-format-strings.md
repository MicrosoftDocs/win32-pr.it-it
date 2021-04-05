---
title: Stringhe di formato del tipo
description: I caratteri di formato denotano gli oggetti di interesse per il motore NDR.
ms.assetid: 71117082-07b0-4ba4-a920-09be8d8427ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f618d857e487f86e2d28ed18300d82e94b76e3a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045078"
---
# <a name="type-format-strings"></a>Stringhe di formato del tipo

I caratteri di formato denotano gli oggetti di interesse per il motore NDR. È presente un carattere di formato per ogni tipo di base, per vari tipi complessi e per le descrizioni di puntatori, compressione, allineamento e altri oggetti esterni. Per i tipi composti, vengono riconosciute diverse categorie di strutture e matrici in base alle rispettive proprietà delle prestazioni. Una stringa di formato per ogni categoria inizia con un token FC che identifica la stringa di formato particolare. I caratteri di formato per le categorie di strutture e matrici possono condividere le correzioni in nel nome del token FC principale mostrato nella tabella seguente.



| Formato carattere | Descrizione                                    |
|------------------|------------------------------------------------|
| C                | Indica le informazioni di conformità nel tipo. |
| V                | Indica le informazioni sulla varianza nel tipo.    |
| P                | Indica che i puntatori fanno parte del tipo.     |



 

Ad esempio, FC \_ CSTRUCT e FC \_ CArray identificano rispettivamente la struttura conforme e i descrittori di matrici conformi.

Di seguito sono riportati i caratteri di formato con significati speciali.



| Formato carattere | Descrizione                                                                         |
|------------------|-------------------------------------------------------------------------------------|
| \_PP FC           | Indica l'inizio della sezione della descrizione del puntatore di una struttura o di una matrice. |



 

Le stringhe di formato di tipo NDR RPC sono descritte in modo più dettagliato negli argomenti seguenti:

-   [Tipi semplici](simple-types-tfs.md)
-   [Pointers](pointers-tfs.md)
-   [Matrici](arrays-tfs.md)
-   [Stringhe](strings-tfs.md)
-   [Descrittori di correlazione](correlation-descriptors-tfs.md)
-   [Strutture](structures-tfs.md)
-   [Layout puntatore](pointer-layout-tfs.md)
-   [Unioni](unions-tfs.md)
-   [Trasmettere \_ come e rappresentare \_ come](transmit-as-and-represent-as-tfs.md)
-   [Marshalling utente](user-marshal-tfs.md)

 

 




