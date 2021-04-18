---
description: Motore di installazione utilizzato per installare le applicazioni o gli aggiornamenti o i servizi eseguiti in Windows. Configura e ripristina le applicazioni installate. Scrivere pacchetti MSI personalizzati per creare un'installazione o un aggiornamento o un aggiornamento dell'installazione per un'applicazione.
ms.assetid: c90b8cbe-d7a1-44ad-ae65-80115bd55e4f
title: Windows Installer
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: d818a3decc7cbede527929dc3756ba2edf193421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313783"
---
# <a name="windows-installer"></a>Windows Installer

> [!NOTE]
> Questa documentazione è destinata agli sviluppatori di software che desiderano utilizzare Windows Installer per compilare pacchetti di installazione per le applicazioni. Se si sta cercando un ridistribuibile per Windows Installer 4,5 e versioni precedenti, vedere [questo articolo](windows-installer-redistributables.md). Si noti che non è disponibile alcun componente ridistribuibile per Windows Installer 5,0. Questa versione è inclusa nel sistema operativo in Windows 7, Windows Server 2008 R2 e versioni successive di client e server (incluso Windows 10).

Microsoft Windows Installer è un servizio di installazione e configurazione fornito con Windows. Il servizio del programma di installazione consente ai clienti di fornire una migliore distribuzione aziendale e fornisce un formato standard per la gestione dei componenti. Il programma di installazione consente inoltre di pubblicizzare le applicazioni e le funzionalità in base al sistema operativo. Per ulteriori informazioni, vedere [supporto della piattaforma](platform-support-of-advertisement.md)per gli annunci.

Questa documentazione descrive Windows Installer 5,0 e versioni precedenti. Non tutte le funzionalità disponibili nelle versioni successive Windows Installer sono disponibili nelle versioni precedenti. Questa documentazione non descrive le versioni precedenti a Windows Installer 2,0. È comunque possibile installare i pacchetti di installazione e le patch creati per Windows Installer 2,0 usando Windows Installer 3,0 e versioni successive.

Windows Installer 3,0 e versioni successive, può installare più patch con una singola transazione che integra lo stato di avanzamento dell'installazione, il rollback e il riavvio. Il programma di installazione può applicare le patch in un ordine specificato indipendentemente dall'ordine con cui le patch vengono fornite al sistema. L'applicazione di patch usando Windows Installer 3,0 aggiorna solo i file interessati dalla patch e può essere notevolmente più veloce rispetto alle versioni precedenti del programma di installazione. Le patch installate con Windows Installer 3,0 o versioni successive possono essere disinstallate in qualsiasi ordine per lasciare lo stato del prodotto uguale a se la patch non è mai stata installata. Gli account con privilegi di amministratore possono usare l'API di Windows Installer 3,0 e versioni successive per eseguire query e inventariare le informazioni relative a prodotto, funzionalità, componente e patch. Il programma di installazione può essere usato per leggere, modificare e sostituire gli elenchi di origine per le origini di rete, URL e supporti. Gli amministratori possono enumerare tutti i contesti utente e di installazione e gestire gli elenchi di origine da un processo esterno.

Windows Installer 4,5 e versioni successive possono installare più pacchetti di installazione usando l' [*elaborazione delle transazioni*](t-gly.md). Se non è possibile installare tutti i pacchetti nella transazione o se l'utente annulla l'installazione, il Windows Installer possibile eseguire il rollback delle modifiche e ripristinare lo stato originale del computer. Il programma di installazione garantisce che tutti i pacchetti appartenenti a una transazione con più pacchetti siano installati o che nessuno dei pacchetti sia installato.

A partire da Windows Installer 5,0, è possibile creare un pacchetto per proteggere nuovi account, [Servizi](../services/services.md)Windows, file, cartelle e chiavi del registro di sistema. Il pacchetto può specificare un descrittore di sicurezza che nega le autorizzazioni, specifica l'ereditarietà delle autorizzazioni da una risorsa padre o specifica le autorizzazioni di un nuovo account. Per informazioni, vedere [protezione delle risorse](securing-resources-.md). Il servizio Windows Installer 5,0 può enumerare tutti i componenti installati nel computer e ottenere il percorso della chiave per il componente. Per ulteriori informazioni, vedere [enumerazione dei componenti](enumerating-components-.md). [Utilizzando la configurazione dei servizi](using-services-configuration.md), i pacchetti Windows Installer 5,0 possono personalizzare i servizi in un computer. Gli sviluppatori del programma di installazione possono utilizzare Windows Installer 5,0 e la creazione di pacchetti [singoli](single-package-authoring.md) per sviluppare pacchetti di installazione singoli in grado di installare un'applicazione nel contesto di [installazione](installation-context.md)per computer o per utente.

