---
description: ICE14 convalida la tabella delle funzionalità di un database Windows Installer.
ms.assetid: fb1970f8-1dba-4b06-aa03-5b33d213fc79
title: ICE14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2e64a6106ae359fe02c6ead271bbae267eeb18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346326"
---
# <a name="ice14"></a>ICE14

ICE14 convalida quanto segue per le funzionalità:

-   Per le funzionalità padre radice non è impostato il bit msidbFeatureAttributesFollowParent nella colonna Attributes della [tabella Feature](feature-table.md). Una funzionalità radice non ha un elemento padre.
-   Nessuna caratteristica ha la stessa voce nelle colonne padre feature e feature \_ della [tabella Feature](feature-table.md). Nessuna funzionalità può essere il proprio padre.

## <a name="result"></a>Risultato

ICE14 Invia un messaggio di errore se trova una funzionalità radice con il set di bit msidbFeatureAttributesFollowParent o una funzionalità con voci identiche nelle colonne padre feature e feature \_ della tabella Feature.

## <a name="example"></a>Esempio

ICE14 restituirebbe gli errori seguenti per l'esempio seguente:

-   La funzionalità Sport presenta lo stesso valore nelle colonne padre feature e feature \_ della tabella file.
-   Per la funzionalità radice sport è impostato il bit msidbFeatureAttributesFollowParent.

Nell'albero delle funzionalità di questo esempio, sport è la funzionalità radice e un elemento padre delle funzionalità di nuoto e football. Freestyle è una funzionalità figlio di swimming. TouchFootball è una funzionalità figlio di football.

[Tabella delle funzionalità](feature-table.md) (parziale)



| Funzionalità       | Attributi | \_Elemento padre della funzionalità |
|---------------|------------|-----------------|
| Sport         | 4          | Sport           |
| Swimming      | 1          | Sport           |
| Calcio      | 4          | Sport           |
| Freestyle     | 1          | Swimming        |
| TouchFootball | 4          | Calcio        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



