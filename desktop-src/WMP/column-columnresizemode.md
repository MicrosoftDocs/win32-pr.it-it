---
title: COLUMN. columnResizeMode
description: L'attributo columnResizeMode specifica o recupera la modalità di ridimensionamento per la colonna.
ms.assetid: 95ece2a3-20a6-4b9d-a2eb-fc69fc612f29
keywords:
- Media Player di Windows COLUMN. columnResizeMode
topic_type:
- apiref
api_name:
- COLUMN.columnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d17b1a2edd878fb15e69c595e3c061c1963a5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327782"
---
# <a name="columncolumnresizemode"></a>COLUMN. columnResizeMode

L'attributo **columnResizeMode** specifica o recupera la modalità di ridimensionamento per la colonna.

``` syntax
        elementID.columnResizeMode
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente uno dei valori seguenti.



| Valore          | Descrizione                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| AutosizeHeader | Valore predefinito. La colonna viene ridimensionata per contenere tutti i dati nella colonna e nell'intestazione.                         |
| AutosizeData   | La colonna viene ridimensionata in modo da contenere solo tutti i dati della colonna.                                                 |
| Fisso          | La colonna è a dimensione fissa.                                                                                    |
| Occupa completamente      | La colonna viene ridimensionata in modo da utilizzare lo spazio rimanente del controllo **playlist** dopo che tutte le altre colonne vengono ridimensionate. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**COLUMN-elemento**](column-element.md)
</dt> </dl>

 

 





