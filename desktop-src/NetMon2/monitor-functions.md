---
description: In questa sezione vengono descritte le funzioni di supporto che è possibile utilizzare per sviluppare monitoraggi personalizzati.
ms.assetid: 2c019183-9823-4e34-bb41-cf35f2731b8f
title: Funzioni di monitoraggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9391927104196e282d4438c0b047e233d61f3619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879498"
---
# <a name="monitor-functions"></a>Funzioni di monitoraggio

In questa sezione vengono descritte le funzioni di supporto che è possibile utilizzare per sviluppare monitoraggi personalizzati.



| Funzione                                       | Descrizione                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DllGetMonitorObject](dllgetmonitorobject.md) | Crea un'istanza del monitoraggio.                                                                                                                              |
| [HTMLValueToUnicode](htmlvaluetounicode.md)   | Converte una \_ stringa di versione HTML CP UTF8 in Unicode.                                                                                                             |
| [LoadDWORD](loaddword.md)                     | Carica un **valore DWORD** da una stringa di configurazione HTML.                                                                                                             |
| [LoadIPAddresses](loadipaddresses.md)         | Carica un elenco di indirizzi IP da una stringa di configurazione HTML TEXTAREA.                                                                                             |
| [LoadIPXAddresses](loadipxaddresses.md)       | Carica un elenco di indirizzi IPX da una stringa di configurazione HTML TEXTAREA.                                                                                            |
| [LoadMACAddresses](loadmacaddresses.md)       | Carica un elenco di indirizzi MAC da una stringa di configurazione HTML TEXTAREA.                                                                                             |
| [LoadStringAddr](loadstringaddr.md)           | Trasforma una stringa (ad esempio "157.54.32.45") in un indirizzo **DWORD** .                                                                                             |
| [LoadTCHAR](loadtchar.md)                     | Cerca un nome di variabile richiesto nella stringa di configurazione e alloca spazio sufficiente (usando **HeapAllocMemory**) per archiviare, copiare e restituire l'oggetto. |
| [OnLoadingDLL](onloadingdll.md)               | Indica che il caricamento della DLL è iniziato. MCSVC chiama questa funzione quando carica la DLL di monitoraggio per la prima volta.                                                     |



 

 

 



