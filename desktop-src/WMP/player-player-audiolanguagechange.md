---
title: Evento Player. AudioLanguageChange
description: L'evento AudioLanguageChange si verifica quando cambia la lingua audio corrente. | Evento Player. AudioLanguageChange
ms.assetid: 29006a51-1b72-4fab-9906-8a0af3d92560
keywords:
- Media Player di Windows Event AudioLanguageChange
- Windows Event AudioLanguageChange Media Player, classe Player
- Classe Player Windows Media Player, evento AudioLanguageChange
topic_type:
- apiref
api_name:
- Player.AudioLanguageChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84809a966280c379f7051e500b4e385d640f890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327068"
---
# <a name="playeraudiolanguagechange-event"></a>Evento Player. AudioLanguageChange

L'evento **AudioLanguageChange** si verifica quando cambia la lingua audio corrente.

## <a name="syntax"></a>Sintassi


```JScript
Player.AudioLanguageChange(
  LangID
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LangID* 
</dt> <dd>

**Numero** (**Long**) che specifica il nuovo identificatore delle impostazioni locali (LCID).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Un LCID identifica in modo univoco un dialetto di lingua particolare, denominato impostazioni locali.

Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file Microsoft JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Controls. currentAudioLanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





