---
title: Metodo Media.isIdentical
description: Il metodo isIdentical recupera un valore che indica se l'oggetto fornito è uguale a quello corrente. | Metodo Media.isIdentical
ms.assetid: af3266d5-4ac2-4e8c-a9f6-44f7938e9c9d
keywords:
- Metodo isIdentical Windows Media Player
- Metodo isIdentical Windows Media Player , classe Media
- Classe media Windows Media Player metodo isIdentical
topic_type:
- apiref
api_name:
- Media.isIdentical
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5147d6ccc72d570709ef6ad898bf52872909dc5e3800d9cc671c774510b45d1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054639"
---
# <a name="mediaisidentical-method"></a>Metodo Media.isIdentical

Il **metodo isIdentical** recupera un valore che indica se l'oggetto fornito è uguale a quello corrente.

## <a name="syntax"></a>Sintassi


```JScript
bRetVal = Media.isIdentical(
  media
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*supporti* \[ Pollici\]
</dt> <dd>

**Oggetto** multimediale da confrontare con l'oggetto **Media** corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un valore **booleano**.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzato *Media*. **isIdentical per** controllare se un elemento multimediale denominato newMedia corrisponde all'elemento multimediale corrente. Se non sono uguali, viene riprodotto il nuovo elemento multimediale. In caso contrario, il supporto corrente continua a essere riprodotto senza interruzioni. **L'oggetto** Player è stato creato con ID = "Player".


```JScript
// Check the new media item to see if it matches the current one.
if (newMedia.isIdentical(Player.currentMedia) != true){

   // Change the current media to the new media item.
   Player.currentMedia = newMedia;

   // Play the new media item.
   Player.controls.play();
}

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> </dl>

 

 





