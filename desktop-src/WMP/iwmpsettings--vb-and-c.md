---
title: Interfaccia IWMPSettings (VB e C) (WMP. h)
description: Fornisce proprietà e metodi che ottengono o impostano i valori delle impostazioni di Windows Media Player. L'interfaccia IWMPSettings espone le proprietà seguenti.
ms.assetid: fb37b455-221e-4cee-a219-cacf2938a92a
keywords:
- Interfaccia IWMPSettings (VB e C) Windows Media Player
- Interfaccia IWMPSettings (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPSettings (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db911cc6d18ba40777e77a803480c7fcab4ff8ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326973"
---
# <a name="iwmpsettings-vb-and-c-interface"></a>Interfaccia IWMPSettings (VB e C#)

Fornisce proprietà e metodi che ottengono o impostano i valori delle impostazioni di Windows Media Player.

L'interfaccia **IWMPSettings** espone le proprietà seguenti.

## <a name="members"></a>Membri

L'interfaccia **IWMPSettings (VB e C#)** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IWMPSettings (VB e C#)** presenta questi metodi.



| Metodo                                                               | Descrizione                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**getMode**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md) | Restituisce un valore che indica se la modalità ciclo o shuffle è attiva.<br/> |
| [**setMode**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md) | Imposta la modalità ciclo o shuffle su attivo o inattivo.<br/>               |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IWMPSettings (VB e C#)** presenta queste proprietà.



| Proprietà                                                                                              | Tipo di accesso           | Descrizione                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Avvio automatico**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)<br/>                   | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica se l'elemento multimediale corrente inizia la riproduzione automatica. <br/>                                     |
| [**bilanciare**](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)<br/>                       | Lettura/Scrittura<br/> | Ottiene o imposta il saldo stereo corrente.<br/>                                                                                          |
| [**baseURL**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)<br/>                       | Lettura/Scrittura<br/> | Ottiene o imposta l'URL di base utilizzato per la risoluzione del percorso relativo con i comandi script URL incorporati nel contenuto multimediale digitale. <br/> |
| [**defaultFrame**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)<br/>             | Lettura/Scrittura<br/> | Ottiene o imposta il nome del fotogramma utilizzato per visualizzare un URL ricevuto in un evento **scriptCommand** . <br/>                          |
| [**enableErrorDialogs**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica se le finestre di dialogo di errore vengono visualizzate automaticamente.<br/>                                           |
| [**invokeURLs**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica se gli eventi URL devono avviare un Web browser. <br/>                                                  |
| [**isAvailable**](iwmpsettings-isavailable--vb-and-c.md)<br/>                                  | Sola lettura<br/>  | Ottiene un valore che indica se è possibile eseguire un'azione specificata. In C# si tratta del metodo **get \_ unavailable** .<br/>             |
| [**mute**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)<br/>                             | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica se l'audio è disattivato. <br/>                                                                          |
| [**playCount**](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)<br/>                   | Lettura/Scrittura<br/> | Ottiene o imposta il numero di volte in cui un elemento multimediale verrà riprodotto. <br/>                                                                         |
| [**tasso**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)<br/>                             | Lettura/Scrittura<br/> | Ottiene o imposta la frequenza di riproduzione corrente per il video. <br/>                                                                                |
| [**volume**](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)<br/>                         | Lettura/Scrittura<br/> | Ottiene o imposta il volume di riproduzione corrente. <br/>                                                                                        |



 

Ottenere un'interfaccia **IWMPSettings** usando la proprietà seguente.



| Oggetto                                                                   | Proprietà                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Oggetto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Impostazioni**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaccia IWMPSettings2 (VB e C#)**](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





