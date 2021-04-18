---
description: Gli utenti e le applicazioni con privilegi amministrativi possono recuperare e modificare le informazioni dell'elenco di origini di rete, URL e supporto per Windows Installer le applicazioni e le patch nel sistema.
ms.assetid: e8c66bad-f594-4926-b3b4-c8b245dcfa83
title: Gestione delle origini di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7fc45253af20ae5f9792ee3a5ec7dd318c80295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318278"
---
# <a name="managing-installation-sources"></a>Gestione delle origini di installazione

Gli utenti e le applicazioni con privilegi amministrativi possono recuperare e modificare le informazioni dell'elenco di origini di rete, URL e supporto per Windows Installer le applicazioni e le patch nel sistema.

**Windows Installer 2,0:** Non supportato. Gli amministratori non possono leggere, riordinare o sostituire le voci nell'elenco di origine e non possono modificare o recuperare le proprietà dell'elenco di origine. È possibile gestire le origini di rete, ma non le origini URL o multimediali. Gli amministratori possono gestire solo gli elenchi di origine per le applicazioni per computer o per le applicazioni installate come per utente per l'utente corrente. Ciò impedisce agli amministratori che usano versioni precedenti a Windows Installer versione 3,0 di gestire le informazioni dell'elenco di origine per tutti gli utenti del sistema.

**Windows Installer 3,0 e versioni successive:** Gli utenti e le applicazioni che dispongono di privilegi di amministratore possono recuperare e modificare le informazioni dell'elenco di origine per Windows Installer le applicazioni e le patch installate nel sistema per tutti gli utenti. Le funzioni elenco di origine possono essere usate per gestire elenchi di origine e proprietà dell'elenco di origine per le origini di rete, URL e supporti. Il programma di installazione può riordinare gli elenchi di origine da un processo esterno.

Gli utenti e le applicazioni che dispongono di privilegi amministrativi possono leggere e modificare i tipi seguenti di informazioni sull'elenco di origini:

-   Elenchi di origine per le applicazioni e le patch installate per tutti gli utenti del sistema.
-   Elenchi di origine per le origini patch esistenti oltre alle origini dell'applicazione.
-   Elenchi di origine per URL e origini multimediali esistenti oltre alle origini di rete.
-   Proprietà dell'elenco di origine, ad esempio [**MEDIAPACKAGEPATH**](mediapackagepath.md), [**DiskPrompt**](diskprompt.md), **LastUsedSource**, **LastUsedType** e **PackageName**.

Le funzioni degli elenchi di origine possono limitare l'ambito degli elenchi di origine trovati specificando il contesto di installazione e il contesto utente. Esistono tre possibili contesti di installazione: per utente (non gestito), per computer e gestiti per utente. Il contesto utente può essere un utente specifico o tutti gli utenti del sistema.

Gli utenti non amministratori non possono modificare l'elenco di origine di un'istanza di un'applicazione o di una patch esistente nel contesto di un altro utente (gestito o non gestito). Gli non amministratori possono modificare gli elenchi di origine di un'istanza di un'applicazione o di una patch installata con i seguenti contesti:

-   Il rispettivo contesto per utente (non gestito).
-   Il contesto del computer, ma solo se i criteri [DisableBrowse](disablebrowse.md), [AllowLockdownBrowse](allowlockdownbrowse.md)e [AlwaysInstallElevated](alwaysinstallelevated.md) consentono la ricerca di un'applicazione o di un'origine patch.
-   Il rispettivo contesto gestito per utente, ma solo se i criteri [DisableBrowse](disablebrowse.md), [AllowLockdownBrowse](allowlockdownbrowse.md)e [AlwaysInstallElevated](alwaysinstallelevated.md) consentono loro di cercare un'applicazione o un'origine patch.

Gli amministratori possono modificare qualsiasi elenco di origine che può essere modificato da un amministratore non amministratore. Inoltre, gli amministratori e le applicazioni che dispongono di privilegi amministrativi possono modificare gli elenchi di origine di un'applicazione o di una patch installata nei contesti seguenti:

-   Contesto per computer.
-   Il rispettivo per utente (non gestito) o il proprio contesto gestito per utente.
-   Contesto gestito per utente di un altro utente.

