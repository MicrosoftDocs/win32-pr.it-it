---
title: Evento Player. CdromMediaChange
description: L'evento CdromMediaChange si verifica quando si inserisce o si espelle un CD o un DVD da un'unità CD o DVD. | Evento Player. CdromMediaChange
ms.assetid: d31a791a-55e5-49ee-bfe5-7488277e3fda
keywords:
- Media Player di Windows Event CdromMediaChange
- Windows Event CdromMediaChange Media Player, classe Player
- Classe Player Windows Media Player, evento CdromMediaChange
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
ms.openlocfilehash: 3c3125235d5f8d19963b85284e7dbe40c7af408d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327064"
---
# <a name="playercdrommediachange-event"></a>Evento Player. CdromMediaChange

L'evento **CdromMediaChange** si verifica quando si inserisce o si espelle un CD o un DVD da un'unità CD o DVD.

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

**Numero** (**Long**) che specifica l'indice dell'unità CD o DVD.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

L'indice dell'unità CD corrisponde all'indice di un oggetto **CDROM** in **cdromcollection**.

Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto cdrom**](cdrom-object.md)
</dt> <dt>

[**Oggetto cdromcollection**](cdromcollection-object.md)
</dt> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





