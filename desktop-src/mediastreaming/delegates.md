---
title: Delegati
description: L'API di streaming multimediale fornisce le funzioni del gestore eventi seguenti.
ms.assetid: CDE7B829-D0D1-479D-9B35-4445E711AF58
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23fbf0f44a0822fd0c8914833b0696fcb9aacad
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516743"
---
# <a name="delegates"></a>Delegati

L' [API di streaming multimediale](media-streaming-api-portal.md) fornisce le funzioni del gestore eventi seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                   | Descrizione                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))<br/>                   | Rappresenta la funzione che gestirà l'evento [**ConnectionStatusChanged**](connectionstatuschanged.md) che notifica al client le modifiche apportate allo stato della connessione di rete del dispositivo.<br/>               |
| [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))<br/>       | Rappresenta la funzione che gestirà gli eventi [**DeviceArrival**](devicearrival.md) e [**DeviceDeparture**](devicedeparture.md) che notificano al client le modifiche nell'elenco dei dispositivi memorizzati nella cache.<br/> |
| [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))<br/> | Rappresenta la funzione che gestirà l'evento [**RenderingParametersUpdate**](renderingparametersupdate.md) che invia una notifica al client di un aggiornamento a uno dei parametri del controllo di rendering di ricevitore.<br/>  |
| [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))<br/> | Rappresenta la funzione che gestirà l'evento [**TransportParametersUpdate**](transportparametersupdate.md) che invia una notifica al client di un aggiornamento a uno dei parametri di trasporto di ricevitore s.<br/>          |



 

 

