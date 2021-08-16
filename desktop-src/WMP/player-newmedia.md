---
title: Metodo Player.newMedia
description: Il metodo newMedia crea un nuovo oggetto Media.
ms.assetid: fccf1559-bac3-4edf-bd88-da2c72cdec21
keywords:
- Metodo newMedia Windows Media Player
- Metodo newMedia Windows Media Player , classe Player
- Classe Player Windows Media Player , metodo newMedia
topic_type:
- apiref
api_name:
- Player.newMedia
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6e3ad30db7ec43bcc0ee6c1470dc608ccf1625390486d9fcd0fd4bf018affdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338106"
---
# <a name="playernewmedia-method"></a>Metodo Player.newMedia

Il **metodo newMedia** crea un nuovo **oggetto Media.**

## <a name="syntax"></a>Sintassi


```JScript
retVal = Player.newMedia(
  URL
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*URL* \[ Pollici\]
</dt> <dd>

**Stringa** contenente l'URL del file multimediale digitale con cui creare **l'oggetto** Media.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto Media.**

## <a name="remarks"></a>Commenti

Il *parametro URL* non deve essere una stringa vuota o null.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





