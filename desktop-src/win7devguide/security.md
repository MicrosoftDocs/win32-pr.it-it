---
title: Sicurezza (Windows 7 Developer Guide)
description: Windows 7 include funzionalità di sicurezza nuove e migliorate che semplificano il miglioramento, l'uso e la gestione della sicurezza delle applicazioni da parte degli sviluppatori.
ms.assetid: c3f19338-8ada-4ded-82a9-ca0869ad469d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c421256c23042ad1ea4bad57a616047e43276449bd93f771543d4eb41286c7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329741"
---
# <a name="security-windows-7-developer-guide"></a>Sicurezza (Windows 7 Developer Guide)

Windows 7 include funzionalità di sicurezza nuove e migliorate che semplificano il miglioramento, l'uso e la gestione della sicurezza delle applicazioni da parte degli sviluppatori. Include un'ampia gamma di nuove funzionalità di sicurezza che non solo consentono di proteggersi dalle minacce, ma limitano anche i danni che gli utenti malintenzionati possono fare se ottengono l'accesso a un computer.

I miglioramenti apportati alla Windows di filtro delle applicazioni consentono agli sviluppatori di creare applicazioni che interagiscono con l'elaborazione dei pacchetti nello stack di rete del sistema operativo. È possibile filtrare e modificare i dati di rete prima che raggiungano la destinazione.

Inoltre, a causa delle modifiche apportate al modello Windows privilegi, la sicurezza del sistema è più gestibile sia dagli sviluppatori che dagli utenti finali. I nuovi miglioramenti semplificano l'identificazione delle richieste critiche per garantire che gli utenti possano accedere alle applicazioni e alle funzionalità necessarie senza compromettere i sistemi. (Vedere [il Centro per sviluppatori msdn sulla sicurezza).](https://msdn.microsoft.com/security/default.aspx)

## <a name="windows-filtering-platform"></a>Piattaforma filtro Windows

In Windows 7, la piattaforma di Windows è stata migliorata per offrire agli sviluppatori un maggiore controllo sulle funzionalità del firewall. Il livello di filtro è stato aumentato e *gli ISV* possono ora collegare protezione e rilevamento personalizzati a livelli inferiori. Inoltre, gli sviluppatori di firewall possono attivare o disattivare in modo selettivo parti Windows firewall.

Usando Windows di filtro, gli sviluppatori possono creare firewall, sistemi di rilevamento delle intrusioni, programmi antivirus, strumenti di monitoraggio di rete e controlli genitori nelle applicazioni. Windows Piattaforma di filtro si integra con e fornisce il supporto per un'ampia gamma di funzionalità del firewall, tra cui la comunicazione autenticata e la configurazione dinamica del firewall in base all'uso da parte delle applicazioni dell'API socket (criteri basati sull'applicazione). Windows La piattaforma di filtro fornisce anche l'infrastruttura per la gestione dei criteri, le notifiche di modifica, la diagnostica di rete e i filtri con stato.

L'architettura iniziale di Windows filtering platform in Windows Vista ha fornito funzionalità per il traffico basato su IP. Anche altri protocolli non IP, ad esempio ARP (Address Resolution Protocol) e i protocolli a livello *mac (Media* Access Control) per la gestione e l'autenticazione di rete, richiedono l'applicazione di filtri, l'ispezione o la registrazione. In Windows 7 è stato fornito un livello di ispezione *NDIS* che supporta i filtri *MAC* ed *ETHERNET* per soddisfare questa esigenza. (Vedere [Windows Filtering Platform.](../fwp/windows-filtering-platform-start-page.md)

## <a name="user-account-control"></a>Controllo dell'account utente

Controllo dell'account utente è un componente di sicurezza di Windows 7 che consente agli sviluppatori di compilare applicazioni che consentono agli utenti di eseguire attività comuni come utenti non amministratori. Gli sviluppatori possono ridurre i rischi per la sicurezza eseguendo applicazioni con un token utente standard, riducendo i rischi di errori o attacchi.

Gli account utente membri del gruppo *Administrators* locale eseguiranno la maggior parte delle applicazioni come utente standard. Separando le funzioni utente e amministratore abilitando al tempo stesso la produttività, Controllo dell'account utente offre agli sviluppatori un maggiore controllo sul livello di accesso degli utenti sulle aree protette di un'applicazione. Controllo dell'account utente richiede le credenziali in modalità *Desktop* protetto, in cui l'intero schermo è protetto per impedire lo spoofing dell'interfaccia utente o del mouse. Vedere Aggiornamenti [della finestra di dialogo Controllo account utente](../win7appqual/user-interface---user-account-control-dialog-updates.md) e Controllo [dell'account utente e WMI.](../wmisdk/user-account-control-and-wmi.md)

 

 
