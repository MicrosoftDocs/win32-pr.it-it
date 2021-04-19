---
title: Proprietà defaultFrame di IWMPSettings
description: La proprietà defaultFrame Ottiene o imposta il nome del frame utilizzato per visualizzare un URL ricevuto in un \_ evento AxWindowsMediaPlayer WMPOCXEvents \_ ScriptCommandEvent.
ms.assetid: 92c775ac-5ff1-4d21-b21d-491bc48a033f
keywords:
- Finestra delle proprietà di defaultFrame Media Player
- Proprietà di defaultFrame Media Player Windows, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player, proprietà defaultFrame
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
ms.openlocfilehash: 28539640214165ab5b2808762ed854b19b434311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325965"
---
# <a name="iwmpsettingsdefaultframe-property"></a>IWMPSettings::d proprietà efaultFrame

La proprietà **DefaultFrame** Ottiene o imposta il nome del frame utilizzato per visualizzare un URL ricevuto in un evento **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** .

## <a name="syntax"></a>Sintassi


```CSharp
public System.String defaultFrame {get; set;}
```


```VB

Public Property defaultFrame As System.String
```





## <a name="property-value"></a>Valore proprietà

**System. String** che corrisponde al valore dell'attributo Name dell'elemento **frame** di destinazione.

## <a name="remarks"></a>Commenti

Se viene specificato un frame di destinazione nell'evento **\_ WMPOCXEvents \_ ScriptCommandEvent** , questa proprietà viene ignorata.

Questa proprietà viene ignorata quando si usa l'applet Java del navigatore Netscape. In Netscape Navigator ogni comando script URL ricevuto visualizzerà l'URL in una nuova finestra del browser, indipendentemente dal valore di **DefaultFrame**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Evento AxWindowsMediaPlayer. ScriptCommand (VB e C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**Interfaccia IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





