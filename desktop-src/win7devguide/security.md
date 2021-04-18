---
title: Sicurezza (Guida per sviluppatori di Windows 7)
description: Windows 7 include funzionalità di sicurezza nuove e migliorate che consentono agli sviluppatori di migliorare, utilizzare e gestire la sicurezza delle proprie applicazioni.
ms.assetid: c3f19338-8ada-4ded-82a9-ca0869ad469d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a3b317f2fe0c7d42559245108bae6a5dbf0e6f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300751"
---
# <a name="security-windows-7-developer-guide"></a>Sicurezza (Guida per sviluppatori di Windows 7)

Windows 7 include funzionalità di sicurezza nuove e migliorate che consentono agli sviluppatori di migliorare, utilizzare e gestire la sicurezza delle proprie applicazioni. Include una serie di nuove funzionalità di sicurezza che non solo consentono di proteggersi dalle minacce, ma anche di limitare il danno che gli utenti malintenzionati possono eseguire se ottengono l'accesso a un computer.

I miglioramenti apportati alla piattaforma filtro Windows consentono agli sviluppatori di creare applicazioni che interagiscono con l'elaborazione dei pacchetti nello stack di rete del sistema operativo. È possibile filtrare e modificare i dati di rete prima che raggiungano la destinazione.

Inoltre, a causa delle modifiche apportate al modello di privilegi Windows, la sicurezza del sistema è più gestibile dagli sviluppatori e dagli utenti finali. I nuovi miglioramenti rendono più semplice identificare le richieste critiche per garantire che gli utenti possano accedere alle applicazioni e alle funzionalità necessarie senza compromettere i sistemi. Vedere [MSDN Security Developer Center](https://msdn.microsoft.com/security/default.aspx).

## <a name="windows-filtering-platform"></a>Piattaforma filtro Windows

In Windows 7, la piattaforma filtro Windows è stata migliorata per offrire agli sviluppatori maggiore controllo sulle funzionalità del firewall. Il livello di filtro è stato aumentato e gli *ISV* possono ora collegare la protezione e il rilevamento personalizzati a livelli inferiori. Inoltre, gli sviluppatori di firewall possono attivare o disattivare selettivamente parti del Windows Firewall.

Grazie alla piattaforma filtro Windows, gli sviluppatori possono creare firewall, sistemi di rilevamento delle intrusioni, programmi antivirus, strumenti di monitoraggio della rete e controlli padre nelle applicazioni. Windows Filtering Platform si integra con e fornisce il supporto per un'ampia gamma di funzionalità firewall, tra cui la comunicazione autenticata e la configurazione dinamica del firewall basata sull'utilizzo delle applicazioni dell'API Sockets (criteri basati su applicazioni). Windows Filtering Platform fornisce anche l'infrastruttura per la gestione dei criteri, le notifiche delle modifiche, la diagnostica di rete e i filtri con stato.

L'architettura iniziale della piattaforma filtro Windows in Windows Vista ha fornito funzionalità per il traffico basato su IP. Altri protocolli non IP, ad esempio i protocolli di livello Address Resolution Protocol (ARP) e Media Access Control (*Mac*) per la gestione della rete e l'autenticazione, richiedono anche filtri, ispezioni o registrazioni. In Windows 7 è stato fornito un livello di ispezione *NDIS* che supporta il filtro *Mac* e *Ethernet* per soddisfare questa esigenza. (Vedere [piattaforma filtro Windows](../fwp/windows-filtering-platform-start-page.md)).

## <a name="user-account-control"></a>Controllo dell'account utente

Il controllo dell'account utente è un componente di sicurezza di Windows 7 che consente agli sviluppatori di creare applicazioni che consentono agli utenti di eseguire attività comuni come utenti non amministratori. Gli sviluppatori possono ridurre i rischi per la sicurezza eseguendo le applicazioni con un token utente standard, riducendo i rischi di errori o attacchi.

Gli account utente che sono membri del gruppo *Administrators* locale eseguiranno la maggior parte delle applicazioni come utente standard. Se si separano le funzioni utente e amministratore durante l'abilitazione della produttività, UAC offre agli sviluppatori un maggiore controllo sul livello di accesso degli utenti su aree protette di un'applicazione. Il controllo dell'account utente richiede le credenziali in modalità *desktop protetto* , in cui l'intera schermata è protetta per impedire lo spoofing dell'interfaccia utente o del mouse. Vedere [gli aggiornamenti della finestra di dialogo controllo dell'account utente](../win7appqual/user-interface---user-account-control-dialog-updates.md) e il [controllo dell'account utente e WMI](../wmisdk/user-account-control-and-wmi.md).

 

 
