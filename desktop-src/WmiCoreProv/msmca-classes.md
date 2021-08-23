---
description: Set di classi WMI che espongono l'architettura di controllo del computer . System Abstraction Layer (SAL) fornisce tutti gli eventi segnalati nella classe MSMCA. Intel Corporation sviluppa e possiede l'mca.
ms.assetid: 4e35f871-5bce-49ed-a3e8-d2d967e6e2dc
title: Classi MSMCA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0f70bead9acbbb23fe0e2115ac12f967c7908f1f0eefa16d65cd1a57947e76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641081"
---
# <a name="msmca-classes"></a>Classi MSMCA

Le classi MSMCA (Microsoft Machine Check Architecture) sono un set di classi WMI che espongono l'architettura di controllo del computer (MCA). System Abstraction Layer (SAL) fornisce tutti gli eventi segnalati nella classe MSMCA. Intel Corporation sviluppa e possiede l'mca.



| Classe                                                                               | Descrizione                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**MSMCAEvent \_ CPUError**](msmcaevent-cpuerror.md)                                 | Rappresenta un evento di errore della CPU.                                                                          |
| [**Intestazione \_ MSMCAEvent**](msmcaevent-header.md)                                     | Rappresenta l'intestazione comune utilizzata da tutte le classi MSMCAEvent.                                          |
| [**MSMCAEvent \_ InvalidError**](msmcaevent-invaliderror.md)                         | Rappresenta un errore non valido di Memory Check Architecture (MCA).                                            |
| [**MSMCAEvent \_ MemoryError**](msmcaevent-memoryerror.md)                           | Rappresenta un evento di errore di memoria MCA.                                                                  |
| [**MSMCAEvent \_ MemoryPageRemoved**](msmcaevent-memorypageremoved.md)               | Indica che il sistema operativo ha rimosso una pagina fisica di memoria.                                 |
| [**MSMCAEvent \_ PCIBusError**](msmcaevent-pcibuserror.md)                           | Rappresenta un errore del bus MCA PCI.                                                                       |
| [**MSMCAEvent \_ PCIComponentError**](msmcaevent-pcicomponenterror.md)               | Rappresenta un errore del componente PCI MCA.                                                                 |
| [**MSMCAEvent \_ PlatformSpecificError**](msmcaevent-platformspecificerror.md)       | Rappresenta un errore specifico della piattaforma MCA.                                                             |
| [**MSMCAEvent \_ SMBIOSError**](msmcaevent-smbioserror.md)                           | Rappresenta un errore bios del sistema MCA.                                                                   |
| [**MSMCAEvent \_ SwitchToCMCPolling**](msmcaevent-switchtocmcpolling.md)             | Indica che la gestione del controllo del computer corretta viene passata al polling.                            |
| [**MSMCAEvent \_ SystemEventError**](msmcaevent-systemeventerror.md)                 | Rappresenta un errore di evento di sistema MCA.                                                                  |
| [**MSMCAInfo**](msmcainfo.md)                                                      | Classe di base astratta da cui vengono derivate tutte le classi di dati del provider MCA (Machine Check Architecture). |
| [**Voce \_ MSMCAInfo**](msmcainfo-entry.md)                                         | Rappresenta una voce di informazioni MCA, CMC (Corrected Machine Check) o Corrected Platform Error (CPE). |
| [**MSMCAInfo \_ RawCMCEvent**](msmcainfo-rawcmcevent.md)                             | Contiene un evento CMC.                                                                                  |
| [**MSMCAInfo \_ RawCorrectedPlatformEvent**](msmcainfo-rawcorrectedplatformevent.md) | Contiene un evento della piattaforma corretto.                                                                   |
| [**MSMCAInfo \_ RawMCAData**](msmcainfo-rawmcadata.md)                               | Specifica i log MCA non elaborati.                                                                            |
| [**MSMCAInfo \_ RawMCAEvent**](msmcainfo-rawmcaevent.md)                             | Contiene un evento MCA.                                                                                  |
| [**WmiEvent**](wmievent.md)                                                        | Classe di base astratta da cui vengono derivate tutte le classi di evento del provider MCA.                             |



 

 

 



