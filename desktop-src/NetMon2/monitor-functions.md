---
description: In questa sezione vengono descritte le funzioni helper che è possibile usare per sviluppare monitoraggi personalizzati.
ms.assetid: 2c019183-9823-4e34-bb41-cf35f2731b8f
title: Funzioni di monitoraggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a46aff05c9d8775edf5bb233cb18f288dc7ba4d65ba0300370ee7ede3a2ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677101"
---
# <a name="monitor-functions"></a>Funzioni di monitoraggio

In questa sezione vengono descritte le funzioni helper che è possibile usare per sviluppare monitoraggi personalizzati.



| Funzione                                       | Descrizione                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DllGetMonitorObject](dllgetmonitorobject.md) | Crea un'istanza del monitoraggio.                                                                                                                              |
| [HTMLValueToUnicode](htmlvaluetounicode.md)   | Converte una stringa di \_ versione UTF8 CP HTML in Unicode.                                                                                                             |
| [LoadDWORD](loaddword.md)                     | Carica un **valore DWORD da** una stringa di configurazione HTML.                                                                                                             |
| [LoadIPAddresses](loadipaddresses.md)         | Carica un elenco di indirizzi IP da una stringa di configurazione TEXTAREA HTML.                                                                                             |
| [LoadIPXAddresses](loadipxaddresses.md)       | Carica un elenco di indirizzi IPX da una stringa di configurazione TEXTAREA HTML.                                                                                            |
| [LoadMACAddresses](loadmacaddresses.md)       | Carica un elenco di indirizzi MAC da una stringa di configurazione TEXTAREA HTML.                                                                                             |
| [LoadStringAddr](loadstringaddr.md)           | Trasforma una stringa (ad esempio "157.54.32.45") in un **indirizzo DWORD.**                                                                                             |
| [LoadTCHAR](loadtchar.md)                     | Cerca un nome di variabile richiesto nella stringa di configurazione e alloca spazio sufficiente (usando **HeapAllocMemory)** per archiviarlo, copiarlo e restituirlo. |
| [OnLoadingDLL](onloadingdll.md)               | Indica che il caricamento della DLL è iniziato. MCSVC chiama questa funzione quando carica per la prima volta la DLL di monitoraggio.                                                     |



 

 

 



