---
description: La proprietà ProductLanguage deve essere aggiornata all'identificatore della lingua numerica (LANGID) per la nuova lingua.
ms.assetid: e00ef69b-c54b-41de-9230-a7582b260891
title: Aggiornamento delle proprietà ProductLanguage e ProductCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9d6cbb47a16e0e0f2f9d696dc73d3f3fe0d1bc278c4631a99469168e2ca23d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809861"
---
# <a name="updating-productlanguage-and-productcode-properties"></a>Aggiornamento delle proprietà ProductLanguage e ProductCode

La [**proprietà ProductLanguage**](productlanguage.md) deve essere aggiornata all'identificatore della lingua numerica (LANGID) per la nuova lingua. Nel caso dell'esempio di localizzazione, il valore della proprietà **ProductLanguage** deve essere modificato da LANGID per inglese (1033) a LANGID per il francese (1036) nella tabella [Proprietà](property-table.md).

Il valore della [**proprietà ProductCode**](productcode.md) nella tabella [Property](property-table.md) deve essere modificato in un nuovo valore univoco durante la localizzazione di un database perché un prodotto localizzato è considerato un prodotto diverso. Ad esempio, le versioni tedesco e inglese di un'applicazione sono considerate due prodotti diversi e devono avere codici di prodotto diversi. Vedere [Codici prodotto](product-codes.md).

Usare l'editor di tabelle di database per aggiornare i valori delle proprietà ProductCode e ProductLanguage nella tabella Property. Non riutilizzare il GUID visualizzato se si copia questo esempio.

[Tabella delle proprietà](property-table.md)



| Proprietà                                   | Valore                                  |
|--------------------------------------------|----------------------------------------|
| [**ProductCode**](productcode.md)         | {EE389960-E426-4EEA-B669-AD8129249881} |
| [**ProductLanguage**](productlanguage.md) | 1036                                   |



 

[Continua](updating-a-summary-information-stream.md)

 

 



