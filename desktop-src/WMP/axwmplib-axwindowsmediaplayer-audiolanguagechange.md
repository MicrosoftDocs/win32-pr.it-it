---
title: Evento AudioLanguageChange dell'oggetto AxWindowsMediaPlayer
description: L'evento AudioLanguageChange si verifica quando cambia la lingua audio corrente. | Evento AudioLanguageChange dell'oggetto AxWindowsMediaPlayer
ms.assetid: 35e4ff82-fc59-4d28-b7fc-1527fb46b960
keywords:
- Evento AudioLanguageChange dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- AudioLanguageChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40538dad18c4cb6767a034ab5d163f16d1822d9149e15c07ca1130f5eb17f30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582726"
---
# <a name="audiolanguagechange-event-of-the-axwindowsmediaplayer-object"></a>Evento AudioLanguageChange dell'oggetto AxWindowsMediaPlayer

L'evento AudioLanguageChange si verifica quando cambia la lingua audio corrente.

``` syntax
[C#]
private void player_AudioLanguageChange(
  object sender,
  _WMPOCXEvents_AudioLanguageChangeEvent e
)

[Visual Basic]
Private Sub player_AudioLanguageChange(
  sender As Object,
  e As _WMPOCXEvents_AudioLanguageChangeEvent
) Handles player.AudioLanguageChange
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ WMPOCXEvents \_ AudioLanguageChangeEventHandler**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ AudioLanguageChangeEvent**, che contiene la proprietà seguente correlata a questo evento.



| Proprietà   | Descrizione                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| **langID** | **System.Int32** Identifica in modo univoco un particolare dialetto linguistico, denominato impostazioni locali.<br/> |



 

## <a name="remarks"></a>Commenti

Un identificatore delle impostazioni locali (LCID) identifica in modo univoco un particolare dialetto di lingua, denominato impostazioni locali.

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

[**IWMPControls3.currentAudioLanguage (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> </dl>

 

 





