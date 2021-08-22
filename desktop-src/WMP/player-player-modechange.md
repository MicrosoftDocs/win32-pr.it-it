---
title: Evento Player.ModeChange
description: L'evento ModeChange si verifica quando viene modificata Windows Media Player modalità di modifica. | Evento Player.ModeChange
ms.assetid: 45b57660-b186-4c0f-8735-61134058b8c9
keywords:
- Eventi ModeChange Windows Media Player
- ModeChange event Windows Media Player , Player class
- Classe player Windows Media Player, evento ModeChange
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
ms.openlocfilehash: e4a1102d49064c602d04915f77eda7ecfa1c748d4aea000cef1271679da1ec62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054359"
---
# <a name="playermodechange-event"></a>Evento Player.ModeChange

**L'evento ModeChange** si verifica quando viene modificata Windows Media Player modalità di modifica.

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

**Stringa** che indica la modalità modificata. Contiene uno dei valori seguenti.



| Valore   | Descrizione                                         |
|---------|-----------------------------------------------------|
| shuffle | Le tracce vengono riprodotte in ordine casuale.                  |
| loop    | L'intera sequenza di tracce viene riprodotta ripetutamente. |



 

</dd> <dt>

*Newvalue* 
</dt> <dd>

**Valore** booleano che indica il nuovo stato della modalità specificata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il valore dei parametri dell'evento viene specificato da Windows Media Player ed è accessibile o passato a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, inclusa l'maiuscola.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Impostazioni.getMode**](settings-getmode.md)
</dt> <dt>

[**Impostazioni.setMode**](settings-setmode.md)
</dt> </dl>

 

 





