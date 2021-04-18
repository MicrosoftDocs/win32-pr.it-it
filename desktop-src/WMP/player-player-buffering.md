---
title: Evento Player. buffering
description: L'evento di buffering si verifica quando il controllo Media Player Windows inizia o termina il buffering o il download. | Evento Player. buffering
ms.assetid: a0a09bf7-19bc-4838-a403-924e8d83b48d
keywords:
- Media Player buffering di Windows Event
- Evento di buffering Media Player di Windows, classe Player
- Classe Player Windows Media Player, evento di buffering
topic_type:
- apiref
api_name:
- Player.Buffering
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a73ac77f9b8e81162a6cc0f9220562caba26eae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327065"
---
# <a name="playerbuffering-event"></a>Evento Player. buffering

L'evento di **buffering** si verifica quando il controllo Media Player Windows inizia o termina il buffering o il download.

## <a name="syntax"></a>Sintassi


```JScript
Player.Buffering(
  Start
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Inizia* 
</dt> <dd>

**Valore booleano** contenente uno dei valori seguenti.



| Valore | Descrizione            |
|-------|------------------------|
| true  | Il buffering è stato avviato. |
| false | Il buffering è terminato.   |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Utilizzare questo evento per determinare quando viene avviata o arrestata la memorizzazione nel buffer o il download. È possibile utilizzare lo stesso blocco di eventi sia per i case che per la *rete* di test. **bufferingProgress** e *rete*. **downloadProgress** per determinare se Windows Media Player sta attualmente memorizzando nel buffer o scaricando il contenuto.

Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Rete. bufferingProgress**](network-bufferingprogress.md)
</dt> <dt>

[**Rete. downloadProgress**](network-downloadprogress.md)
</dt> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





