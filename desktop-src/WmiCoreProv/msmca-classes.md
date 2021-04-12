---
description: Set di classi WMI che espongono l'architettura di controllo del computer (MCA). System Abstraction Layer (SAL) fornisce tutti gli eventi segnalati nella classe MSMCA. Intel Corporation sviluppa e possiede il MCA.
ms.assetid: 4e35f871-5bce-49ed-a3e8-d2d967e6e2dc
title: Classi MSMCA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461d4c5c50ae5316c96c3dffc18af7b729cfa6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347056"
---
# <a name="msmca-classes"></a>Classi MSMCA

Le classi MSMCA (Microsoft Machine Check Architecture) sono un set di classi WMI che espongono l'architettura di controllo del computer (MCA). System Abstraction Layer (SAL) fornisce tutti gli eventi segnalati nella classe MSMCA. Intel Corporation sviluppa e possiede il MCA.



| Classe                                                                               | Descrizione                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**\_CPUError MSMCAEvent**](msmcaevent-cpuerror.md)                                 | Rappresenta un evento di errore della CPU.                                                                          |
| [**\_Intestazione MSMCAEvent**](msmcaevent-header.md)                                     | Rappresenta l'intestazione comune utilizzata da tutte le classi MSMCAEvent.                                          |
| [**\_InvalidError MSMCAEvent**](msmcaevent-invaliderror.md)                         | Rappresenta un errore di non valido dell'architettura di controllo della memoria (MCA).                                            |
| [**\_MemoryError MSMCAEvent**](msmcaevent-memoryerror.md)                           | Rappresenta un evento di errore di memoria MCA.                                                                  |
| [**\_MemoryPageRemoved MSMCAEvent**](msmcaevent-memorypageremoved.md)               | Indica che il sistema operativo ha rimosso una pagina fisica di memoria.                                 |
| [**\_PCIBusError MSMCAEvent**](msmcaevent-pcibuserror.md)                           | Rappresenta un errore del bus PCI MCA.                                                                       |
| [**\_PCIComponentError MSMCAEvent**](msmcaevent-pcicomponenterror.md)               | Rappresenta un errore del componente PCI MCA.                                                                 |
| [**\_PlatformSpecificError MSMCAEvent**](msmcaevent-platformspecificerror.md)       | Rappresenta un errore specifico della piattaforma MCA.                                                             |
| [**\_SMBIOSError MSMCAEvent**](msmcaevent-smbioserror.md)                           | Rappresenta un errore del BIOS di sistema MCA.                                                                   |
| [**\_SwitchToCMCPolling MSMCAEvent**](msmcaevent-switchtocmcpolling.md)             | Indica che la gestione della verifica del computer corretta passa al polling.                            |
| [**\_SystemEventError MSMCAEvent**](msmcaevent-systemeventerror.md)                 | Rappresenta un errore di evento di sistema MCA.                                                                  |
| [**MSMCAInfo**](msmcainfo.md)                                                      | Classe di base astratta dalla quale vengono derivate tutte le classi di dati del provider MCA (Machine Check Architecture). |
| [**\_Voce MSMCAInfo**](msmcainfo-entry.md)                                         | Rappresenta un MCA, un controllo del computer corretto (CMC) o una voce di informazioni di errore della piattaforma (CPE) corretta. |
| [**\_RawCMCEvent MSMCAInfo**](msmcainfo-rawcmcevent.md)                             | Contiene un evento CMC.                                                                                  |
| [**\_RawCorrectedPlatformEvent MSMCAInfo**](msmcainfo-rawcorrectedplatformevent.md) | Contiene un evento della piattaforma con correzione.                                                                   |
| [**\_RawMCAData MSMCAInfo**](msmcainfo-rawmcadata.md)                               | Specifica i log MCA non elaborati.                                                                            |
| [**\_RawMCAEvent MSMCAInfo**](msmcainfo-rawmcaevent.md)                             | Contiene un evento MCA.                                                                                  |
| [**WmiEvent**](wmievent.md)                                                        | Classe di base astratta da cui derivano tutte le classi di evento del provider MCA.                             |



 

 

 