> [!Note]  
> Gli utenti e le applicazioni che dispongono di privilegi amministrativi non possono modificare l'elenco di origine di un'istanza di un'applicazione o di una patch installata nel contesto per utente (non gestito) di un altro utente.

 

## <a name="managing-network-and-url-sources-for-products-and-patches"></a>Gestione delle origini di rete e URL per prodotti e patch

Usare la funzione [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) per aggiungere o riordinare l'elenco di origine di origini di rete e URL per una patch o un'applicazione in un determinato contesto. Usare il parametro *dwContext* per specificare il contesto di installazione. Usare il parametro *szUserSid* per specificare il contesto utente.

Usare la funzione [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) per creare un elenco di origine per una patch che non è ancora stata applicata a nessuna applicazione nel contesto specificato. Questa operazione può essere utile quando si registra una patch con privilegi elevati. Per ulteriori informazioni sulla registrazione di privilegi elevati per una patch, vedere [applicazione di patch Per-User applicazioni gestite](patching-per-user-managed-applications.md).

Utilizzare la funzione [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea) per rimuovere un'origine esistente per un'applicazione o una patch in un contesto specificato. La rimozione dell'origine corrente per un'applicazione o una patch impone al programma di installazione di cercare un'origine nell'elenco di origine alla successiva richiesta di un'origine.

Utilizzare la funzione [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) per enumerare le origini nell'elenco di origine di una patch o di un'applicazione specificata.

## <a name="managing-media-sources-for-products-and-patches"></a>Gestione delle origini multimediali per prodotti e patch

Usare la funzione [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska) per aggiungere o aggiornare le informazioni sul disco dell'origine multimediale di un'applicazione o di una patch registrata. Ogni voce viene identificata in modo univoco da un ID disco. Se il disco esiste già, viene aggiornato con i valori nuovi per etichetta volume e richiesta disco. Se il disco non esiste, viene creata una nuova voce del disco con i nuovi valori.

Usare la funzione [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska) per rimuovere un disco registrato esistente nell'origine supporto per un'applicazione o una patch in un contesto specifico.

Usare la funzione [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa) per enumerare un elenco di dischi registrati nell'origine multimediale per un'applicazione o una patch.

## <a name="retrieval-and-modification-of-source-list-information"></a>Recupero e modifica delle informazioni sull'elenco di origine

Usare le funzioni [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) e [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa) per recuperare o modificare le informazioni sull'elenco di origine di un'applicazione o di una patch in un contesto specifico. Usare il parametro *dwContext* per specificare il contesto di installazione. Usare il parametro *szUserSid* per specificare il contesto utente.

È possibile accedere alle proprietà dell'elenco di origine, ad esempio [**MEDIAPACKAGEPATH**](mediapackagepath.md), [**DiskPrompt**](diskprompt.md), **LastUsedSource**, **LastUsedType** e **PackageName** .

> [!Note]  
> È possibile leggere la proprietà elenco origine **LastUsedType** . Non è possibile impostarlo direttamente tramite la funzione [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa) .

 

## <a name="clearing-the-complete-source-list-or-forcing-a-source-resolution"></a>Cancellazione dell'elenco di origine completo o forzatura di una risoluzione dell'origine

Utilizzare la funzione [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa) per rimuovere tutte le origini esistenti di un determinato tipo di origine per l'applicazione o l'istanza di patch specificata. Se la patch non è installata da alcuna applicazione nello stesso contesto, viene rimossa anche la registrazione delle patch. Usare il parametro *dwContext* per specificare il contesto di installazione. Usare il parametro *szUserSid* per specificare il contesto utente.

Usare [**MsiSourceListForceResolutionEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa) per cancellare l'ultima voce di origine usata per un'applicazione o una patch nel contesto specificato. Questa funzione rimuove la registrazione della proprietà denominata **LastUsedSource**. Questa funzione non influisce sull'elenco di origini registrate. La cancellazione della registrazione **LastUsedSource** impone al programma di installazione di eseguire una risoluzione dell'origine sulle origini registrate la volta successiva che richiede l'origine.

 

 



