---
description: L'applicazione di patch a Controllo dell'account utente consente agli autori delle installazioni del programma di installazione di Windows di identificare le patch con firma digitale che possono essere applicate in futuro da utenti non amministratori.
ms.assetid: f7d64f61-24c8-4037-a10b-d68d0e9e3c42
title: Applicazione di patch a Controllo dell'account utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 689da3d09541199d6ff231e4f6ce909d7342025ab443d79e4db47aee9deb2733
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012809"
---
# <a name="user-account-control-uac-patching"></a>Applicazione di patch a Controllo dell'account utente

[*L'applicazione*](u-gly.md) di patch a Controllo dell'account utente consente agli autori delle installazioni del programma di installazione di Windows di identificare le patch con firma digitale che possono essere applicate in futuro da utenti non amministratori.

Se la firma digitale non corrisponde al certificato, Windows Vista visualizza una finestra di dialogo di controllo dell'account utente che richiede l'autorizzazione dell'amministratore prima di installare la patch. Nei sistemi precedenti a Windows Vista, il programma di installazione non applierà una patch firmata che non corrisponde al certificato.

Se un utente non amministratore tenta di applicare una patch a un'applicazione e non sono state soddisfatte le condizioni seguenti, Windows Vista invierà una notifica all'utente che è necessaria l'autorizzazione dell'amministratore prima di installare la patch. Un utente non amministratore può continuare a installare la patch, senza dover ottenere autorizzazioni di amministratore aggiuntive, purché siano soddisfatte le condizioni seguenti.

-   L'applicazione è stata installata Windows Vista o Windows XP usando Windows Installer 3.0 o versione successiva.

    **Windows Server 2008:** Non supportato.

-   Se l'applicazione è stata installata in Windows XP, l'applicazione deve essere stata installata anche da supporti rimovibili, ad esempio un disco CD-ROM o DVD. Questa restrizione non si applica se l'applicazione è stata installata in Windows Vista.
-   L'applicazione non è stata installata da [un'immagine di origine dell'installazione](administrative-installation.md) amministrativa.
-   L'applicazione è stata installata in origine per computer. Per informazioni su come consentire agli utenti non amministratori di applicare patch alle applicazioni gestite per utente dopo che la patch è stata approvata come attendibile da un amministratore, vedere Applicazione di patch [Per-User applicazioni gestite.](patching-per-user-managed-applications.md)
-   La [tabella MsiPatchCertificate è](msipatchcertificate-table.md) presente nel pacchetto windows installer (file .msi) e contiene le informazioni necessarie per abilitare controllo dell'account utente. La tabella e le informazioni potrebbero essere state incluse nel pacchetto di installazione originale o aggiunte al pacchetto da un file di patch Windows Installer (file msp).
-   Le patch sono firmate digitalmente da un certificato elencato nella [tabella MsiPatchCertificate](msipatchcertificate-table.md). Per altre informazioni sui certificati di firma digitale, vedere [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).
-   La firma digitale nel pacchetto patch può essere verificata rispetto al certificato nella [tabella MsiPatchCertificate](msipatchcertificate-table.md). Per altre informazioni sull'uso di firme digitali, certificati digitali e [](https://msdn.microsoft.com/library/cc527452.aspx) [**WinVerifyTrust,**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)vedere la sezione Sicurezza di Microsoft Windows Software Development Kit (SDK).
-   Il certificato del firmatario usato per verificare la firma digitale nel pacchetto di patch è valido e non è stato revocato.
    > [!Note]  
    > Anche se non è possibile firmare una patch utilizzando un certificato scaduto, la valutazione di una firma digitale su una patch non ha esito negativo se il certificato è scaduto. La valutazione usa la tabella [MsiPatchCertificate](msipatchcertificate-table.md)corrente, costituita dalla tabella MsiPatchCertificate nel pacchetto originale e da eventuali modifiche apportate alla tabella da patch sequenziate prima di quella corrente. Una patch può aggiungere nuovi certificati alla tabella MsiPatchCertificate per valutare le patch sequenziate dopo la patch corrente. Un certificato revocato viene sempre rifiutato.

     

-   L'applicazione di patch con privilegi minimi non è stata disabilitata impostando la proprietà [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) o il [criterio DisableLUAPatching.](disableluapatching.md)

Una patch applicata tramite l'applicazione di patch di Controllo dell'account utente può essere rimossa anche da un utente non amministratore.

Gli amministratori possono applicare patch ai prodotti installati per computer indipendentemente dall'impostazione di Controllo dell'account utente dell'applicazione.

È possibile determinare se l'applicazione di patch con privilegi minimi è abilitata per un'applicazione usando la funzione [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) per eseguire una query per la proprietà INSTALLPROPERTY AUTHORIZED LUA APP oppure usando il metodo ProductInfo per eseguire una query per la proprietà \_ \_ \_ "AuthorizedLUAApp". [](installer-productinfo.md) Se il valore di una delle due proprietà è 1, l'applicazione è abilitata per l'applicazione di patch all'account utente con privilegi minimi.

Un amministratore può disabilitare l'applicazione di patch con privilegi minimi nel computer impostando il [criterio DisableLUAPatching](disableluapatching.md) su 1. È possibile impostare la [**proprietà MSIDISABLELUAPATCHING**](msidisableluapatching.md) su 1 durante l'installazione iniziale di un'applicazione per impedire l'applicazione di patch con privilegi minimi solo per tale applicazione.

Questa funzionalità è disponibile a partire da Windows Installer versione 3.0. L'applicazione di patch di Controllo dell'account utente è stata definita applicazione di patch per gli account utente con privilegi minimi (LUA) in Windows XP. L'applicazione di patch LUA non è disponibile Windows 2000 e Windows Server 2003.

Per altre informazioni sulla compatibilità delle applicazioni e sullo sviluppo di applicazioni compatibili con Controllo dell'account utente, vedere le informazioni sul controllo dell'account utente disponibili in [Microsoft Technet.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10))

 

 
