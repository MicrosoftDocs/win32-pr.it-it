---
title: Evento DomainChange dell'oggetto AxWindowsMediaPlayer
description: L'evento DomainChange si verifica quando il dominio DVD viene modificato. | Evento DomainChange dell'oggetto AxWindowsMediaPlayer
ms.assetid: a080082e-1ba4-4080-b39c-b84292ecacb0
keywords:
- Evento DomainChange dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- DomainChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37f10679225fb893fad8bcf6fc6687021256e305e8c5a08e6ebe96d16b74e81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136124"
---
# <a name="domainchange-event-of-the-axwindowsmediaplayer-object"></a>Evento DomainChange dell'oggetto AxWindowsMediaPlayer

L'evento DomainChange si verifica quando il dominio DVD viene modificato.

``` syntax
[C#]
private void player_DomainChange(
  object sender,
  _WMPOCXEvents_DomainChangeEvent e
)

[Visual Basic]
Private Sub player_DomainChange(  
  sender As Object,
  e As _WMPOCXEvents_DomainChangeEvent
) Handles player.DomainChange
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ WMPOCXEvents \_ DomainChangeEventHandler**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ DomainChangeEvent**, che contiene la proprietà seguente correlata a questo evento.



| Proprietà  | Descrizione                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| strDomain | System.StringIndicates il nuovo dominio. Per i valori possibili, vedere la sezione Osservazioni.<br/> |



 

## <a name="remarks"></a>Commenti

La tabella seguente illustra i valori possibili per la proprietà strDomain.



| string            | Descrizione                                                          |
|-------------------|----------------------------------------------------------------------|
| firstPlay         | Esecuzione dell'inizializzazione predefinita di un disco DVD.                     |
| videoManagerMenu  | Visualizzazione dei menu per l'intero disco. Noto anche come Menu radice o TopMenu. |
| videoTitleSetMenu | Visualizzazione dei menu per il set di titoli corrente. Noto anche come titleMenu.     |
| title             | Visualizzazione del titolo corrente.                                        |
| stop              | Il DVD Navigator si trova nel dominio DVD Stop.                         |



 

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

[**Interfaccia IWMPDVD (VB e C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





