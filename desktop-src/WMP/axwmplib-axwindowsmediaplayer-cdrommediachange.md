---
title: Evento CdromMediaChange dell'oggetto AxWindowsMediaPlayer
description: L'evento CdromMediaChange si verifica quando un CD o DVD viene inserito o espulso da un'unità CD o DVD. | Evento CdromMediaChange dell'oggetto AxWindowsMediaPlayer
ms.assetid: 0a6378c1-59e4-4be3-8764-d5c4ab478b6c
keywords:
- Evento CdromMediaChange dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- CdromMediaChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55dac05b3ca8a8675bfae431d3f2e8ffbb38db8701a2501fa80d282cd3c976ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055006"
---
# <a name="cdrommediachange-event-of-the-axwindowsmediaplayer-object"></a>Evento CdromMediaChange dell'oggetto AxWindowsMediaPlayer

**L'evento CdromMediaChange** si verifica quando un CD o DVD viene inserito o espulso da un'unità CD o DVD.

``` syntax
[C#]
private void player_CdromMediaChange(
  object sender,
  _WMPOCXEvents_CdromMediaChangeEvent e
)

[Visual Basic]
Private Sub player_CdromMediaChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromMediaChangeEvent
) Handles player.CdromMediaChange
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromMediaChangeEventHandler**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromMediaChangeEvent**, che contiene la proprietà seguente correlata a questo evento.



| Proprietà | Descrizione                                                        |
|----------|--------------------------------------------------------------------|
| CdromNum | System.Int32Specifica l'indice dell'unità CD o DVD.<br/> |



 

## <a name="remarks"></a>Commenti

L'indice dell'unità CD corrisponde all'indice di un'interfaccia IWMPCdrom accessibile tramite l'interfaccia IWMPCdromCollection.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPCdrom (VB e C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPCdromCollection (VB e C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> </dl>

 

 





