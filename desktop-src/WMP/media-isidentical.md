---
title: Metodo media. IsValid
description: Il metodo IsValid recupera un valore che indica se l'oggetto fornito è uguale a quello corrente. | Metodo media. IsValid
ms.assetid: af3266d5-4ac2-4e8c-a9f6-44f7938e9c9d
keywords:
- Metodo di Media Player di Windows identico
- Metodo di Windows Media Player, classe multimediale
- Media class Media Player Windows, metodo identico
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
ms.openlocfilehash: 196487889c075938e763c2b2305b614cffb5f09f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329308"
---
# <a name="mediaisidentical-method"></a>Metodo media. IsValid

Il **Metodo IsValid** recupera un valore che indica se l'oggetto fornito è uguale a quello corrente.

## <a name="syntax"></a>Sintassi


```JScript
bRetVal = Media.isIdentical(
  media
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*supporto* \[ di in\]
</dt> <dd>

Oggetto **multimediale** da confrontare con l'oggetto **multimediale** corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore booleano**.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene usato il *supporto*. è **identico** per verificare se un elemento multimediale denominato newMedia è uguale all'elemento multimediale corrente. Se non sono uguali, viene riprodotto il nuovo elemento multimediale. In caso contrario, i supporti correnti continueranno a essere riprodotti senza interruzioni. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> </dl>

 

 





