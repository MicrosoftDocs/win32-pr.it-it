---
title: Proprietà invokeURLs di IWMPSettings
description: La proprietà invokeURLs ottiene o imposta un valore che indica se gli eventi URL devono avviare un Web browser.
ms.assetid: e16c968d-a1b7-4c3a-9c1a-5748ed44cdac
keywords:
- Proprietà invokeURLs Windows Media Player
- proprietà invokeURLs Windows Media Player, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player proprietà invokeURLs
topic_type:
- apiref
api_name:
- IWMPSettings.invokeURLs
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dba44af7e6ec700f9df810486acb57af24a14c9e5d4966fddbfe4b242d346a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053429"
---
# <a name="iwmpsettingsinvokeurls-property"></a>Proprietà IWMPSettings::invokeURLs

La **proprietà invokeURLs** ottiene o imposta un valore che indica se gli eventi URL devono avviare un Web browser.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Boolean invokeURLs {get; set;}
```


```VB

Public Property invokeURLs As System.Boolean
```





## <a name="property-value"></a>Valore proprietà

Valore **System.Boolean che** indica se gli eventi URL devono avviare un Web browser. Il valore predefinito è **True**.

## <a name="remarks"></a>Commenti

I file multimediali digitali e i flussi possono contenere comandi di script URL. Quando un comando di script URL viene inviato al controllo Windows Media Player, viene passato per primo al gestore dell'evento **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** indipendentemente dal valore recuperato da **invokeURLs**. Dopo la chiusura di **\_ WMPOCXEvents \_ ScriptCommandEvent,** Windows Media Player controlla **invokeURLs** per determinare se avviare il Web browser predefinito con l'URL. È possibile visualizzare in modo selettivo gli URL selezionandoli in **\_ WMPOCXEvents \_ ScriptCommandEvent** e impostando **invokeURLs come** desiderato.

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

 

 





