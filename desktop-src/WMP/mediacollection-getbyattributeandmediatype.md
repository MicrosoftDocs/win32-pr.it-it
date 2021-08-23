---
title: Metodo MediaCollection.getByAttributeAndMediaType
description: Il metodo getByAttributeAndMediaType recupera un oggetto Playlist contenente oggetti Media con l'attributo e il tipo di supporto specificati.
ms.assetid: 75241b38-ae0e-4216-b405-af9a9c71f5ec
keywords:
- Metodo getByAttributeAndMediaType Windows Media Player
- Metodo getByAttributeAndMediaType Windows Media Player , classe MediaCollection
- Classe MediaCollection Windows Media Player metodo , getByAttributeAndMediaType
topic_type:
- apiref
api_name:
- MediaCollection.getByAttributeAndMediaType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46dab1bdcb511e4c96374b17bc6a98be95e48fd64d005eb856c9ec247af48f2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647881"
---
# <a name="mediacollectiongetbyattributeandmediatype-method"></a>Metodo MediaCollection.getByAttributeAndMediaType

Il **metodo getByAttributeAndMediaType** recupera un oggetto **Playlist** contenente oggetti **Media** con l'attributo e il tipo di supporto specificati.

## <a name="syntax"></a>Sintassi


```JScript
retVal = MediaCollection.getByAttributeAndMediaType(
  attribute,
  value,
  mediaType
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*attributo* \[ Pollici\]
</dt> <dd>

**Stringa contenente** l'attributo.

</dd> <dt>

*value* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il valore.

</dd> <dt>

*mediaType* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il tipo di supporto. Deve contenere uno dei valori seguenti: "audio", "video", "photo", "playlist" o "other".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un oggetto **Playlist**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento su attributi**](attribute-reference.md)
</dt> <dt>

[**Oggetto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Oggetto Playlist**](playlist-object.md)
</dt> </dl>

 

 





