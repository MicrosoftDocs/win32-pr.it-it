---
description: ICE14 convalida la tabella delle funzionalità di un database Windows Installer.
ms.assetid: fb1970f8-1dba-4b06-aa03-5b33d213fc79
title: ICE14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85a0789b7844fcbee52654d29b700b167a073fa51778ef3882b1fcbe2864fbb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638171"
---
# <a name="ice14"></a>ICE14

ICE14 convalida quanto segue per le funzionalità:

-   Per le funzionalità padre radice non è impostato il bit msidbFeatureAttributesFollowParent nella colonna Attributi della [tabella Funzionalità](feature-table.md). Una funzionalità radice non ha un elemento padre.
-   Nessuna funzionalità ha la stessa voce nelle colonne Feature e Feature \_ Parent della tabella [Feature](feature-table.md). Nessuna funzionalità può essere il proprio elemento padre.

## <a name="result"></a>Risultato

ICE14 invia un messaggio di errore se trova una funzionalità radice con il bit msidbFeatureAttributesFollowParent impostato o una funzionalità con voci identiche nelle colonne Feature e Feature Parent della tabella \_ Feature.

## <a name="example"></a>Esempio

ICE14 restituirà gli errori seguenti per l'esempio seguente:

-   La funzionalità Sport ha lo stesso valore nelle colonne Feature e Feature \_ Parent della tabella File.
-   La funzionalità radice Sport ha il bit msidbFeatureAttributesFollowParent impostato.

Nell'albero delle funzionalità di questo esempio, Sport è la funzionalità radice e un elemento padre delle funzionalità Di nuoto e calcio. Freestyle è una funzionalità figlio di Swimming. TouchFootball è una funzionalità figlio di Football.

[Tabella delle funzionalità](feature-table.md) (parziale)



| Funzionalità       | Attributi | Elemento \_ padre della funzionalità |
|---------------|------------|-----------------|
| Sport         | 4          | Sport           |
| Nuoto      | 1          | Sport           |
| Calcio      | 4          | Sport           |
| Freestyle     | 1          | Nuoto        |
| TouchFootball | 4          | Calcio        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



