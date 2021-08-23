---
title: Gruppi di funzioni di gestione di rete
description: Le funzioni di gestione della rete possono essere suddivise nei gruppi seguenti.
ms.assetid: 4b5d3554-f81a-4ecf-bf31-ee4753509f38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e49a8c45c59031a12653f5cb863fef320a33c93bc60cabdd4cd6fb4aece9dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012509"
---
# <a name="network-management-function-groups"></a>Gruppi di funzioni di gestione di rete

Le funzioni di gestione della rete possono essere suddivise nei gruppi seguenti:

-   [Funzioni di avviso](alert-functions.md)
-   [Funzioni ApiBuffer](apibuffer-functions.md)
-   [Funzioni del servizio directory](directory-service-functions.md)
-   [file system distribuito (Dfs)](/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions)
-   [Funzioni Get](get-functions.md)
-   [Funzioni di raggruppamento](group-functions.md)
-   [Funzioni del gruppo locale](local-group-functions.md)
-   [Funzioni di messaggio](message-functions.md)
-   [Funzioni NetFile](netfile-functions.md)
-   [Funzioni di Utilità remota](remote-utility-functions.md)
-   [Funzioni di pianificazione](schedule-functions.md)
-   [Funzioni server](server-functions.md)
-   [Funzioni di trasporto server e workstation](server-and-workstation-transport-functions.md)
-   [Funzioni di sessione](session-functions.md)
-   [Funzioni di condivisione](share-functions.md)
-   [Funzioni statistiche](/windows/desktop/NetShare/statistics-functions)
-   [Usare le funzioni](use-functions.md)
-   [Funzioni utente](user-functions.md)
-   [Funzioni modali dell'utente](user-modal-functions.md)
-   [Funzioni utente per workstation e workstation](workstation-and-workstation-user-functions.md)

Se si programma per Active Directory, è possibile chiamare determinati metodi di interfaccia ADSI per ottenere le stesse funzionalità che è possibile ottenere chiamando determinate funzioni di gestione di rete. Per altre informazioni, vedere [Mapping ad ADSI Interfaces to the Network Management Functions](mapping-adsi-interfaces-to-the-network-management-functions.md).

Il sistema fornisce anche un set indipendente dalla rete di funzioni di rete[(funzioni WNet](/windows/desktop/WNet/wnet-functions)) che consentono alle funzioni di rete di funzionare in prodotti di fornitori di reti diversi. Se l'applicazione può essere convertita in modo da usare una funzione WNet, è necessario eseguire la conversione. Esistono motivi per apportare la modifica:

-   Le funzioni WNet sono indipendenti dalla rete, mentre le funzioni di gestione di rete funzionano solo su reti Microsoft.
-   Alcune delle funzioni potrebbero non essere supportate nelle versioni future dei sistemi operativi Microsoft se sono state sostituite. Microsoft non prevede di rimuovere funzioni specifiche a meno che non siano disponibili funzionalità equivalenti o migliori.

 

 