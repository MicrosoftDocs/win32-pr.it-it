---
description: Questa guida fornisce le informazioni necessarie per consentire all'applicazione Microsoft Windows di usare la nuova generazione del protocollo Internet versione 6 (IPv6).
ms.assetid: 8e862eb0-2ba9-40b0-ac73-fcb0e625965e
title: Guida a IPv6 per Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c52d86dfcdfa06df80dc71a3f3313de19f9201c7421a3f27f094589a6656dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741115"
---
# <a name="ipv6-guide-for-windows-sockets-applications"></a>Guida a IPv6 per Windows Sockets

Questa guida fornisce le informazioni necessarie per consentire all'applicazione Microsoft Windows di usare la nuova generazione del protocollo Internet versione 6 (IPv6). L'aggiunta della funzionalità IPv6 all'applicazione non è necessariamente un processo di portabilità. Per convertire un'applicazione, suggerisce di modificare il codice in modo che funzioni su una piattaforma diversa, il che implica l'abbandono della piattaforma precedente. Questa guida è strutturata in modo specifico per consentire l'aggiunta di funzionalità IPv6 a un'applicazione mantenendo al tempo stesso la funzionalità IPv4.

Questa guida illustra i problemi associati all'aggiunta di funzionalità IPv6 e quindi fa riferimento alle aree di sviluppo più interessate dalla transizione. Ogni area riceve una spiegazione approfondita delle insidie da controllare, delle strategie suggerite per evitarle e suggerimenti su come usare al meglio i nuovi elementi programmatici [di Windows Sockets 2](what-s-new-for-windows-sockets-2.md) (funzioni e strutture). Per altre informazioni su IPv6, vedere [Supporto di IPv6.](ipv6-support-2.md)

Questa guida fornisce anche esempi di codice per offrire esperienza e rappresentazioni visive dei problemi che possono verificarsi durante la modifica delle applicazioni. Gli esempi provengono da esempi completi e funzionanti di una semplice applicazione Windows Sockets modificata per supportare sia IPv4 che IPv6. Il codice sorgente per questi esempi di lavoro è incluso per intero in due appendici alla fine di questo documento: [Appendice A:](appendix-a-ipv4-only-source-code-2.md) Codice sorgente solo IPv4 include il codice sorgente per un'applicazione prima che venga modificata per supportare IPv6; [Appendice B: Codice](appendix-b-ip-version-agnostic-source-code-2.md) sorgente indipendente dalla versione IP fornisce il codice sorgente dopo che l'applicazione è stata abilitata per IPv6.

Microsoft offre un'utilità denominata Checkv4.exe che consente di trovare codice potenzialmente sensibile alla portabilità nel codice dell'applicazione e fornisce anche raccomandazioni per le correzioni. L'utilità Checkv4.exe viene illustrata in questo documento, usando l'applicazione di esempio inclusa nelle appendici, insieme a screenshot che visualizzano l'output prodotto dall'utilità Checkv4.exe. Per altre informazioni, vedere [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).

Le aree di programmazione trattate da questa guida sono:

-   [Modifica delle strutture dei dati per le applicazioni Winsock IPv6](changing-data-structures-2.md)
-   [Chiamate di funzione per applicazioni Winsock IPv6](function-calls-2.md)
-   [Uso di indirizzi IPv4 hardcoded](use-of-hardcoded-ipv4-addresses-2.md)
-   [Interfaccia utente problemi relativi alle applicazioni Winsock IPv6](user-interface-issues-2.md)
-   [Protocolli sottostanti per applicazioni Winsock IPv6](underlying-protocols-2.md)
-   [Dual-Stack Sockets per applicazioni Winsock IPv6](dual-stack-sockets.md)

Poiché non esiste una sequenza uniforme di eventi, le sezioni che consentono di risolvere i problemi di abilitazione di IPv6 non vengono disposte in modo sequenzialemente significativo, pertanto è possibile fare riferimento a qualsiasi sezione in qualsiasi momento. È consigliabile esaminare ogni sezione durante l'aggiunta della funzionalità IPv6 all'applicazione. È anche consigliabile leggere le informazioni sull'utilità Checkv4.exe, perché include suggerimenti sull'ordine in cui risolvere i problemi di abilitazione di IPv6.

Per esaminare l'utilità Checkv4.exe ed esaminare l'ordine in cui è consigliabile affrontare il processo di porting nelle applicazioni, vedere Uso [dell'utilità Checkv4.exe](using-the-checkv4-exe-utility-2.md). Questa sezione include informazioni su un flag in fase di compilazione che verifica rigorosamente la presenza di elementi di programmazione incompatibili con IPv6.

Per passare direttamente all'applicazione di esempio, vedere [Appendice A: Codice](appendix-a-ipv4-only-source-code-2.md) sorgente solo IPv4 e [Appendice B:](appendix-b-ip-version-agnostic-source-code-2.md)Codice sorgente indipendente dalla versione IP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Protocollo IP versione 6 (IPv6)](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[Supporto IPv6](ipv6-support-2.md)
</dt> <dt>

[IPv6 Technology Preview per Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[Utilizzo dell'utilità Checkv4.exe](using-the-checkv4-exe-utility-2.md)
</dt> <dt>

[Appendice A: Codice sorgente solo IPv4](appendix-a-ipv4-only-source-code-2.md)
</dt> <dt>

[Appendice B: Codice sorgente indipendente dalla versione IP](appendix-b-ip-version-agnostic-source-code-2.md)
</dt> </dl>

 

 



