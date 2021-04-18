---
title: Piattaforma filtro Windows
description: Windows Filtering Platform (WFP) è un set di servizi API e di sistema che forniscono una piattaforma per la creazione di applicazioni di filtro di rete.
ms.assetid: 0436f559-20e6-4199-8391-10eb7d85df23
keywords:
- Piattaforma filtro Windows
- Pagina iniziale della piattaforma filtro Windows, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cf63f995b44be607977dd0c70c6c91eed024e81
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "106300628"
---
# <a name="windows-filtering-platform"></a>Piattaforma filtro Windows

## <a name="purpose"></a>Scopo

Windows Filtering Platform (WFP) è un set di servizi API e di sistema che forniscono una piattaforma per la creazione di applicazioni di filtro di rete. L'API di Piattaforma filtro Windows consente agli sviluppatori di scrivere codice che interagisce con l'elaborazione dei pacchetti che si verifica a diversi livelli nello stack di rete del sistema operativo. È possibile filtrare e modificare i dati di rete prima che raggiungano la destinazione.

Grazie a una piattaforma di sviluppo più semplice, Pam è progettato per sostituire le tecnologie di filtro dei pacchetti precedenti, ad esempio i filtri Transport Driver Interface (TDI), i filtri NDIS (Network Driver Interface Specification) e i provider di servizi a più livelli Winsock (LSP). A partire da Windows Server 2008 e Windows Vista, l'hook del firewall e i driver dell'hook di filtro non sono disponibili. le applicazioni che usavano questi driver dovrebbero invece usare Pam.

Con l'API WFP gli sviluppatori possono implementare firewall, sistemi di rilevamento delle intrusioni, programmi antivirus, strumenti di monitoraggio della rete e controlli padre. Pam si integra con e fornisce il supporto per le funzionalità del firewall, ad esempio la comunicazione autenticata e la configurazione dinamica del firewall basata sull'utilizzo dell'API Sockets da parte delle applicazioni (criteri basati su applicazioni). PAM fornisce inoltre l'infrastruttura per la gestione dei criteri IPsec, le notifiche di modifica, la diagnostica di rete e i filtri con stato.

Windows Filtering Platform è una piattaforma di sviluppo e non un firewall. L'applicazione firewall incorporata nei sistemi operativi Windows Vista, Windows Server 2008 e versioni successive Windows Firewall with Advanced Security (WFAS) viene implementata tramite WFP. Pertanto, le applicazioni sviluppate con l'API Pam o l' [API wfas](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) utilizzano la logica di arbitraggio di filtro comune incorporata in Pam.

L'API PAM è costituita da un'API in modalità utente e da un'API in modalità kernel. In questa sezione viene fornita una panoramica dell'intero WFP e viene descritto in dettaglio solo la parte in modalità utente dell'API Pam. Per una descrizione dettagliata dell'API PAM in modalità kernel, vedere la Guida in linea di [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) .

## <a name="developer-audience"></a>Sviluppatori

L'API Windows Filtering Platform è progettata per l'uso da parte dei programmatori che usano il software di sviluppo C/C++. I programmatori devono acquisire familiarità con i concetti di rete e la progettazione dei sistemi mediante componenti in modalità utente e kernel.

## <a name="run-time-requirements"></a>Requisiti di runtime

Windows Filtering Platform è supportato nei client che eseguono Windows Vista e versioni successive e nei server che eseguono Windows Server 2008 e versioni successive. Per informazioni sui requisiti di run-time per un elemento di programmazione specifico, vedere la sezione requisiti della pagina di riferimento per tale elemento.





 

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                               | Descrizione                                                                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Novità della piattaforma filtro Windows](what-s-new-in-windows-filtering-platform.md)<br/> | Informazioni sulle nuove funzionalità e API nella piattaforma filtro Windows.<br/>                    |
| [Informazioni sulla piattaforma filtro Windows](about-windows-filtering-platform.md)<br/>                 | Panoramica della piattaforma filtro Windows.<br/>                                             |
| [Uso della piattaforma filtro Windows](using-windows-filtering-platform.md)<br/>                 | Codice di esempio che usa l'API della piattaforma filtro Windows. <br/>                                |
| [Informazioni di riferimento sulle API della piattaforma filtro Windows](fwp-reference.md)<br/>                            | Documentazione per le funzioni, le strutture e le costanti di Windows Filtering Platform.<br/> |



 

## <a name="additional-resources"></a>Risorse aggiuntive

Per porre domande e discutere sull'uso dell'API Pam, visitare il forum relativo alla [piattaforma filtro Windows](https://social.msdn.microsoft.com/forums/wfp/threads/).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla progettazione dell'API della piattaforma filtro Windows in modalità kernel](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[Informazioni di riferimento sull'API della piattaforma filtro Windows in modalità kernel](/windows-hardware/drivers/ddi/_netvista/)
</dt> <dt>

[Windows Firewall con sicurezza avanzata](/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page)
</dt> <dt>

[Classe helper di diagnostica WFP](/windows/desktop/NDF/windows-filtering-platform-extensible-helper-class)
</dt> <dt>

[Estensioni Secure socket Winsock](/windows/desktop/WinSock/winsock-secure-socket-extensions)
</dt> </dl>

 

