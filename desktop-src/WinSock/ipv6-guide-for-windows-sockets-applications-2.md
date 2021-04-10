---
description: Questa guida fornisce le informazioni necessarie per consentire all'applicazione Microsoft Windows di usare la nuova generazione di protocollo Internet, versione 6 (IPv6).
ms.assetid: 8e862eb0-2ba9-40b0-ac73-fcb0e625965e
title: Guida a IPv6 per le applicazioni Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3c582ba8dc10c167d47aafe98b1e8742551f948
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129170"
---
# <a name="ipv6-guide-for-windows-sockets-applications"></a>Guida a IPv6 per le applicazioni Windows Sockets

Questa guida fornisce le informazioni necessarie per consentire all'applicazione Microsoft Windows di usare la nuova generazione di protocollo Internet, versione 6 (IPv6). L'aggiunta di funzionalità IPv6 all'applicazione non è necessariamente un processo di porting. Per eseguire il porting di un'applicazione, è necessario modificare il codice per lavorare su una piattaforma diversa, che implica l'uscita dalla precedente piattaforma. Questa guida è strutturata in modo specifico per consentire l'aggiunta di funzionalità IPv6 a un'applicazione, mantenendo al tempo stesso la funzionalità IPv4.

In questa guida vengono illustrati i problemi associati all'aggiunta di funzionalità IPv6, quindi vengono indirizzate le aree di sviluppo più interessate dalla transizione. Ogni area riceve una spiegazione completa degli errori da tenere sotto controllo, le strategie suggerite per evitarle e suggerimenti su come sfruttare al meglio i nuovi elementi programmatici di [Windows Sockets 2](what-s-new-for-windows-sockets-2.md) (funzioni e strutture). Per ulteriori informazioni su IPv6, vedere [supporto per IPv6](ipv6-support-2.md).

Questa guida fornisce anche esempi di codice per offrire un'esperienza pratica e rappresentazioni visive dei problemi che possono verificarsi quando si modificano le applicazioni. Gli esempi derivano da esempi completi e funzionanti di una semplice applicazione Windows Sockets che è stata modificata per supportare sia IPv4 che IPv6. Il codice sorgente per questi esempi funzionanti è incluso interamente in due appendici alla fine di questo documento: [appendice a: il codice sorgente solo IPv4](appendix-a-ipv4-only-source-code-2.md) include il codice sorgente di un'applicazione prima che venga modificato per supportare IPv6. [Appendice B: codice sorgente indipendente dalla versione IP](appendix-b-ip-version-agnostic-source-code-2.md) fornisce il codice sorgente dopo che l'applicazione è stata abilitata per IPv6.

Microsoft fornisce un'utilità denominata Checkv4.exe che consente di trovare codice potenzialmente dipendente dal porting nel codice dell'applicazione, oltre a indicazioni per le correzioni. L'utilità Checkv4.exe viene illustrata in questo documento, utilizzando l'applicazione di esempio inclusa nelle appendici, insieme a schermate che visualizzano l'output prodotto dall'utilità Checkv4.exe. Per ulteriori informazioni, vedere [utilizzo dell'utilità Checkv4.exe](using-the-checkv4-exe-utility-2.md).

Le aree di programmazione indirizzate in questa guida sono:

-   [Modifica delle strutture di dati per applicazioni Winsock IPv6](changing-data-structures-2.md)
-   [Chiamate di funzione per applicazioni Winsock IPv6](function-calls-2.md)
-   [Utilizzo di indirizzi IPv4 hardcoded](use-of-hardcoded-ipv4-addresses-2.md)
-   [Problemi dell'interfaccia utente per le applicazioni Winsock IPv6](user-interface-issues-2.md)
-   [Protocolli sottostanti per applicazioni Winsock IPv6](underlying-protocols-2.md)
-   [Socket dual stack per applicazioni Winsock IPv6](dual-stack-sockets.md)

Poiché non esiste una sequenza uniforme di eventi, le sezioni che indirizzano i problemi di abilitazione di IPv6 non vengono disposte in modo sequenziale, quindi è possibile fare riferimento a qualsiasi sezione in qualsiasi momento. Si consiglia vivamente di rivedere ogni sezione durante l'aggiunta della funzionalità IPv6 all'applicazione. È inoltre consigliabile leggere informazioni sull'utilità Checkv4.exe, in quanto include suggerimenti sull'ordine di risoluzione dei problemi di abilitazione di IPv6.

Per esaminare l'utilità di Checkv4.exe e per rivedere l'ordine in cui è necessario affrontare il processo di porting nelle applicazioni, vedere [utilizzo dell'utilità di Checkv4.exe](using-the-checkv4-exe-utility-2.md). In questa sezione sono incluse informazioni su un flag della fase di compilazione che controlla rigorosamente gli elementi di programmazione incompatibili con IPv6.

Per passare direttamente all'applicazione di esempio, vedere [appendice a: codice sorgente solo IPv4](appendix-a-ipv4-only-source-code-2.md) e [Appendice B: codice sorgente indipendente dalla versione IP](appendix-b-ip-version-agnostic-source-code-2.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Protocollo IP versione 6 (IPv6)](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[Supporto IPv6](ipv6-support-2.md)
</dt> <dt>

[Anteprima della tecnologia IPv6 per Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[Utilizzo dell'utilità Checkv4.exe](using-the-checkv4-exe-utility-2.md)
</dt> <dt>

[Appendice A: codice sorgente solo IPv4](appendix-a-ipv4-only-source-code-2.md)
</dt> <dt>

[Appendice B: codice sorgente indipendente dalla versione IP](appendix-b-ip-version-agnostic-source-code-2.md)
</dt> </dl>

 

 



