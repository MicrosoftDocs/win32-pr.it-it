---
title: Evento Player.CdromMediaChange
description: L'evento CdromMediaChange si verifica quando un CD o DVD viene inserito o espulso da un'unità CD o DVD. | Evento Player.CdromMediaChange
ms.assetid: d31a791a-55e5-49ee-bfe5-7488277e3fda
keywords:
- Evento CdromMediaChange Windows Media Player
- Evento CdromMediaChange Windows Media Player , classe Player
- Classe Player Windows Media Player , evento CdromMediaChange
topic_type:
- apiref
api_name:
- Player.CdromMediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca5e7301c1fb697f4dbbceea2d4dc46af1d884fe4b3e06166b5c24aa43502a73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747387"
---
# <a name="playercdrommediachange-event"></a>Evento Player.CdromMediaChange

**L'evento CdromMediaChange** si verifica quando un CD o DVD viene inserito o espulso da un'unità CD o DVD.

## <a name="syntax"></a>Sintassi


```JScript
Player.CdromMediaChange(
  CdromNum
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CdromNum* 
</dt> <dd>

**Numero** (**long**) che specifica l'indice dell'unità CD o DVD.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

L'indice dell'unità CD corrisponde all'indice di **un oggetto Cdrom** in **CdromCollection**.

Il valore dei parametri dell'evento viene specificato da Windows Media Player ed è accessibile o passato a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, inclusa l'maiuscola.

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Cdrom**](cdrom-object.md)
</dt> <dt>

[**Oggetto CdromCollection**](cdromcollection-object.md)
</dt> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