## <a name="where-applicable"></a>Se applicabile

Windows Installer consente di installare e configurare in modo efficiente i prodotti e le applicazioni in esecuzione su Windows. Il programma di installazione offre nuove funzionalità per annunciare le funzionalità senza installarle, installare prodotti su richiesta e aggiungere personalizzazioni utente.

Windows Installer 5,0 in esecuzione in Windows Server 2012 o Windows 8 supporta l'installazione di app approvate in Windows RT. Non è possibile installare un pacchetto di Windows Installer, una patch o una trasformazione che non è stata firmata da Microsoft in Windows RT. La proprietà [**Riepilogo modello**](template-summary.md) indica la piattaforma compatibile con un database di installazione e, in questo caso, deve includere il valore per Windows RT.

Windows Installer è progettato per lo sviluppo di applicazioni di tipo desktop.

## <a name="developer-audience"></a>Sviluppatori

Questa documentazione è destinata agli sviluppatori di software che desiderano creare applicazioni che utilizzano Windows Installer. Vengono fornite informazioni generali sui pacchetti di installazione e sul servizio del programma di installazione. Contiene descrizioni complete del Application Programming Interface e degli elementi del database del programma di installazione. Questa documentazione contiene inoltre informazioni aggiuntive per gli sviluppatori che desiderano utilizzare un editor tabelle o uno strumento di creazione di pacchetti per creare o gestire un'installazione.

## <a name="run-time-requirements"></a>Requisiti di runtime

Windows Installer 5,0 è incluso in, Windows 7, Windows Server 2008 R2 e versioni successive. Non è disponibile alcun componente ridistribuibile per Windows Installer 5,0.

Le versioni precedenti alla Windows Installer 5,0 sono state rilasciate con Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP e Windows 2000. [Windows Installer i ridistribuibili](windows-installer-redistributables.md) sono disponibili per Windows Installer 4,5 e alcune versioni precedenti.

* Windows Installer 4,5 richiede Windows Server 2008, Windows Vista, Windows XP con Service Pack 2 (SP2) e versioni successive e Windows Server 2003 con Service Pack 1 (SP1) e versioni successive.

* Windows Installer 4,0 richiede Windows Vista o Windows Server 2008. Non è disponibile alcun componente ridistribuibile per l'installazione di Windows Installer 4,0 in altri sistemi operativi. Una versione aggiornata di Windows Installer 4,0, che non aggiunge nuove funzionalità, è disponibile in Windows Vista con Service Pack 1 (SP1) e Windows Server 2008.

* Windows Installer 3,1 richiede Windows Server 2003, Windows XP o Windows 2000 con Service Pack 3 (SP3).

* Windows Installer 3,0 richiede Windows Server 2003, Windows XP o Windows 2000 con SP3. Windows Installer 3,0 è incluso in Windows XP con Service Pack 2 (SP2). È disponibile come ridistribuibile per Windows 2000 Server con Service Pack 3 (SP3) e Windows 2000 Server con Service Pack 4 (SP4), Windows XP RTM e Windows XP con Service Pack 1 (SP1) e Windows Server 2003 RTM.

* Windows Installer 2,0 è incluso in Windows Server 2003 e Windows XP.

* Windows Installer 2,0 è disponibile come pacchetto per l'installazione o l'aggiornamento a Windows Installer 2,0 in Windows 2000. Questo pacchetto non deve essere usato per installare o aggiornare Windows Installer 2,0 in Windows Server 2003 e Windows XP.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                       | Descrizione                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Roadmap](roadmap-to-windows-installer-documentation.md)<br/>                        | Guida alla documentazione Windows Installer.<br/>       |
| [Overview](about-windows-installer.md)<br/>                                          | Informazioni generali sul programma di installazione.<br/>          |
| [Novità di Windows Installer](what-s-new-in-windows-installer.md)<br/>           | Elenca le aggiunte e le modifiche apportate ai Windows Installer.<br/> |
| [Riferimento](installer-function-reference.md)<br/>                                    | Documentazione delle funzioni Windows Installer.<br/>     |
| [Esempi di script di Windows Installer](windows-installer-scripting-examples.md)<br/> | Windows Installer esempi di utilizzo di script.<br/>          |



 

 

 
