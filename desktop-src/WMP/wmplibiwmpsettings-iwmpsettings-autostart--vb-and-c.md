---
title: Proprietà autoStart di IWMPSettings
description: La proprietà autoStart ottiene o imposta un valore che indica se la riproduzione dell'elemento multimediale corrente inizia automaticamente.
ms.assetid: 01a1cb78-9951-478a-8ea3-1ae06164beab
keywords:
- proprietà autoStart Windows Media Player
- proprietà autoStart Windows Media Player, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player proprietà , autoStart
topic_type:
- apiref
api_name:
- IWMPSettings.autoStart
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7be64a030bbfe8abbd81830a7638094cd3da93939f3184ad3a4cfca0063c9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568468"
---
# <a name="iwmpsettingsautostart-property"></a>Proprietà IWMPSettings::autoStart

La **proprietà autoStart** ottiene o imposta un valore che indica se la riproduzione dell'elemento multimediale corrente inizia automaticamente.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Boolean autoStart {get; set;}
```


```VB

Public Property autoStart As System.Boolean
```





## <a name="property-value"></a>Valore proprietà

Valore **System.Boolean che** indica se la riproduzione dell'elemento multimediale corrente inizia automaticamente. Il valore predefinito è **True**.

## <a name="remarks"></a>Commenti

Se **autoStart** è impostato su **true,** la riproduzione dell'elemento multimediale inizierà quando **axWindowsMediaPlayer.URL,** **AxWindowsMediaPlayer.currentPlaylist** o **AxWindowsMediaPlayer.currentMedia** è impostato. In caso contrario, la riproduzione dell'elemento multimediale non verrà avviata fino a quando non viene chiamato il metodo **IWMPControls.play.**

A meno che non si imposta **autoStart** su **true** immediatamente prima di specificare un elemento multimediale, non è consigliabile usare questa impostazione come alternativa all'uso del metodo **IWMPControls.play.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AxWindowsMediaPlayer.currentMedia (VB e C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.currentPlaylist (VB e C#)**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.URL (VB e C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPControls.play (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





