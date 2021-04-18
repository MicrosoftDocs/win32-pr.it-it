---
title: Evento DomainChange dell'oggetto AxWindowsMediaPlayer
description: L'evento DomainChange si verifica quando viene modificato il dominio DVD. | Evento DomainChange dell'oggetto AxWindowsMediaPlayer
ms.assetid: a080082e-1ba4-4080-b39c-b84292ecacb0
keywords:
- Evento DomainChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
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
ms.openlocfilehash: 342ac559f75c3bb7d65b442bfbdced5e5ed3f690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331400"
---
# <a name="domainchange-event-of-the-axwindowsmediaplayer-object"></a>Evento DomainChange dell'oggetto AxWindowsMediaPlayer

L'evento DomainChange si verifica quando viene modificato il dominio DVD.

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

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_DomainChangeEventHandler WMPOCXEvents**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ DomainChangeEvent**, che contiene la proprietà seguente correlata a questo evento.



| Proprietà  | Descrizione                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| strDomain | System. StringIndicates il nuovo dominio. Per i valori possibili, vedere la sezione Osservazioni.<br/> |



 

## <a name="remarks"></a>Commenti

Nella tabella seguente vengono illustrati i valori possibili per la proprietà strDomain.



| string            | Descrizione                                                          |
|-------------------|----------------------------------------------------------------------|
| firstPlay         | Esecuzione dell'inizializzazione predefinita di un disco DVD.                     |
| videoManagerMenu  | Visualizzazione dei menu per l'intero disco. Noto anche come menu radice o menu di scelta rapida. |
| videoTitleSetMenu | Visualizzazione dei menu per il set di titoli corrente. Noto anche come titleMenu.     |
| title             | Visualizzazione del titolo corrente.                                        |
| stop              | Il navigatore DVD si trova nel dominio di arresto DVD.                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPDVD (VB e C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





