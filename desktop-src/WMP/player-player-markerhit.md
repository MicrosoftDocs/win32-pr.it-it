---
title: Evento Player. MarkerHit
description: L'evento MarkerHit si verifica quando viene raggiunto un marcatore. | Evento Player. MarkerHit
ms.assetid: c97aff61-6f06-4589-a75b-ac2af340cb1d
keywords:
- Media Player di Windows Event MarkerHit
- Windows Event MarkerHit Media Player, classe Player
- Classe Player Windows Media Player, evento MarkerHit
topic_type:
- apiref
api_name:
- Player.MarkerHit
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cce6b9ca7c103e9a9e9151a7ff0467a59786b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326309"
---
# <a name="playermarkerhit-event"></a>Evento Player. MarkerHit

L'evento **MarkerHit** si verifica quando viene raggiunto un marcatore.

## <a name="syntax"></a>Sintassi


```JScript
Player.MarkerHit(
  MarkerNum
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*MarkerNum* 
</dt> <dd>

**Numero** (**Long**) che indica il numero del marcatore raggiunto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





