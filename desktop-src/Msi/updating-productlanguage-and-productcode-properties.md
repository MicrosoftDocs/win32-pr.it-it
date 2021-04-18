---
description: Per la nuova lingua, è necessario aggiornare la proprietà ProductLanguage all'identificatore di lingua numerico (LANGID).
ms.assetid: e00ef69b-c54b-41de-9230-a7582b260891
title: Aggiornamento delle proprietà ProductLanguage e ProductCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a7537cdb0295075fbfd1b8b58e45a051610cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318274"
---
# <a name="updating-productlanguage-and-productcode-properties"></a>Aggiornamento delle proprietà ProductLanguage e ProductCode

Per la nuova lingua, è necessario aggiornare la proprietà [**ProductLanguage**](productlanguage.md) all'identificatore di lingua numerico (LangID). Nel caso dell'esempio di localizzazione, il valore della proprietà **ProductLanguage** deve essere modificato da LangID per la lingua inglese (1033) a LangID per il francese (1036) nella tabella delle [Proprietà](property-table.md).

Il valore della proprietà [**ProductCode**](productcode.md) nella tabella delle [Proprietà](property-table.md) deve essere modificato in un nuovo valore univoco quando si localizza un database perché un prodotto localizzato è considerato un prodotto diverso. Ad esempio, le versioni tedesche e in inglese di un'applicazione sono considerate due prodotti diversi e devono avere codici prodotto diversi. Vedere [codici prodotto](product-codes.md).

Utilizzare l'Editor tabella di database per aggiornare i valori delle proprietà ProductCode e ProductLanguage nella tabella delle proprietà. Non riutilizzare il GUID visualizzato se si copia questo esempio.

[Tabella delle proprietà](property-table.md)



| Proprietà                                   | Valore                                  |
|--------------------------------------------|----------------------------------------|
| [**ProductCode**](productcode.md)         | {EE389960-E426-4EEA-B669-AD8129249881} |
| [**ProductLanguage**](productlanguage.md) | 1036                                   |



 

[Continua](updating-a-summary-information-stream.md)

 

 



