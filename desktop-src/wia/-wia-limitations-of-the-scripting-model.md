---
description: 'Altre informazioni su: limitazioni del modello di scripting'
ms.assetid: b8ddbfac-5b5e-4aff-beea-82e7fc984790
title: Limitazioni del modello di scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36ef43cd2cf2133b126eee065c2b33e463eb6401
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307345"
---
# <a name="limitations-of-the-scripting-model"></a>Limitazioni del modello di scripting

> [!Note]  
> Questo sistema di scripting è stato sostituito con il livello di automazione Windows Image Acquisition (WIA). Vedere [livello di automazione acquisizione immagini Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

Il modello di scripting di Windows Image Acquisition (WIA) espone un subset di funzionalità WIA. Nella tabella seguente vengono fornite le descrizioni delle limitazioni del modello di scripting. 

| Funzionalità WIA               | Limitazione del modello di scripting                                                                                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eliminazione dell'interfaccia utente  | Impossibile disattivare l'interfaccia utente per l'impostazione delle proprietà del dispositivo/trasferimento.                                                                                                                                                                                               |
| Impostazione di proprietà              | Impossibile impostare (scrivere) le proprietà di un dispositivo o di un elemento.                                                                                                                                                                                                                        |
| Registrazione per gli eventi di callback | Può ricevere solo la notifica per tre eventi specifici: [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md), [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)e [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md). |
| Gestione degli errori                 | Non è possibile gestire gli errori WIA.                                                                                                                                                                                                                                                |



 

 

 
