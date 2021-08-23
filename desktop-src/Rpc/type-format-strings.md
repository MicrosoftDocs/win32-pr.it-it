---
title: Stringhe di formato dei tipi
description: I caratteri di formato indicano gli oggetti di interesse per il motore NDR.
ms.assetid: 71117082-07b0-4ba4-a920-09be8d8427ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f4aa17494cbef0f3bcc232f89104e3502f94de4a3285a1da6cc0229af0fe26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011119"
---
# <a name="type-format-strings"></a>Stringhe di formato dei tipi

I caratteri di formato indicano gli oggetti di interesse per il motore NDR. È disponibile un carattere di formato per ogni tipo di base, per vari tipi complessi e per le descrizioni di puntatori, di creazione di un pacchetto, di allineamento e di altri oggetti vari. Per i tipi composti, diverse categorie di strutture e matrici vengono riconosciute in base alle relative proprietà delle prestazioni. Una stringa di formato per ogni categoria inizia con un token fc che identifica la stringa di formato specifica. I caratteri di formato per le categorie di strutture e matrici possono condividere le correzioni nel nome del token FC iniziale illustrato nella tabella seguente.



| Carattere di formato | Descrizione                                    |
|------------------|------------------------------------------------|
| C                | Indica informazioni sulla conformità nel tipo. |
| V                | Indica informazioni sulla varianza nel tipo.    |
| P                | Indica che i puntatori fanno parte del tipo .     |



 

Ad esempio, FC CSTRUCT e FC CARRAY identificano rispettivamente la struttura conforme e i descrittori di matrice \_ \_ conformi.

Di seguito sono riportati i caratteri di formato con significati speciali.



| Carattere di formato | Descrizione                                                                         |
|------------------|-------------------------------------------------------------------------------------|
| FC \_ PP           | Indica l'inizio della sezione di descrizione del puntatore di una struttura o di una matrice. |



 

Le stringhe di formato di tipo NDR RPC sono descritte in modo più dettagliato negli argomenti seguenti:

-   [Tipi semplici](simple-types-tfs.md)
-   [Pointers](pointers-tfs.md)
-   [Matrici](arrays-tfs.md)
-   [Stringhe](strings-tfs.md)
-   [Descrittori di correlazione](correlation-descriptors-tfs.md)
-   [Strutture](structures-tfs.md)
-   [Layout dell'indicatore di misura](pointer-layout-tfs.md)
-   [Unioni](unions-tfs.md)
-   [\_Trasmetti come e Rappresenta \_ come](transmit-as-and-represent-as-tfs.md)
-   [Marshalling dell'utente](user-marshal-tfs.md)

 

 




