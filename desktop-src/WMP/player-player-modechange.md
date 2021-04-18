---
title: Evento Player. ModeChange
description: L'evento ModeChange si verifica quando viene modificata una modalità di Windows Media Player. | Evento Player. ModeChange
ms.assetid: 45b57660-b186-4c0f-8735-61134058b8c9
keywords:
- Media Player di Windows Event ModeChange
- Windows Event ModeChange Media Player, classe Player
- Classe Player Windows Media Player, evento ModeChange
topic_type:
- apiref
api_name:
- Player.ModeChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb202672c7fce6705b8e86889c0ca44d7004a19e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325833"
---
# <a name="playermodechange-event"></a>Evento Player. ModeChange

L'evento **ModeChange** si verifica quando viene modificata una modalità di Windows Media Player.

## <a name="syntax"></a>Sintassi


```JScript
Player.ModeChange(
  ModeName,
  NewValue
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ModeName* 
</dt> <dd>

**Stringa** che indica la modalità che è stata modificata. Contiene uno dei valori seguenti.



| Valore   | Descrizione                                         |
|---------|-----------------------------------------------------|
| shuffle | Le tracce vengono riprodotte in ordine casuale.                  |
| loop    | L'intera sequenza di tracce viene riprodotta ripetutamente. |



 

</dd> <dt>

*NewValue* 
</dt> <dd>

**Valore booleano** che indica il nuovo stato della modalità specificata.

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
</dt> <dt>

[**Settings. getMode**](settings-getmode.md)
</dt> <dt>

[**Settings. semode**](settings-setmode.md)
</dt> </dl>

 

 





