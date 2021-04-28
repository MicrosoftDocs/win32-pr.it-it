---
description: Rimozione della reflection del Registro di sistema di Windows
ms.assetid: 4b42d44d-cde8-4d96-96c5-24b7ab7e4cec
title: Rimozione della reflection del Registro di sistema di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeab0109cbbac988c89d6add91fa899cea9169ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116259"
---
# <a name="removal-of-windows-registry-reflection"></a>Rimozione della reflection del Registro di sistema di Windows

## <a name="platform"></a>Piattaforma

**Client** - Windows 7  
**Server** - Windows Server 2008 R2  









## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità** - Bassa  
**Frequenza** - Bassa  





## <a name="description"></a>Descrizione

Il processo di reflection del Registro di sistema copia le chiavi e i valori del Registro di sistema tra due viste del Registro di sistema per mantenerle sincronizzate. Nelle installazioni precedenti a 64 bit di Windows, il processo rifletteva un subset delle chiavi del Registro di sistema reindirizzate tra le visualizzazioni a 32 bit e a 64 bit. Tuttavia, l'implementazione di questo ha causato alcune incoerenze nello stato del Registro di sistema. Per informazioni dettagliate sulla reflection del Registro di sistema, vedere l'articolo MSDN corrispondente *nella sezione Collegamenti* ad altre risorse riportata di seguito.

A partire da Windows 7, è stata rimossa completamente la reflection del Registro di sistema ed è stato unito il merge delle chiavi che si riflettevano:

-   Classi software \_ HKEY LOCAL \_ MACHINE \\ \\
-   HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ COM3
-   HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ EventSystem
-   HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Ole
-   HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Rpc
-   Classi software HKEY \_ USERS \\ \* \\ \\
-   Classi HKEY \_ USERS \\ \* \_

In effetti, ciò offre lo stesso comportamento di reflection, poiché le modifiche a queste chiavi sono immediatamente disponibili per le applicazioni a 32 bit e a 64 bit.

Le chiavi riflesse in modo condizionale rimangono suddivise:

-   HKEY \_ LOCAL \_ MACHINE \\ Software \\ Classes \\ CLSID
-   Interfaccia delle classi software HKEY \_ LOCAL \_ MACHINE \\ \\ \\
-   HKEY \_ USERS - Classi software \\ \* \\ \\ \\ CLSID
-   Interfaccia delle \_ classi \\ \* \\ software \\ \\ HKEY USERS
-   HKEY \_ USERS \\ \* \_ Classes \\ CLSID
-   Interfaccia delle classi HKEY \_ USERS \\ \* \_ \\

Vengono usati per mantenere i dati che non devono essere condivisi tra le applicazioni a 32 bit e a 64 bit.

## <a name="manifestation"></a>Manifestazione

Le chiavi CLSID e Interface dell'elenco precedente non vengono più riflesse mentre sono ancora reindirizzate. Anche se si tratta del comportamento desiderato nella maggior parte dei casi, è possibile che le applicazioni prendano una dipendenza dal comportamento riflessa in Vista.

Le funzioni che consentono alle applicazioni di controllare la reflection (RegDisableReflectionKey e RegEnableReflectionKey) non sono operazioni in Windows 7.

## <a name="mitigation-of-impact"></a>Mitigazione dell'impatto

COM è il principale consumer della reflection del Registro di sistema. COM e altri consumer sono stati aggiornati per supportare questa modifica. Questa modifica non influisce sulle applicazioni che usano API COM standard.

## <a name="solution"></a>Soluzione

Applicare una delle opzioni seguenti se si fa affidamento sulla reflection del Registro di sistema per sincronizzare le visualizzazioni a 32 bit e a 64 bit:

-   Creare chiavi in entrambe le visualizzazioni in modo esplicito durante l'installazione
-   Spostare le chiavi all'esterno dell'ambito delle chiavi riflesse
-   Controllare entrambe le viste del Registro di sistema durante l'esecuzione di query per una chiave riflessa

    **Nota:** I \_ flag KEY WOW64 \_ 32KEY e KEY \_ WOW64 \_ 64KEY non possono essere combinati

Applicare una delle opzioni seguenti se si fa affidamento sulle funzioni RegDisableReflectionKey per disabilitare la reflection del Registro di sistema:

-   Creare le chiavi in entrambe le viste in modo esplicito durante l'installazione
-   Spostare le chiavi all'esterno dell'ambito delle chiavi riflesse
-   Usare sottochiavi specifiche della piattaforma (ad esempio x86, amd64 e ia64) per separare i dati specifici del bitness

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Articolo sulla reflection del Registro di sistema](../winprog64/registry-reflection.md)
-   [Elenco di chiavi reindirizzate all'interno dell'articolo Redirector del Registro di sistema](../winprog64/registry-redirector.md)
-   [Procedure consigliate per Wow64](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)

> [!Note]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi/aree geografiche.

 

 

 
