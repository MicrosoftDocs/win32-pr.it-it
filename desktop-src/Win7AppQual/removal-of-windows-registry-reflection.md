---
description: .
ms.assetid: 4b42d44d-cde8-4d96-96c5-24b7ab7e4cec
title: Rimozione della reflection del registro di sistema di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c610cb0b6ce446e3105fd61cb940028f478892ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317613"
---
# <a name="removal-of-windows-registry-reflection"></a>Rimozione della reflection del registro di sistema di Windows

## <a name="platform"></a>Piattaforma

**Client** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Effetto sulle funzionalità

 **Gravità** -bassa  
**Frequenza** -bassa  





## <a name="description"></a>Descrizione

Il processo di reflection del registro di sistema copia le chiavi e i valori del registro di sistema tra due visualizzazioni del registro di sistema per mantene Nelle installazioni precedenti di Windows a 64 bit, il processo ha riflesso un subset delle chiavi del registro di sistema reindirizzate tra le visualizzazioni a 32 bit e 64 bit. Tuttavia, l'implementazione di questo ha causato alcune incoerenze nello stato del registro di sistema. Per informazioni dettagliate sulla reflection del registro di sistema, vedere l'articolo di MSDN corrispondente nella sezione *collegamenti ad altre risorse* .

A partire da Windows 7, la reflection del registro di sistema è stata rimossa completamente e sono state unite le chiavi che erano state riflesse:

-   \_ \_ Classi software del computer locale \\ HKEY \\
-   HKEY \_ \_ computer locale \\ software \\ Microsoft \\ COM3
-   HKEY \_ \_ computer locale \\ software \\ Microsoft \\ EventSystem
-   \_Software per \_ computer locale HKEY \\ \\ Microsoft \\ OLE
-   HKEY \_ \_ computer locale \\ software \\ Microsoft \\ RPC
-   \_ \\ \* \\ Classi software per utenti \\ HKEY
-   \_Classi di utenti HKEY \\ \* \_

In realtà, questo fornisce lo stesso comportamento di reflection, dal momento che le modifiche apportate a queste chiavi sono immediatamente disponibili per le applicazioni a 32 bit e a 64 bit.

Le chiavi riflesse in modo condizionale rimangono separate:

-   HKEY \_ \_ classi software del computer locale \\ \\ \\ CLSID
-   \_Interfaccia delle \_ \\ classi software \\ del computer locale HKEY \\
-   \_ \\ \* \\ Classi software utenti \\ HKEY \\ CLSID
-   \_ \\ \* \\ \\ Interfaccia classi software \\ utenti HKEY
-   \_Classi di utenti HKEY \\ \* \_ \\ CLSID
-   \_ \\ \* \_ Interfaccia classi utenti \\ HKEY

Vengono utilizzati per tenere i dati che non devono essere condivisi tra applicazioni a 32 bit e a 64 bit.

## <a name="manifestation"></a>Manifestazione

Il CLSID e le chiavi di interfaccia dall'elenco precedente non vengono più riflesse mentre vengono ancora reindirizzati. Sebbene questo sia il comportamento desiderato nella maggior parte dei casi, è possibile che le applicazioni possano assumere una dipendenza dal comportamento riflesso in vista.

Le funzioni che consentono alle applicazioni di controllare la reflection (RegDisableReflectionKey e RegEnableReflectionKey) non sono Ops in Windows 7.

## <a name="mitigation-of-impact"></a>Attenuazione dell'effetto

COM è il principale consumatore della reflection del registro di sistema. COM e altri consumer sono stati aggiornati per adattarsi a questa modifica. Questa modifica non influisce sulle applicazioni che utilizzano API COM standard.

## <a name="solution"></a>Soluzione

Applicare una delle opzioni seguenti se si basa la reflection del registro di sistema per sincronizzare le visualizzazioni a 32 bit e a 64 bit:

-   Crea chiavi in entrambe le visualizzazioni in modo esplicito durante l'installazione
-   Spostare le chiavi dall'ambito delle chiavi riflesse
-   Controllare entrambe le visualizzazioni del registro di sistema quando si esegue una query per una chiave riflessa

    **Nota:** \_ \_ \_ \_ Impossibile combinare i flag 64KEY di WOW64 32KEY e Key WOW64

Applicare una delle opzioni seguenti se si basano sulle funzioni RegDisableReflectionKey per disabilitare la reflection del registro di sistema:

-   Crea chiavi in entrambe le visualizzazioni in modo esplicito durante l'installazione
-   Spostare le chiavi dall'ambito delle chiavi riflesse
-   Usare sottochiavi specifiche della piattaforma (ad esempio x86, amd64 e ia64) per separare i dati specifici di bit

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Articolo di reflection del registro di sistema](../winprog64/registry-reflection.md)
-   [Elenco delle chiavi reindirizzate nell'articolo redirector del registro di sistema](../winprog64/registry-redirector.md)
-   [Procedure consigliate per WOW64](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)

> [!Note]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi/aree geografiche.

 

 

 
