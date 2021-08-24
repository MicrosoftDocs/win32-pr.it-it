---
title: COLUMN.columnResizeMode
description: L'attributo columnResizeMode specifica o recupera la modalità di ridimensionamento per questa colonna.
ms.assetid: 95ece2a3-20a6-4b9d-a2eb-fc69fc612f29
keywords:
- COLUMN.columnResizeMode Windows Media Player
topic_type:
- apiref
api_name:
- COLUMN.columnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c59046aa76c01a1439e5db8f0fb6850e7df74d874cba555d1f9c3829f09d9598
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764001"
---
# <a name="columncolumnresizemode"></a>COLUMN.columnResizeMode

**L'attributo columnResizeMode** specifica o recupera la modalità di ridimensionamento per questa colonna.

``` syntax
        elementID.columnResizeMode
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura** contenente uno dei valori seguenti.



| Valore          | Descrizione                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| AutosizeHeader | Valore predefinito. La colonna viene ridimensionata per contenere tutti i dati sia nella colonna che nell'intestazione.                         |
| AutosizeData   | La colonna viene ridimensionata in modo da contenere solo tutti i dati nella colonna.                                                 |
| Fisso          | Le dimensioni della colonna sono fisse.                                                                                    |
| Si estende      | La colonna viene ridimensionata in modo da usare lo spazio rimanente nel **controllo PLAYLIST** dopo il ridimensionamento di tutte le altre colonne. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento COLUMN**](column-element.md)
</dt> </dl>

 

 





