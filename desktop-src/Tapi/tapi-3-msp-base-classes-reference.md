---
description: Il materiale seguente fornisce informazioni dettagliate sulle classi di base del provider di servizi multimediali.
ms.assetid: ef845c44-1ff5-42a1-8e91-38d66e6fe363
title: Informazioni di riferimento sulle classi base DI TAPI 3 MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1c0b2f19f372e60972c66d965f689ec79f930f343080be21471fbc4ba59f67c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905741"
---
# <a name="tapi-3-msp-base-classes-reference"></a>Informazioni di riferimento sulle classi base DI TAPI 3 MSP

Il materiale seguente fornisce informazioni dettagliate sulle classi di base del provider di servizi multimediali.



| Classi di base del provider di servizi multimediali (ordine alfabetico) | Descrizione                                                                                                                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CAudioCaptureTerminal](caudiocaptureterminal.md)       | Derivato da [CSingleFilterTerminal e](csinglefilterterminal.md) implementa un terminale di acquisizione audio statico per i dispositivi wave DirectShow filtro wavein. Definito in MSPtmac.h.               |
| [CAudioRenderTerminal](caudiorenderterminal.md)         | Derivato da [CSingleFilterTerminal e](csinglefilterterminal.md) implementa un terminale di rendering audio statico per i dispositivi wave usando il DirectShow waveout. Definito in MSPtrmar.h.              |
| [CBaseTerminal](cbaseterminal.md)                       | Classe di base del terminale applicabile ai terminali statici e dinamici. È completamente generico, quindi qualsiasi implementazione terminale può derivare direttamente o indirettamente da questa classe. Definito in MSPterm.h |
| [**CMSPAddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)                       | Implementa l'oggetto indirizzo MSP e supporta [**l'interfaccia ITMSPAddress.**](/windows/desktop/api/msp/nn-msp-itmspaddress) Definito in MSPaddr.h.                                                                                |
| [CMSPArray](cmsparray.md)                               | Modello che implementa una matrice intelligente che crescerà su richiesta. Definito in MSPutils.h.                                                                                                               |
| [**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)                     | Fornisce un'implementazione generica dell'oggetto chiamata e supporta [**l'interfaccia ITStreamControl.**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) Definito in MSPcall.h.                                                       |
| [**CMSPCallMultiGraph**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)         | Definisce una chiamata che usa un grafico di filtro per ogni flusso. Definito in MSPcall.h.                                                                                                                          |
| [**CMSPStream**](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)                         | Espone metodi che consentono a un'applicazione di avviare, sospendere o arrestare un flusso secondario e di selezionare o deselezionare i terminali. Definito in MSPstrm.h.                                                              |
| [Thread CMSP](cmspthread.md)                             | Implementa il thread di lavoro del msp. Definito in MSPthrd.h.                                                                                                                                               |
| [CSingleFilterTerminal](csinglefilterterminal.md)       | Classe di base del terminale aggiuntiva applicabile ai terminali statici e dinamici. Rende più specifica l'implementazione presupponendo che il terminale abbia un singolo DirectShow filtro. Definito in MSPterm.h.    |
| [CVideoCaptureTerminal](cvideocaptureterminal.md)       | Derivato da [CSingleFilterTerminal e](csinglefilterterminal.md) implementa un terminale di acquisizione video statico usando un singolo DirectShow filtro. Definito in MSPtmvc.h.                                  |



 

 

 
