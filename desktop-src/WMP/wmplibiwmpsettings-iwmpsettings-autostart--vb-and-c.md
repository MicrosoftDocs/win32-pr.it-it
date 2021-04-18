---
title: Proprietà di avvio automatico IWMPSettings
description: La proprietà AutoStart Ottiene o imposta un valore che indica se l'elemento multimediale corrente inizia la riproduzione automatica.
ms.assetid: 01a1cb78-9951-478a-8ea3-1ae06164beab
keywords:
- Finestra delle proprietà di avvio automatico Media Player
- Proprietà di avvio automatico Media Player Windows, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player, proprietà AutoStart
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
ms.openlocfilehash: aaf6c1fb43107df11462737286e26fa7801360d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330448"
---
# <a name="iwmpsettingsautostart-property"></a>Proprietà IWMPSettings:: autostart

La proprietà **autostart** Ottiene o imposta un valore che indica se l'elemento multimediale corrente inizia la riproduzione automatica.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Boolean autoStart {get; set;}
```


```VB

Public Property autoStart As System.Boolean
```





## <a name="property-value"></a>Valore proprietà

Valore **System. Boolean** che indica se l'elemento multimediale corrente inizia la riproduzione automatica. Il valore predefinito è **True**.

## <a name="remarks"></a>Commenti

Se **autostart** è impostato su **true**, l'elemento multimediale inizierà a riprodurre quando viene impostato **AxWindowsMediaPlayer. URL**, **AxWindowsMediaPlayer. currentPlaylist** o **AxWindowsMediaPlayer. currentMedia** . In caso contrario, l'elemento multimediale non inizierà a riprodurre fino a quando non viene chiamato il metodo **IWMPControls. Play** .

Se non si imposta **avvio automatico** su **true** immediatamente prima di specificare un elemento multimediale, è consigliabile non fare affidamento su questa impostazione come sostituto per l'utilizzo del metodo **IWMPControls. Play** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AxWindowsMediaPlayer. currentMedia (VB e C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. currentPlaylist (VB e C#)**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB e C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Play (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





