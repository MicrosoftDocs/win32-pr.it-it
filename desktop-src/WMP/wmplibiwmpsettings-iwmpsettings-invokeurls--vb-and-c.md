---
title: Proprietà invokeURLs di IWMPSettings
description: La proprietà invokeURLs Ottiene o imposta un valore che indica se gli eventi URL devono avviare un Web browser.
ms.assetid: e16c968d-a1b7-4c3a-9c1a-5748ed44cdac
keywords:
- Finestra delle proprietà di invokeURLs Media Player
- Proprietà di invokeURLs Media Player Windows, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player, proprietà invokeURLs
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
ms.openlocfilehash: bbdd68d797b54f4e9365f381b2b5c705dffc419b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333910"
---
# <a name="iwmpsettingsinvokeurls-property"></a>Proprietà IWMPSettings:: invokeURLs

La proprietà **invokeURLs** Ottiene o imposta un valore che indica se gli eventi URL devono avviare un Web browser.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Boolean invokeURLs {get; set;}
```


```VB

Public Property invokeURLs As System.Boolean
```





## <a name="property-value"></a>Valore proprietà

Valore **System. Boolean** che indica se gli eventi URL devono avviare un Web browser. Il valore predefinito è **True**.

## <a name="remarks"></a>Commenti

I file multimediali digitali e i flussi possono contenere comandi di script URL. Quando un comando script URL viene inviato al controllo Media Player di Windows, viene passato prima al gestore eventi **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** , indipendentemente dal valore recuperato da **invokeURLs**. Dopo la chiusura di **\_ WMPOCXEvents \_ ScriptCommandEvent** , Windows Media Player controlla **invokeURLs** per determinare se avviare il Web browser predefinito con l'URL. È possibile visualizzare gli URL in modo selettivo selezionando **\_ WMPOCXEvents \_ ScriptCommandEvent** e impostando **invokeURLs** come desiderato.

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

 

 





