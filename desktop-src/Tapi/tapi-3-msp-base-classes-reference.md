---
description: Il materiale seguente fornisce informazioni dettagliate sulle classi base del provider di servizi multimediali.
ms.assetid: ef845c44-1ff5-42a1-8e91-38d66e6fe363
title: Guida di riferimento alle classi di base di TAPI 3 MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4cca24b69a645b18cc0950288e0de983b54355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227481"
---
# <a name="tapi-3-msp-base-classes-reference"></a>Guida di riferimento alle classi di base di TAPI 3 MSP

Il materiale seguente fornisce informazioni dettagliate sulle classi base del provider di servizi multimediali.



| Classi base del provider di servizi multimediali (ordine alfabetico) | Descrizione                                                                                                                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CAudioCaptureTerminal](caudiocaptureterminal.md)       | Derivato da [CSingleFilterTerminal](csinglefilterterminal.md) e implementa un terminale di acquisizione audio statico per i dispositivi Wave usando il filtro di DirectShow WaveIn. Definito in MSPtmac. h.               |
| [CAudioRenderTerminal](caudiorenderterminal.md)         | Derivato da [CSingleFilterTerminal](csinglefilterterminal.md) e implementa un terminale di rendering audio statico per i dispositivi Wave usando il filtro di Wave di DirectShow. Definito in MSPtrmar. h.              |
| [CBaseTerminal](cbaseterminal.md)                       | Classe di base del terminale applicabile sia ai terminali statici che a quelli dinamici. È completamente generico, pertanto qualsiasi implementazione del terminale può derivare direttamente o indirettamente da questa classe. Definito in MSPterm. h |
| [**CMSPAddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)                       | Implementa l'oggetto indirizzo MSP e supporta l'interfaccia [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress) . Definito in MSPaddr. h.                                                                                |
| [CMSPArray](cmsparray.md)                               | Modello che implementa una Smart Array che aumenterà su richiesta. Definito in MSPutils. h.                                                                                                               |
| [**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)                     | Fornisce un'implementazione generica dell'oggetto chiamata e supporta l'interfaccia [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) . Definito in MSPcall. h.                                                       |
| [**CMSPCallMultiGraph**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)         | Definisce una chiamata che usa un grafico di filtro per ogni flusso. Definito in MSPcall. h.                                                                                                                          |
| [**CMSPStream**](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)                         | Espone metodi che consentono a un'applicazione di avviare, sospendere o arrestare un sottoflusso e di selezionare o deselezionare i terminali. Definito in MSPstrm. h.                                                              |
| [CMSPThread](cmspthread.md)                             | Implementa il thread di lavoro di MSP. Definito in MSPthrd. h.                                                                                                                                               |
| [CSingleFilterTerminal](csinglefilterterminal.md)       | Classe di base terminale aggiuntiva applicabile sia ai terminali statici che a quelli dinamici. Rende più specifica l'implementazione supponendo che il terminale disponga di un singolo filtro DirectShow. Definito in MSPterm. h.    |
| [CVideoCaptureTerminal](cvideocaptureterminal.md)       | Derivato da [CSingleFilterTerminal](csinglefilterterminal.md) e implementa un terminale di acquisizione video statico usando un singolo filtro DirectShow. Definito in MSPtmvc. h.                                  |



 

 

 
