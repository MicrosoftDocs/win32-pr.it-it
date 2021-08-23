---
description: Servizi Desktop remoto (Windows 7 e Windows Server 2008 R2 Application Quality)
ms.assetid: 94ac6a91-1e00-45f3-9374-3ac48ac63765
title: Servizi Desktop remoto (Windows 7 e Windows Server 2008 R2 Application Quality)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10af070d54dceebe51f9872b3b58c42467040d5ad8f24f593774576b159cbbf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645741"
---
# <a name="remote-desktop-services-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Servizi Desktop remoto (Windows 7 e Windows Server 2008 R2 Application Quality)

## <a name="affected-platforms"></a>Piattaforme interessate

**Server** : Windows Server 2008 \| Windows Server 2008 R2  

## <a name="description"></a>Descrizione

Servizi Desktop remoto (precedentemente noto come Servizi terminal) consente a più utenti simultanei di accedere Windows Server per fornire servizi di hosting di applicazioni e dati usando la tecnologia Microsoft "Presentation Virtualization".

Mentre la maggior parte delle applicazioni a 32 bit e a 64 bit viene eseguita così come è in Windows Servizi Desktop remoto, molte altre non vengono eseguite come previsto a causa della differenza nella piattaforma (ambiente multi-utente, accesso simultaneo da parte di più utenti e così via).

Per altre informazioni sulla qualità dell'applicazione, vedere *La conformità delle applicazioni per Servizi terminal* white paper. Visitare la pagina Servizi Desktop remoto del prodotto e i siti Web TechNet di TS per altre informazioni Servizi Desktop remoto. Per altre informazioni sullo sviluppo di applicazioni per Servizi Desktop remoto, vedere Linee guida per la programmazione *di Servizi terminal.* Queste risorse potrebbero non essere disponibili in alcune lingue e paesi/aree geografiche.

## <a name="manifestation-of-impacts-and-their-mitigations"></a>Riduzione degli effetti e delle relative mitigazioni

Tre modifiche in Windows 7 influiscono sulle applicazioni in Servizi Desktop remoto:

-   Windows Server 2008 R2 è solo a 64 bit
-   Virtualizzazione IP per sessione
-   Distribuzioni basate su MSI: chiavi specifiche dell'utente

**Solo a 64 bit Windows Server 2008 R2**

Le applicazioni scritte per il server a 32 bit verranno eseguite in modalità WoW e non in modo nativo in Windows Server 2008 R2 o, di conseguenza, in Servizi Desktop remoto. Per informazioni dettagliate, vedere l'argomento Windows 7 64-Bit Only (Solo 7 a 64 bit).

*Mitigazioni solo per la versione a 64 bit Windows Server 2008 R2*

La maggior parte delle applicazioni scritte per a 32 bit continuerà a funzionare normalmente in modalità WoW. Le nuove applicazioni scritte per Windows 7 Servizi Desktop remoto devono essere sviluppate e testate per la distribuzione in piattaforme a 64 bit.

**Virtualizzazione IP**

Virtualizzazione IP di Desktop remoto consente all'utente di assegnare indirizzi IP a connessioni Desktop remoto per sessione o per programma:

-   Se si assegnano indirizzi IP per sessione, tutte le applicazioni useranno l'indirizzo IP della sessione.
-   Se si assegnano indirizzi IP in base al programma, solo le applicazioni specificate useranno l'indirizzo IP della sessione e le applicazioni rimanenti nella sessione non saranno interessate.
-   Se si assegnano indirizzi IP per più programmi, questi condivideranno un indirizzo IP di sessione.
-   Se nel computer sono disponibili più schede di rete, è necessario sceglierne anche una per Virtualizzazione IP di Desktop remoto.

*Mitigazioni per la virtualizzazione IP*

Alcuni programmi richiedono un indirizzo IP univoco per ogni istanza dell'applicazione. Prima di Windows Server 2008 R2, ogni sessione in un server Desktop remoto condivideva lo stesso indirizzo IP, causando problemi di compatibilità per queste applicazioni. Virtualizzazione IP di Desktop remoto consente l'esecuzione di queste applicazioni in Desktop remoto Server.

**Distribuzioni basate su MSI**

Microsoft Installer RDS Compatibility è una nuova funzionalità inclusa in Servizi Desktop remoto in Windows Server 2008 R2. Con Servizi Desktop remoto in Windows Server 2008 R2, le installazioni di applicazioni per utente vengono accodati da Desktop remoto Server e quindi gestite da Microsoft Installer.

In Windows Server 2008 R2 è possibile installare un programma in Desktop remoto Server esattamente come si installa il programma in un desktop locale. Assicurarsi, tuttavia, di installare il programma per tutti gli utenti e di installare tutti i componenti del programma localmente nel Desktop remoto Server.

*Mitigazioni per le distribuzioni basate su MSI*

Prima della versione Windows Server 2008 R2 di Servizi Desktop remoto, Windows supportava solo un Windows installazione del programma di installazione alla volta. Per le applicazioni che richiedevano configurazioni per utente, ad esempio Microsoft Office Word, un amministratore doveva preinstallare l'applicazione e gli sviluppatori di applicazioni dovevano testare queste applicazioni sia nel client desktop remoto che nell'host di sessione Desktop remoto. Windows La funzionalità di compatibilità rds del programma di installazione consente di identificare e installare configurazioni per utente mancanti per più utenti contemporaneamente e rende l'esperienza di installazione dell'applicazione in Desktop remoto Server simile a quella in un desktop locale.

**Windows Server 2008 R2 con il [ruolo Servizi Desktop remoto](../termserv/terminal-services-portal.md) abilitato:** Non supportato. L'installazione di più pacchetti [tramite la tabella MsiEmbeddedChainer](../msi/msiembeddedchainer-table.md) ha esito negativo [se il Servizi Desktop remoto](../termserv/terminal-services-portal.md) è abilitato.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Linee guida per la programmazione di Servizi terminal](../termserv/terminal-services-programming-guidelines.md)
-   [Servizi terminal - Servizi home page](https://www.microsoft.com/windowsserver2008/en/us/rds-product-home.aspx)
-   [Conformità delle applicazioni per Servizi terminal white paper](/collaborate/connect-redirect)

> [!Note]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi/aree geografiche.

 

 

 
