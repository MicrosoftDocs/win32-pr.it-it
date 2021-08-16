---
description: 'Altre informazioni su: Limitazioni del modello di scripting'
ms.assetid: b8ddbfac-5b5e-4aff-beea-82e7fc984790
title: Limitazioni del modello di scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4a1b2dc25c1ea73fd9d793e4d3de1bff7c8193b04aadbe00796ca4a021791886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208063"
---
# <a name="limitations-of-the-scripting-model"></a>Limitazioni del modello di scripting

> [!Note]  
> Questo sistema di scripting è stato sostituito con Windows di automazione di acquisizione di immagini (WIA). Vedere [Windows di automazione dell'acquisizione di immagini.](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)

 

Il Windows di scripting WIA (Image Acquisition) espone un subset di funzionalità WIA. Nella tabella seguente vengono fornite le descrizioni delle limitazioni del modello di scripting. 

| Funzionalità WIA               | Limitazione del modello di scripting                                                                                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eliminazione dell'interfaccia utente  | Impossibile eliminare l'interfaccia utente per l'impostazione delle proprietà del dispositivo/trasferimento.                                                                                                                                                                                               |
| Impostazione di proprietà              | Non è possibile impostare (scrivere) le proprietà di dispositivi o elementi.                                                                                                                                                                                                                        |
| Registrazione per eventi di callback | Può ricevere notifica solo per tre eventi specificati: [**OnTransferComplete,**](-wia--iwiaevents-ontransfercomplete.md) [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)e [**OnDeviceDisconnected.**](-wia--iwiaevents-ondevicedisconnected.md) |
| Gestione degli errori                 | Impossibile gestire gli errori WIA.                                                                                                                                                                                                                                                |



 

 

 
