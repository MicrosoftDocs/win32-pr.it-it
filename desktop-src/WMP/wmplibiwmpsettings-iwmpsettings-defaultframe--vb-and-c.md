---
title: Proprietà defaultFrame IWMPSettings
description: La proprietà defaultFrame ottiene o imposta il nome del frame usato per visualizzare un URL ricevuto in un evento AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent.
ms.assetid: 92c775ac-5ff1-4d21-b21d-491bc48a033f
keywords:
- proprietà defaultFrame Windows Media Player
- proprietà defaultFrame Windows Media Player, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player , proprietà defaultFrame
topic_type:
- apiref
api_name:
- IWMPSettings.defaultFrame
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39352b2c49bfdcd50f3e5c74d88a9fafef6752034dbd220cda3bb34dc0ed5de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053439"
---
# <a name="iwmpsettingsdefaultframe-property"></a>Proprietà IWMPSettings::d efaultFrame

La **proprietà defaultFrame** ottiene o imposta il nome del frame usato per visualizzare un URL ricevuto in un evento **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent.**

## <a name="syntax"></a>Sintassi


```CSharp
public System.String defaultFrame {get; set;}
```


```VB

Public Property defaultFrame As System.String
```





## <a name="property-value"></a>Valore proprietà

Oggetto **System.String** che rappresenta il valore dell'attributo name dell'elemento **FRAME di** destinazione.

## <a name="remarks"></a>Commenti

Se nell'evento **\_ \_ ScriptCommandEvent di WMPOCXEvents** viene specificato un frame di destinazione, questa proprietà viene ignorata.

Questa proprietà viene ignorata quando si usa Netscape Navigator applet Java. In Netscape Navigator, ogni comando di script URL ricevuto visualizza l'URL in una nuova finestra del browser, indipendentemente dal valore di **defaultFrame**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Evento AxWindowsMediaPlayer.ScriptCommand (VB e C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**Interfaccia IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





