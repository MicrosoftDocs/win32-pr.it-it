---
title: Piattaforma filtro Windows
description: Windows Piattaforma filtro (WFP) è un set di servizi API e di sistema che forniscono una piattaforma per la creazione di applicazioni di filtro di rete.
ms.assetid: 0436f559-20e6-4199-8391-10eb7d85df23
keywords:
- Piattaforma filtro Windows
- Windows Pagina iniziale della piattaforma di filtro, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c1f0e412426dd2bae7e5861d3b328d4e285c303aef046970e725a02965b974
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766491"
---
# <a name="windows-filtering-platform"></a>Piattaforma filtro Windows

## <a name="purpose"></a>Scopo

Windows Piattaforma filtro (WFP) è un set di servizi API e di sistema che forniscono una piattaforma per la creazione di applicazioni di filtro di rete. L'API di Piattaforma filtro Windows consente agli sviluppatori di scrivere codice che interagisce con l'elaborazione dei pacchetti che si verifica a diversi livelli nello stack di rete del sistema operativo. È possibile filtrare e modificare i dati di rete prima che raggiungano la destinazione.

Fornendo una piattaforma di sviluppo più semplice, WFP è progettato per sostituire le tecnologie di filtro pacchetti precedenti, ad esempio i filtri Transport Driver Interface (TDI), i filtri NDIS (Network Driver Interface Specification) e i provider di servizi a più livelli (LSP) Winsock. A partire da Windows Server 2008 e Windows Vista, l'hook del firewall e i driver dell'hook del filtro non sono disponibili; Le applicazioni che usavano questi driver devono invece usare WFP.

Con l'API WFP, gli sviluppatori possono implementare firewall, sistemi di rilevamento delle intrusioni, programmi antivirus, strumenti di monitoraggio di rete e controllo genitori. WFP si integra con e fornisce il supporto per le funzionalità del firewall, ad esempio la comunicazione autenticata e la configurazione dinamica del firewall in base all'uso dell'API sockets da parte delle applicazioni (criteri basati su applicazioni). IL WFP fornisce anche l'infrastruttura per la gestione dei criteri IPsec, le notifiche delle modifiche, la diagnostica di rete e il filtro con stato.

Windows La piattaforma di filtro è una piattaforma di sviluppo e non un firewall stesso. L'applicazione firewall incorporata in Windows Vista, Windows Server 2008 e sistemi operativi successivi Windows Firewall con sicurezza avanzata (WFAS) viene implementata tramite WFP. Pertanto, le applicazioni sviluppate con l'API WFP o [L'API WFAS](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) usano la logica di arbitraggio dei filtri comune incorporata in WFP.

L'API WFP è costituita da un'API in modalità utente e da un'API in modalità kernel. Questa sezione offre una panoramica dell'intero WFP e descrive in dettaglio solo la parte in modalità utente dell'API WFP. Per una descrizione dettagliata dell'API WFP in modalità kernel, vedere la Guida online [di Windows Driver Kit.](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)

## <a name="developer-audience"></a>Sviluppatori

L'API Windows Filtering Platform è progettata per l'uso da parte dei programmatori che usano software di sviluppo C/C++. I programmatori devono avere familiarità con i concetti di rete e la progettazione di sistemi che usano componenti in modalità utente e kernel.

## <a name="run-time-requirements"></a>Requisiti di runtime

La Windows Filtering Platform è supportata nei client che eseguono Windows Vista e versioni successive e nei server che eseguono Windows Server 2008 e versioni successive. Per informazioni sui requisiti di run-time per un elemento di programmazione specifico, vedere la sezione Requisiti della pagina di riferimento per tale elemento.





 

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                               | Descrizione                                                                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Novità di Windows Filtering Platform](what-s-new-in-windows-filtering-platform.md)<br/> | Informazioni sulle nuove funzionalità e API in Windows Filtering Platform.<br/>                    |
| [Informazioni Windows filtering platform](about-windows-filtering-platform.md)<br/>                 | Panoramica di Windows Filtering Platform.<br/>                                             |
| [Uso della Windows di filtro](using-windows-filtering-platform.md)<br/>                 | Codice di esempio con l'API Windows Filtering Platform. <br/>                                |
| [Windows Informazioni di riferimento sulle API della piattaforma di filtro](fwp-reference.md)<br/>                            | Documentazione per le Windows, le strutture e le costanti della piattaforma di filtro.<br/> |



 

## <a name="additional-resources"></a>Risorse aggiuntive

Per porre domande e discutere sull'uso dell'API WFP, visitare il forum Windows [Filtering Platform](https://social.msdn.microsoft.com/forums/wfp/threads/).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Api della piattaforma Windows kernel -Guida alla progettazione](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[API della piattaforma Windows kernel-mode - Informazioni di riferimento](/windows-hardware/drivers/ddi/_netvista/)
</dt> <dt>

[Windows Firewall con sicurezza avanzata](/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page)
</dt> <dt>

[Classe helper estendibile diagnostica WFP](/windows/desktop/NDF/windows-filtering-platform-extensible-helper-class)
</dt> <dt>

[Estensioni secure socket Winsock](/windows/desktop/WinSock/winsock-secure-socket-extensions)
</dt> </dl>

 

