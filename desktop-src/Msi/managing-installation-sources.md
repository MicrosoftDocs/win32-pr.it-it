---
description: Gli utenti e le applicazioni con privilegi amministrativi possono recuperare e modificare le informazioni sull'elenco di reti, URL e origini multimediali per le applicazioni e le patch del programma di installazione di Windows nel sistema.
ms.assetid: e8c66bad-f594-4926-b3b4-c8b245dcfa83
title: Gestione delle origini di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e7555bc9595ba10d9ce569c15c2a8138a05348e503d86a025f0cfe1783843fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013069"
---
# <a name="managing-installation-sources"></a>Gestione delle origini di installazione

Gli utenti e le applicazioni con privilegi amministrativi possono recuperare e modificare le informazioni sull'elenco di reti, URL e origini multimediali per le applicazioni e le patch del programma di installazione di Windows nel sistema.

**Windows Installer 2.0:** Non supportato. Gli amministratori non possono leggere, riordinare o sostituire le voci nell'elenco di origine e non possono modificare o recuperare le proprietà dell'elenco di origine. È possibile gestire le origini di rete, ma non le origini URL o supporti. Gli amministratori possono gestire solo gli elenchi di origine per le applicazioni per computer o le applicazioni installate in base all'utente per l'utente corrente. Ciò impedisce agli amministratori che usano versioni precedenti Windows Installer versione 3.0 di gestire le informazioni dell'elenco di origine per tutti gli utenti del sistema.

**Windows Installer 3.0 e versioni successive:** Gli utenti e le applicazioni con privilegi di amministratore possono recuperare e modificare le informazioni dell'elenco di origine per le applicazioni del programma di installazione di Windows e le patch installate nel sistema per tutti gli utenti. Le funzioni dell'elenco di origine possono essere usate per gestire gli elenchi di origine e le proprietà dell'elenco di origine per le origini di rete, URL e supporti. Il programma di installazione può riordinare gli elenchi di origine da un processo esterno.

Gli utenti e le applicazioni con privilegi amministrativi possono leggere e modificare i tipi seguenti di informazioni sull'elenco di origine:

-   Elenchi di origine per le applicazioni e le patch installate per tutti gli utenti nel sistema.
-   Elenchi di origine per le origini patch esistenti oltre alle origini dell'applicazione.
-   Elenchi di origine per url e origini multimediali esistenti oltre alle origini di rete.
-   Proprietà dell'elenco di origine, ad esempio [**MEDIAPACKAGEPATH,**](mediapackagepath.md) [**DiskPrompt,**](diskprompt.md) **LastUsedSource,** **LastUsedType** e **PackageName.**

Le funzioni degli elenchi di origine possono limitare l'ambito degli elenchi di origine trovati specificando il contesto di installazione e il contesto utente. Esistono tre possibili contesti di installazione: per utente (non gestito), per computer e gestito per utente. Il contesto utente può essere un utente specifico o tutti gli utenti nel sistema.

Gli utenti non amministratori non possono modificare l'elenco di origine di un'istanza di un'applicazione o una patch esistente nel contesto per utente (gestito o non gestito) di un altro utente. Gli utenti non amministratori possono modificare gli elenchi di origine di un'istanza di un'applicazione o di una patch installata nei contesti seguenti:

-   Il proprio contesto per utente (non gestito).
-   Il contesto del computer, ma solo se i criteri [DisableBrowse](disablebrowse.md), [AllowLockdownBrowse](allowlockdownbrowse.md)e [AlwaysInstallElevated](alwaysinstallelevated.md) consentono di cercare un'applicazione o un'origine patch.
-   Il proprio contesto gestito per utente, ma solo se i criteri [DisableBrowse](disablebrowse.md), [AllowLockdownBrowse](allowlockdownbrowse.md)e [AlwaysInstallElevated](alwaysinstallelevated.md) consentono di cercare un'applicazione o un'origine patch.

Gli amministratori possono modificare qualsiasi elenco di origine che un utente non amministratore può modificare. Inoltre, gli amministratori e le applicazioni con privilegi amministrativi possono modificare gli elenchi di origine di un'applicazione o di una patch installata nei contesti seguenti:

