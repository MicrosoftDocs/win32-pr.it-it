---
title: Gruppi di funzioni di gestione di rete
description: Le funzioni di gestione della rete possono essere divise nei gruppi seguenti.
ms.assetid: 4b5d3554-f81a-4ecf-bf31-ee4753509f38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bce5c0fb3dd70facb0ebbbb2479b968d428c49e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046914"
---
# <a name="network-management-function-groups"></a>Gruppi di funzioni di gestione di rete

Le funzioni di gestione della rete possono essere divise nei gruppi seguenti:

-   [Funzioni di avviso](alert-functions.md)
-   [Funzioni ApiBuffer](apibuffer-functions.md)
-   [Funzioni del servizio directory](directory-service-functions.md)
-   [Funzioni file system distribuito (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions)
-   [Funzioni Get](get-functions.md)
-   [Funzioni di gruppo](group-functions.md)
-   [Funzioni di gruppo locale](local-group-functions.md)
-   [Funzioni di messaggio](message-functions.md)
-   [Funzioni NetFile](netfile-functions.md)
-   [Funzioni remote Utility](remote-utility-functions.md)
-   [Funzioni di pianificazione](schedule-functions.md)
-   [Funzioni server](server-functions.md)
-   [Funzioni di trasporto per server e workstation](server-and-workstation-transport-functions.md)
-   [Funzioni di sessione](session-functions.md)
-   [Funzioni di condivisione](share-functions.md)
-   [Funzioni statistiche](/windows/desktop/NetShare/statistics-functions)
-   [Usare le funzioni](use-functions.md)
-   [Funzioni utente](user-functions.md)
-   [Funzioni modali utente](user-modal-functions.md)
-   [Funzioni utente workstation e workstation](workstation-and-workstation-user-functions.md)

Se si sta programmando per Active Directory, è possibile chiamare determinati metodi di interfaccia ADSI per ottenere la stessa funzionalità che è possibile ottenere chiamando determinate funzioni di gestione della rete. Per ulteriori informazioni, vedere [mapping di interfacce ADSI alle funzioni di gestione della rete](mapping-adsi-interfaces-to-the-network-management-functions.md).

Il sistema fornisce anche un set indipendente dalla rete di funzioni di rete ([funzioni WNet](/windows/desktop/WNet/wnet-functions)) che consentono alle funzioni di rete di funzionare in diversi prodotti di fornitori di rete. Se l'applicazione può essere convertita in modo da usare una funzione WNet, è necessario eseguire la conversione. Esistono motivi per apportare la modifica:

-   Le funzioni WNet sono indipendenti dalla rete, mentre le funzioni di gestione di rete funzionano solo su reti Microsoft.
-   Alcune funzioni potrebbero non essere supportate nelle versioni future dei sistemi operativi Microsoft se sono state sostituite. Microsoft non prevede di rimuovere funzioni specifiche, a meno che non sia disponibile una funzionalità equivalente o migliore.

 

 