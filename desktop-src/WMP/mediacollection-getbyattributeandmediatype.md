---
title: Mediacollection. getByAttributeAndMediaType, metodo
description: Il metodo getByAttributeAndMediaType recupera un oggetto playlist contenente gli oggetti multimediali con l'attributo e il tipo di supporto specificati.
ms.assetid: 75241b38-ae0e-4216-b405-af9a9c71f5ec
keywords:
- Metodo getByAttributeAndMediaType Windows Media Player
- Metodo getByAttributeAndMediaType Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo getByAttributeAndMediaType
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
ms.openlocfilehash: 7e26abbf2f19d50ec6a10ebbafe12afae8576f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330347"
---
# <a name="mediacollectiongetbyattributeandmediatype-method"></a>Mediacollection. getByAttributeAndMediaType, metodo

Il metodo **getByAttributeAndMediaType** recupera un oggetto **playlist** contenente gli oggetti **multimediali** con l'attributo e il tipo di supporto specificati.

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

*attributo* \[ in\]
</dt> <dd>

**Stringa** contenente l'attributo.

</dd> <dt>

*valore* \[ di in\]
</dt> <dd>

**Stringa** che contiene il valore.

</dd> <dt>

*mediaType* \[ in\]
</dt> <dd>

**Stringa** che contiene il tipo di supporto. Deve contenere uno dei valori seguenti: "audio", "video", "Photo", "playlist" o "other".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un oggetto **playlist**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> <dt>

[**Mediacollection (oggetto)**](mediacollection-object.md)
</dt> <dt>

[**Oggetto playlist**](playlist-object.md)
</dt> </dl>

 

 





