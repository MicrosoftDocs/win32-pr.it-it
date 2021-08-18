---
title: Interfaccia IWMPSettings (VB e C) (Wmp.h)
description: Fornisce proprietà e metodi che ottengono o impostano i valori delle Windows Media Player predefinite. L'interfaccia IWMPSettings espone le proprietà seguenti.
ms.assetid: fb37b455-221e-4cee-a219-cacf2938a92a
keywords:
- Interfaccia IWMPSettings (VB e C) Windows Media Player
- Interfaccia IWMPSettings (VB e C) Windows Media Player , descritta
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
ms.openlocfilehash: 6a537efcd9b39f993705244020e579b9d667164180fd5cd70ab05fc692bed8fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996471"
---
# <a name="iwmpsettings-vb-and-c-interface"></a>Interfaccia IWMPSettings (VB e C#)

Fornisce proprietà e metodi che ottengono o impostano i valori delle Windows Media Player predefinite.

**L'interfaccia IWMPSettings** espone le proprietà seguenti.

## <a name="members"></a>Membri

**L'interfaccia IWMPSettings (VB e C#)** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili **nell'interfaccia IWMPSettings (VB e C#).**



| Metodo                                                               | Descrizione                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**getMode**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md) | Restituisce un valore che indica se la modalità ciclo o casuale è attiva.<br/> |
| [**setMode**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md) | Imposta la modalità loop o shuffle su attiva o inattiva.<br/>               |



 

### <a name="properties"></a>Proprietà

Queste **proprietà sono disponibili nell'interfaccia IWMPSettings (VB e C#).**



| Proprietà                                                                                              | Tipo di accesso           | Descrizione                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autostart**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)<br/>                   | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica se la riproduzione dell'elemento multimediale corrente inizia automaticamente. <br/>                                     |
| [**Equilibrio**](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)<br/>                       | Lettura/Scrittura<br/> | Ottiene o imposta il bilanciamento stereo corrente.<br/>                                                                                          |
| [**baseURL**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)<br/>                       | Lettura/Scrittura<br/> | Ottiene o imposta l'URL di base utilizzato per la risoluzione del percorso relativo con comandi di script URL incorporati nel contenuto multimediale digitale. <br/> |
| [**defaultFrame**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)<br/>             | Lettura/Scrittura<br/> | Ottiene o imposta il nome del frame utilizzato per visualizzare un URL ricevuto in un **evento scriptCommand.** <br/>                          |
| [**enableErrorDialogs**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica se le finestre di dialogo di errore vengono visualizzate automaticamente.<br/>                                           |
| [**invokeURLs**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica se gli eventi URL devono avviare un Web browser. <br/>                                                  |
| [**isAvailable**](iwmpsettings-isavailable--vb-and-c.md)<br/>                                  | Sola lettura<br/>  | Ottiene un valore che indica se è possibile eseguire un'azione specificata. In C# si tratta del **metodo get \_ isAvailable.**<br/>             |
| [**Muto**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)<br/>                             | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica se l'audio è disattivato. <br/>                                                                          |
| [**playCount**](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)<br/>                   | Lettura/Scrittura<br/> | Ottiene o imposta il numero di volte in cui un elemento multimediale verrà riprodotto. <br/>                                                                         |
| [**Tasso**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)<br/>                             | Lettura/Scrittura<br/> | Ottiene o imposta la velocità di riproduzione corrente per il video. <br/>                                                                                |
| [**Volume**](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)<br/>                         | Lettura/Scrittura<br/> | Ottiene o imposta il volume di riproduzione corrente. <br/>                                                                                        |



 

Ottenere **un'interfaccia IWMPSettings** usando la proprietà seguente.



| Oggetto                                                                   | Proprietà                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Oggetto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Impostazioni**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaccia IWMPSettings2 (VB e C#)**](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





