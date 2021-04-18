---
title: PLAYLIST. setColumnResizeMode
description: Il metodo setColumnResizeMode specifica il modo in cui la colonna indicizzata si ridimensiona.
ms.assetid: 84ca0e60-ca24-4058-ae08-5b9cf3d7c38f
keywords:
- PLAYLIST. setColumnResizeMode Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setColumnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a1b83020f4400f4f1095c84e281fe498f2b67da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333841"
---
# <a name="playlistsetcolumnresizemode"></a>PLAYLIST. setColumnResizeMode

Il metodo **setColumnResizeMode** specifica il modo in cui la colonna indicizzata si ridimensiona.

``` syntax
        elementID.setColumnResizeMode(column, mode)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="column"></span><span id="COLUMN"></span>*colonna*
</dt> <dd>

**Numero** (**Long**) che indica l'indice della colonna da modificare.

</dd> <dt>

<span id="mode"></span><span id="MODE"></span>*modalità*
</dt> <dd>

**Stringa** che indica la modalità di ridimensionamento. Contiene uno dei valori seguenti.



| Valore          | Descrizione                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| AutosizeHeader | La colonna viene ridimensionata per contenere tutti i dati nella colonna e nell'intestazione.                                  |
| AutosizeData   | La colonna viene ridimensionata in modo da contenere solo tutti i dati della colonna.                                                 |
| Fisso          | La colonna è a dimensione fissa.                                                                                    |
| Occupa completamente      | La colonna viene ridimensionata in modo da utilizzare lo spazio rimanente nell'elemento della **playlist** dopo che tutte le altre colonne vengono ridimensionate. |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PLAYLIST (elemento)**](playlist-element.md)
</dt> </dl>

 

 





