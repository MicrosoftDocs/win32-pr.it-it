---
description: .
ms.assetid: 94ac6a91-1e00-45f3-9374-3ac48ac63765
title: Servizi Desktop remoto (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46bd39785526b11ac2e4c0ede26bbb9971aadc9a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321148"
---
# <a name="remote-desktop-services-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Servizi Desktop remoto (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)

## <a name="affected-platforms"></a>Piattaforme interessate

**Server** : windows Server 2008 \| Windows Server 2008 R2  

## <a name="description"></a>Descrizione

Servizi Desktop remoto (precedentemente noto come servizi Terminal) consente a più utenti simultanei di accedere a Windows Server per offrire servizi di hosting di applicazioni e dati utilizzando la tecnologia Microsoft "Presentation Virtualization".

Sebbene la maggior parte delle applicazioni a 32 bit e a 64 bit sia eseguita in Windows Servizi Desktop remoto, diverse altre non funzionano come previsto a causa della differenza nella piattaforma (ambiente multiutente, accesso simultaneo da parte di più utenti e così via).

Per ulteriori informazioni sulla qualità dell'applicazione, vedere la pagina relativa alla *conformità delle applicazioni per Servizi Terminal* white paper. Visitare la pagina del prodotto Servizi Desktop remoto e i siti Web TechNet di Servizi terminal ulteriori informazioni sui Servizi Desktop remoto. Per ulteriori informazioni sullo sviluppo di applicazioni per Servizi Desktop remoto, consultare le *linee guida per la programmazione di Servizi terminal*. Queste risorse potrebbero non essere disponibili in alcune lingue e paesi/aree geografiche.

## <a name="manifestation-of-impacts-and-their-mitigations"></a>Manifesto degli effetti e relative mitigazioni

Tre modifiche in Windows 7 influiscono sulle applicazioni nei Servizi Desktop remoto:

-   Windows Server 2008 R2 è solo 64 bit
-   Virtualizzazione IP per sessione
-   Distribuzioni basate su MSI-chiavi specifiche dell'utente

**Solo a 64 bit Windows Server 2008 R2**

Le applicazioni scritte per il server a 32 bit vengono eseguite in modalità WoW e non in modo nativo in Windows Server 2008 R2 o, di conseguenza, in Servizi Desktop remoto. Per informazioni dettagliate, vedere l'argomento solo Windows a 7 64 bit.

*Mitigazioni per solo Windows Server 2008 R2 a 64 bit*

La maggior parte delle applicazioni scritte per 32 bit continuerà a funzionare normalmente in modalità WoW. Tutte le nuove applicazioni scritte per Windows 7 Servizi Desktop remoto devono essere sviluppate e testate per la distribuzione su piattaforme a 64 bit.

**Virtualizzazione IP**

Virtualizzazione IP di Desktop remoto consente all'utente di assegnare gli indirizzi IP alle connessioni Desktop remoto in base a ogni sessione o a ogni programma:

-   Se si assegnano indirizzi IP per ogni singola sessione, tutte le applicazioni utilizzeranno l'indirizzo IP della sessione.
-   Se si assegnano indirizzi IP in base al programma, solo le applicazioni specificate utilizzeranno l'indirizzo IP della sessione e le applicazioni rimanenti nella sessione non saranno interessate.
-   Se si assegnano indirizzi IP per più programmi, essi condivideranno un indirizzo IP della sessione.
-   Se nel computer sono presenti più schede di rete, è necessario sceglierne una per Virtualizzazione IP di Desktop remoto.

*Mitigazioni per la virtualizzazione IP*

Alcuni programmi richiedono un indirizzo IP univoco per ogni istanza dell'applicazione. Prima di Windows Server 2008 R2, ogni sessione in un server desktop remoto condivide lo stesso indirizzo IP, causando problemi di compatibilità per queste applicazioni. Virtualizzazione IP di Desktop remoto consente l'esecuzione di queste applicazioni su un server Desktop remoto.

**Distribuzioni basate su MSI**

Microsoft Installer RDS Compatibility è una nuova funzionalità inclusa con Servizi Desktop remoto in Windows Server 2008 R2. Con Servizi Desktop remoto in Windows Server 2008 R2, le installazioni delle applicazioni per utente vengono accodate dal server di Desktop remoto e quindi gestite dal programma di installazione di Microsoft.

In Windows Server 2008 R2, è possibile installare un programma nel server Desktop remoto esattamente come si installa il programma in un desktop locale. Assicurarsi, tuttavia, di installare il programma per tutti gli utenti e installare tutti i componenti del programma localmente nel server Desktop remoto.

*Mitigazioni per le distribuzioni basate su MSI*

Prima della versione di Servizi Desktop remoto di Windows Server 2008 R2, Windows supportava solo una Windows Installer installazione alla volta. Per le applicazioni che necessitano di configurazioni per utente, ad esempio Microsoft Office Word, un amministratore necessario per pre-installare l'applicazione e gli sviluppatori di applicazioni devono testare queste applicazioni sia sul client desktop remoto che sulla host sessione Desktop remoto. Windows Installer funzionalità di compatibilità Servizi Desktop remoto consente l'identificazione e l'installazione di configurazioni per utente mancanti per più utenti contemporaneamente e rende l'esperienza di installazione dell'applicazione nel server Desktop remoto simile a quella di un desktop locale.

**Windows Server 2008 R2 con il ruolo [Servizi Desktop remoto](../termserv/terminal-services-portal.md) abilitato:** Non supportato. L'installazione di più pacchetti con la [tabella MsiEmbeddedChainer](../msi/msiembeddedchainer-table.md) ha esito negativo se il ruolo [Servizi Desktop remoto](../termserv/terminal-services-portal.md) è abilitato.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Linee guida per la programmazione di Servizi terminal](../termserv/terminal-services-programming-guidelines.md)
-   [home page del prodotto Servizi terminal](https://www.microsoft.com/windowsserver2008/en/us/rds-product-home.aspx)
-   [Preparazione delle applicazioni per Servizi terminal white paper](/collaborate/connect-redirect)

> [!Note]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi/aree geografiche.

 

 

 
