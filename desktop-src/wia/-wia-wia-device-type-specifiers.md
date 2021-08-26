---
description: Windows Gli identificatori di tipo di dispositivo wia (Image Acquisition) sono costanti che indicano il tipo di dispositivo collegato al computer di un utente.
ms.assetid: 569b99ab-628b-4a43-a6e5-0ae81524fcc0
title: Identificatori di tipo di dispositivo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdefac4672b46fea7a7dad021fa9ebec710b3b77eabb7a1f7cac405b8e7e519
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056971"
---
# <a name="wia-device-type-specifiers"></a>Identificatori di tipo di dispositivo WIA

Windows Gli identificatori di tipo di dispositivo wia (Image Acquisition) sono costanti che indicano il tipo di dispositivo collegato al computer di un utente. Usare la macro GET \_ STIDEVICE TYPE per ottenere questi valori dalla proprietà del tipo \_ di dispositivo WIA. Di seguito sono riportati gli identificatori di tipo di dispositivo WIA validi: 

| Tipo di dispositivo                 | Significato                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| StiDeviceTypeDefault        | Dispositivo WIA generico. Durante le enumerazioni dei dispositivi, questa costante viene usata per enumerare tutti i dispositivi WIA.                         |
| StiDeviceTypeDigitalCamera  | Il dispositivo è una fotocamera. *Questo identificatore non è supportato da Windows* Vista e versioni *successive.*                                     |
| StiDeviceTypeScanner        | Il dispositivo è uno scanner.                                                                                                    |
| StiDeviceTypeStreamingVideo | Il dispositivo contiene video in streaming. *Questo identificatore non è supportato da* Windows Server 2003, Windows Vista o versioni *successive.*  |



 

 

 



