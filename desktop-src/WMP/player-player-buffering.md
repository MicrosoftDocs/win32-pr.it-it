---
title: Evento Player.Buffering
description: L'evento Buffering si verifica quando il controllo Windows Media Player inizia o termina il buffering o il download. | Evento Player.Buffering
ms.assetid: a0a09bf7-19bc-4838-a403-924e8d83b48d
keywords:
- Memorizzazione nel buffer dei dati Windows Media Player
- Buffering event Windows Media Player , Player class
- Classe player Windows Media Player , evento buffering
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
ms.openlocfilehash: d0ac382315d37fcd36a5470ae3f7f07bf4454687b660a2311498b5b0866e32b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747522"
---
# <a name="playerbuffering-event"></a>Evento Player.Buffering

**L'evento Buffering** si verifica quando il controllo Windows Media Player inizia o termina il buffering o il download.

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

**Valore** booleano contenente uno dei valori seguenti.



| Valore | Descrizione            |
|-------|------------------------|
| true  | La memorizzazione nel buffer è stata avviata. |
| false | La memorizzazione nel buffer è terminata.   |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare questo evento per determinare quando il buffering o il download viene avviato o arrestato. È possibile usare lo stesso blocco di eventi sia per i case che per i test *di Rete*. **bufferingProgress** e *Rete*. **downloadProgress** per determinare se Windows Media Player sta attualmente memorizzata nel buffer o scaricando il contenuto.

Il valore dei parametri dell'evento viene specificato da Windows Media Player ed è accessibile o passato a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, inclusa l'maiuscola.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Network.bufferingProgress**](network-bufferingprogress.md)
</dt> <dt>

[**Network.downloadProgress**](network-downloadprogress.md)
</dt> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





