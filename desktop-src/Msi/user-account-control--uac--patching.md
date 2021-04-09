---
description: Il controllo dell'account utente (UAC) consente agli autori di Windows Installer installazioni di identificare patch firmate digitalmente che possono essere applicate in futuro da utenti non amministratori.
ms.assetid: f7d64f61-24c8-4037-a10b-d68d0e9e3c42
title: Applicazione di patch al controllo dell'account utente (UAC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d111a39245ab15b24c1734d278a8e0a477e68a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885477"
---
# <a name="user-account-control-uac-patching"></a>Applicazione di patch al controllo dell'account utente (UAC)

Il [*controllo dell'account utente*](u-gly.md) (UAC) consente agli autori di Windows Installer installazioni di identificare patch firmate digitalmente che possono essere applicate in futuro da utenti non amministratori.

Se la firma digitale non corrisponde al certificato, Windows Vista Visualizza una finestra di dialogo del controllo dell'account utente che richiede l'autorizzazione di amministratore prima di installare la patch. Nei sistemi precedenti a Windows Vista, tramite il programma di installazione non viene applicata una patch firmata che non corrisponde al certificato.

Se un utente non amministratore tenta di applicare una patch a un'applicazione e non sono state soddisfatte le condizioni seguenti, Windows Vista invierà una notifica all'utente che è necessaria l'autorizzazione di amministratore prima di installare la patch. Un non amministratore può continuare l'installazione della patch, senza la necessità di ottenere ulteriori autorizzazioni di amministratore, purché siano soddisfatte le condizioni seguenti.

-   L'applicazione è stata installata in Windows Vista o Windows XP utilizzando Windows Installer 3,0 o versione successiva.

    **Windows Server 2008:** Non supportato.

-   Se l'applicazione è stata installata in Windows XP, l'applicazione deve essere installata anche da un supporto rimovibile, ad esempio un disco CD-ROM o DVD. Questa restrizione non è applicabile se l'applicazione è stata installata in Windows Vista.
-   L'applicazione non è stata installata da un'immagine di origine dell' [installazione amministrativa](administrative-installation.md) .
-   L'applicazione è stata originariamente installata per computer. Per informazioni su come consentire agli utenti non amministratori di applicare patch alle applicazioni gestite per ogni utente dopo che la patch è stata approvata come attendibile da un amministratore, vedere [applicazione di patch a Per-User applicazioni gestite](patching-per-user-managed-applications.md).
-   La [tabella MsiPatchCertificate](msipatchcertificate-table.md) è presente nel pacchetto di Windows Installer (file con estensione msi) e contiene le informazioni necessarie per abilitare il controllo dell'account utente. È possibile che la tabella e le informazioni siano state incluse nel pacchetto di installazione originale o aggiunte al pacchetto da un file di patch Windows Installer (file con estensione msp).
-   Le patch sono firmate digitalmente da un certificato elencato nella [tabella MsiPatchCertificate](msipatchcertificate-table.md). Per ulteriori informazioni sui certificati di firma digitale, vedere [firme digitali e Windows Installer](digital-signatures-and-windows-installer.md).
-   La firma digitale nel pacchetto di patch può essere verificata rispetto al certificato nella [tabella MsiPatchCertificate](msipatchcertificate-table.md). Per ulteriori informazioni sull'utilizzo di firme digitali, certificati digitali e [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), vedere la sezione relativa alla [sicurezza](https://msdn.microsoft.com/library/cc527452.aspx) del Software Development Kit (SDK) di Microsoft Windows.
-   Il certificato del firmatario usato per verificare la firma digitale nel pacchetto di patch è valido e non è stato revocato.
    > [!Note]  
    > Sebbene non sia possibile firmare una patch usando un certificato scaduto, la valutazione di una firma digitale in una patch non ha esito negativo se il certificato è scaduto. La valutazione utilizza la [tabella MsiPatchCertificate](msipatchcertificate-table.md)corrente, che è costituita dalla tabella MsiPatchCertificate nel pacchetto originale e dalle patch sequenziate prima della tabella corrente. Una patch può aggiungere nuovi certificati alla tabella MsiPatchCertificate per valutare le patch sequenziate dopo la patch corrente. Un certificato revocato viene sempre rifiutato.

     

-   L'applicazione di patch con privilegi minimi non è stata disabilitata impostando la proprietà [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) o il criterio [DisableLUAPatching](disableluapatching.md) .

Una patch applicata con l'applicazione di patch del controllo dell'account utente può essere rimossa anche da un utente non amministratore.

Gli amministratori possono applicare patch ai prodotti installati per computer indipendentemente dall'impostazione del controllo dell'account utente dell'applicazione.

È possibile determinare se l'applicazione di patch con privilegi minimi è abilitata per un'applicazione usando la funzione [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) per eseguire una query per la proprietà INSTALLPROPERTY dell' \_ \_ app Lua autorizzata \_ o usando il metodo [**ProductInfo**](installer-productinfo.md) per eseguire una query per la proprietà "AuthorizedLUAApp". Se il valore di una delle due proprietà è 1, l'applicazione è abilitata per l'applicazione di patch a un account utente con privilegi minimi.

Un amministratore può disabilitare l'applicazione di patch con privilegi minimi nel computer impostando il criterio [DisableLUAPatching](disableluapatching.md) su 1. È possibile impostare la proprietà [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) su 1 durante l'installazione iniziale di un'applicazione per evitare l'applicazione di patch con privilegi minimi solo per tale applicazione.

Questa funzionalità è disponibile a partire dalla versione Windows Installer 3,0. L'applicazione di patch a controllo dell'account utente (UAC) è stata chiamata applicazione di patch con privilegi minimi in Windows XP. L'applicazione di patch LUA non è disponibile in Windows 2000 e Windows Server 2003.

Per ulteriori informazioni sulla compatibilità delle applicazioni e sullo sviluppo di applicazioni compatibili con controllo dell'account utente, vedere le informazioni sull'UAC fornite in [Microsoft TechNet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)).

 

 
