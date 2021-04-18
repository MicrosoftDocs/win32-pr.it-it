---
description: Gli identificatori del tipo di dispositivo Windows Image Acquisition (WIA) sono costanti che indicano il tipo di dispositivo collegato al computer di un utente.
ms.assetid: 569b99ab-628b-4a43-a6e5-0ae81524fcc0
title: Identificatori del tipo di dispositivo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc18b000d84bec5e5be37a5a5c52f28f6f8325d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307316"
---
# <a name="wia-device-type-specifiers"></a>Identificatori del tipo di dispositivo WIA

Gli identificatori del tipo di dispositivo Windows Image Acquisition (WIA) sono costanti che indicano il tipo di dispositivo collegato al computer di un utente. Utilizzare la \_ \_ macro di tipo Get STIDEVICE per ottenere questi valori dalla proprietà WIA Device Type. Gli identificatori di tipo di dispositivo WIA validi sono i seguenti: 

| Tipo di dispositivo                 | Significato                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| StiDeviceTypeDefault        | Dispositivo WIA generico. Durante le enumerazioni dei dispositivi, questa costante viene usata per enumerare tutti i dispositivi WIA.                         |
| StiDeviceTypeDigitalCamera  | Il dispositivo è una fotocamera. *Questo identificatore non è supportato da* Windows Vista *e versioni successive.*                                     |
| StiDeviceTypeScanner        | Il dispositivo è uno scanner.                                                                                                    |
| StiDeviceTypeStreamingVideo | Il dispositivo contiene video di streaming. *Questo identificatore non è supportato da* Windows Server 2003 *,* Windows Vista *o versioni successive.* |



 

 

 



