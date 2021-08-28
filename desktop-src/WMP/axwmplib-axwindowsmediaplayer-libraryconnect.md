---
title: Evento LibraryConnect dell'oggetto AxWindowsMediaPlayer
description: L'evento LibraryConnect si verifica quando una libreria diventa disponibile.
ms.assetid: f67243ce-0e25-43a7-b754-6b0e80d72055
keywords:
- Evento LibraryConnect dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- LibraryConnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940eed16004009e928309ae1a2e5d8f792b9fd0cb36fe8e836abfefb89e3ab95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123951"
---
# <a name="libraryconnect-event-of-the-axwindowsmediaplayer-object"></a>Evento LibraryConnect dell'oggetto AxWindowsMediaPlayer

L'evento LibraryConnect si verifica quando una libreria diventa disponibile.

``` syntax
[C#]
private void player_LibraryConnect(
  object sender,
  _WMPOCXEvents_LibraryConnectEvent e
)

[Visual Basic]
Private Sub player_LibraryConnect(  
  sender As Object,
  e As _WMPOCXEvents_LibraryConnectEvent
) Handles player.LibraryConnect
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ Libreria WMPOCXEventsConnectEventHandler \_**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ LibraryConnectEvent**, che contiene la proprietà seguente correlata a questo evento.



| Proprietà | Descrizione                                                                                |
|----------|--------------------------------------------------------------------------------------------|
| pLibrary | **WMPLib.IWMPLibrary** Interfaccia che rappresenta la libreria connessa.<br/> |



 

## <a name="remarks"></a>Commenti

Questo evento non si verifica per la libreria locale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11<br/>                                                                                         |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPLibrary (VB e C#)**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