-   Contesto per computer.
-   Il proprio contesto gestito per utente (non gestito) o il proprio contesto gestito per utente.
-   Contesto gestito per utente di un altro utente.

> [!Note]  
> Gli utenti e le applicazioni con privilegi amministrativi non possono modificare l'elenco di origine di un'istanza di un'applicazione o di una patch installata nel contesto per utente (non gestito) di un altro utente.

 

## <a name="managing-network-and-url-sources-for-products-and-patches"></a>Gestione delle origini di rete e URL per prodotti e patch

Usare la [**funzione MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) per aggiungere o riordinare l'elenco di origini di rete e URL per una patch o un'applicazione in un contesto specifico. Usare il *parametro dwContext* per specificare il contesto di installazione. Usare il *parametro szUserSid* per specificare il contesto utente.

Usare la [**funzione MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) per creare un elenco di origine per una patch che non è ancora stata applicata ad alcuna applicazione nel contesto specificato. Ciò può essere utile quando si registra una patch con privilegi elevati. Per altre informazioni sulla registrazione di privilegi elevati per una patch, vedere Applicazione di [patch Per-User applicazioni gestite.](patching-per-user-managed-applications.md)

Usare la [**funzione MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea) per rimuovere un'origine esistente per un'applicazione o una patch in un contesto specificato. La rimozione dell'origine corrente per un'applicazione o una patch forza il programma di installazione a cercare un'origine nell'elenco di origine alla successiva richiesta di un'origine.

Usare la [**funzione MsiSourceListEnumSources per**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) enumerare le origini nell'elenco di origine di una patch o di un'applicazione specificata.

## <a name="managing-media-sources-for-products-and-patches"></a>Gestione delle origini multimediali per prodotti e patch

Usare la [**funzione MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska) per aggiungere o aggiornare le informazioni sul disco dell'origine multimediale di un'applicazione o di una patch registrata. Ogni voce è identificata in modo univoco da un ID disco. Se il disco esiste già, viene aggiornato con i nuovi valori di etichetta di volume e richiesta del disco. Se il disco non esiste, viene creata una nuova voce del disco con i nuovi valori.

Usare la [**funzione MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska) per rimuovere un disco registrato esistente nell'origine supporto per un'applicazione o una patch in un contesto specifico.

Usare la [**funzione MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa) per enumerare un elenco di dischi registrati nell'origine supporto per un'applicazione o una patch.

## <a name="retrieval-and-modification-of-source-list-information"></a>Recupero e modifica delle informazioni dell'elenco di origine

Usare le [**funzioni MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) e [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa) per recuperare o modificare le informazioni sull'elenco di origine per un'applicazione o una patch in un contesto specifico. Usare il *parametro dwContext* per specificare il contesto di installazione. Usare il *parametro szUserSid* per specificare il contesto utente.

È possibile accedere alle proprietà dell'elenco di origine, ad esempio [**MEDIAPACKAGEPATH,**](mediapackagepath.md) [**DiskPrompt,**](diskprompt.md) **LastUsedSource,** **LastUsedType** e **PackageName.**

> [!Note]  
> La **proprietà dell'elenco di origine LastUsedType** può essere solo letta. Non può essere impostata direttamente usando la [**funzione MsiSourceListSetInfo.**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)

 

## <a name="clearing-the-complete-source-list-or-forcing-a-source-resolution"></a>Cancellazione dell'elenco di origine completo o forzatura di una risoluzione dell'origine

Usare la [**funzione MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa) per rimuovere tutte le origini esistenti di un determinato tipo di origine per l'applicazione o l'istanza di patch specificata. La registrazione della patch viene rimossa anche se la patch non viene installata da alcuna applicazione nello stesso contesto. Usare il *parametro dwContext* per specificare il contesto di installazione. Usare il *parametro szUserSid* per specificare il contesto utente.

Usare [**MsiSourceListForceResolutionEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa) per cancellare l'ultima voce di origine usata per un'applicazione o una patch nel contesto specificato. Questa funzione rimuove la registrazione della proprietà denominata **LastUsedSource.** Questa funzione non influisce sull'elenco di origine registrato. La cancellazione **della registrazione LastUsedSource** forza il programma di installazione a eseguire una risoluzione dell'origine per le origini registrate la volta successiva che richiede l'origine.

 

 



