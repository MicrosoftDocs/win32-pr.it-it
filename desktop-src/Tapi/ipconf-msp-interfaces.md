---
description: Il provider di servizi di audioconferenza IP implementa diverse interfacce specifiche del provider per il controllo partecipante. Queste interfacce sono esposte nell'oggetto chiamata, se questo MSP è associato alla chiamata.
ms.assetid: 01af2452-de2d-42ce-970d-82a83ae0b428
title: Interfacce MSP IPConf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edb3c04a93909d237ae25e06c3ed2e0fcc5db9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131043"
---
# <a name="ipconf-msp-interfaces"></a>Interfacce MSP IPConf

\[ Le interfacce MSP IPConf non sono disponibili per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il provider di servizi di audioconferenza IP implementa diverse interfacce specifiche del provider per il controllo partecipante. Queste interfacce sono esposte nell'oggetto chiamata, se questo MSP è associato alla chiamata.

Le interfacce [**ITParticipantEvent**](itparticipantevent.md) e [**IEnumParticipant**](ienumparticipant.md) sono oggetti autonomi e sono elencate di seguito per praticità di riferimento.



| Interfaccia                                            | Descrizione                                                                                                                                               |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMulticastControl**](imulticastcontrol.md)       | Consente a un'applicazione di impostare e ottenere la modalità loopback [**( \_ \_ modalità loopback multicast**](multicast-loopback-mode.md)) per un oggetto conferenza multicast. |
| [**ITParticipant**](itparticipant.md)               | Consente a un'applicazione di recuperare informazioni sui partecipanti alla conferenza e ottenere i puntatori ai flussi associati a tali partecipanti.             |
| [**ITParticipantControl**](itparticipantcontrol.md) | Consente a un'applicazione di recuperare i puntatori ai partecipanti a una conferenza.                                                                           |
| [**ITParticipantEvent**](itparticipantevent.md)     | Consente a un'applicazione di recuperare informazioni sugli eventi relativi a un partecipante alla conferenza.                                                                  |
| [**IEnumParticipant**](ienumparticipant.md)         | Enumera [**ITParticipant**](itparticipant.md).                                                                                                        |



 

 

 



