---
title: PLAYLIST.setColumnResizeMode
description: Il metodo setColumnResizeMode specifica le dimensioni della colonna indicizzata stessa.
ms.assetid: 84ca0e60-ca24-4058-ae08-5b9cf3d7c38f
keywords:
- PLAYLIST.setColumnResizeMode Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setColumnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72f356108ff016c404468a9b152b4adac247cd72ee089a9e82ea3206c4c2ffea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335803"
---
# <a name="playlistsetcolumnresizemode"></a>PLAYLIST.setColumnResizeMode

Il **metodo setColumnResizeMode** specifica le dimensioni della colonna indicizzata stessa.

``` syntax
        elementID.setColumnResizeMode(column, mode)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="column"></span><span id="COLUMN"></span>*Colonna*
</dt> <dd>

**Numero** (**long**) che indica l'indice della colonna da modificare.

</dd> <dt>

<span id="mode"></span><span id="MODE"></span>*Modalità*
</dt> <dd>

**Stringa** che indica la modalità di ridimensionamento. Contiene uno dei valori seguenti.



| Valore          | Descrizione                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| AutosizeHeader | La colonna viene ridimensionata per contenere tutti i dati sia nella colonna che nell'intestazione.                                  |
| AutosizeData   | La colonna viene ridimensionata in modo da contenere solo tutti i dati nella colonna.                                                 |
| Fisso          | Le dimensioni della colonna sono fisse.                                                                                    |
| Si estende      | La colonna viene ridimensionata in modo da usare lo spazio rimanente nell'elemento **PLAYLIST** dopo il ridimensionamento di tutte le altre colonne. |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





