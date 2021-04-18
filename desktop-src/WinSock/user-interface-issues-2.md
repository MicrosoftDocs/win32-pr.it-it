---
description: Una delle modifiche più ovvie da IPv4 a IPv6 è la dimensione dell'indirizzo IP. Molte interfacce utente forniscono finestre di dialogo che consentono a un utente di immettere un indirizzo IP, come esemplificato nella figura seguente.
ms.assetid: e2d7fd41-297a-400b-ae59-5d67db2be6f6
title: Problemi dell'interfaccia utente per le applicazioni Winsock IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03305073687cdd77e17c529d70ffe5959df40960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316602"
---
# <a name="user-interface-issues-for-ipv6-winsock-applications"></a>Problemi dell'interfaccia utente per le applicazioni Winsock IPv6

Una delle modifiche più ovvie da IPv4 a IPv6 è la dimensione dell'indirizzo IP. Molte interfacce utente forniscono finestre di dialogo che consentono a un utente di immettere un indirizzo IP, come esemplificato nella figura seguente.

![casella indirizzo IPv4 comune in un'interfaccia utente](images/portingguide001.jpg)

L'indirizzamento in IPv6, a causa di molti fattori quali la lunghezza, la complessità e il significato delle sezioni nello spazio degli indirizzi IPv6, non è favorevole alla modifica o alla specifica da parte degli utenti. Pertanto, la necessità di fornire agli utenti la possibilità di specificare il proprio indirizzo è ridotta. Inoltre, a causa della complessità associata all'indirizzamento IPv6, la possibilità per gli amministratori di specificare le informazioni sugli indirizzi IPv6 non può essere eseguita in base ai singoli nodi.

La visualizzazione di un indirizzo IPv6 nell'interfaccia utente non è inutilizzabile e pertanto gli sviluppatori devono considerare la variabilità delle dimensioni di un indirizzo IPv6 quando si modifica un'applicazione per supportare IPv6.

Nella parte restante di questa sezione viene illustrata la differenza tra la prevedibilità degli indirizzi IPv4 e la lunghezza degli indirizzi IPv6. Questa sezione presuppone che gli indirizzi IPv6 siano visualizzati nella relativa rappresentazione esadecimale.

Gli indirizzi IPv4 sono di dimensioni stimabili, perché seguono rigidamente la notazione decimale punteggiata, come illustrato nell'esempio di indirizzo seguente:

``` syntax
10.10.256.1
```

Gli indirizzi IPv6 non sono così stimabili, a causa della convenzione degli indirizzi IPv6 che consente l'uso di un doppio segno di due punti (::) per rappresentare una serie di zeri. Di conseguenza, le rappresentazioni di indirizzo IPv6 seguenti equivalgono allo stesso indirizzo IPv6:

``` syntax
1040:0:0:0:0:0:0:1
1040::1
```

La capacità di rappresentare una serie di zeri con un doppio segno di due punti restituisce una lunghezza imprevedibile per qualsiasi IPv6 specificato, che richiede ai programmatori di prendere in considerazione questa funzionalità quando si creano visualizzazioni dell'interfaccia utente degli indirizzi IPv6. Certamente, gli sviluppatori devono assicurarsi che l'interfaccia utente sia in grado di visualizzare gli indirizzi IP che non utilizzano un doppio segno di due punti per rappresentare una serie di zeri (il primo indirizzo riportato di seguito), oltre a essere in grado di visualizzare l'indirizzo IPv6 più lungo possibile (secondo indirizzo, con l'indirizzo IPv4 incorporato) quando si crea l'interfaccia utente che supporta IPv6. Si noti, inoltre, che l'aggiunta dell'identificatore di ambito (ID) all'indirizzo seguente comporta un aumento della lunghezza di un numero di altri undici caratteri:

``` syntax
21DA:00D3:0010:2F3B:02AA:00FF:FE28:9C5A
0000:0000:0000:0000:0000:ffff:123.123.123.123
```

Un altro aspetto importante è che gli indirizzi basati sul nome siano più appropriati degli indirizzi IPv6 basati su numeri. Se gli indirizzi basati sul nome sono più appropriati, è necessario considerare le convenzioni di denominazione nell'interfaccia utente, inclusi eventuali controlli degli errori di input appropriati per l'attività.

Esistono altre complessità associate alla visualizzazione degli indirizzi IPv6 che devono essere presi in considerazione dagli sviluppatori durante la modifica dell'applicazione e durante la progettazione delle rappresentazioni dell'interfaccia utente degli indirizzi IPv6. Di seguito sono riportate alcune considerazioni:

-   L'indirizzo deve contenere tutte le sequenze di zeri oppure utilizzare la notazione con due punti.
-   È più appropriato usare una rappresentazione di indirizzo basata su numeri o una rappresentazione basata su nome?
-   L'utente è interessato a discernere un certo aspetto dello schema di indirizzamento, ad esempio il prefisso della subnet, l'identificatore dell'ambito o altri campi sottocampi?
-   L'utente è interessato a determinare altri aspetti dell'indirizzo, ad esempio l'identificatore TLA, l'identificatore NLA o l'identificatore del contratto di contratto?
-   L'interfaccia utente sarà in grado di discernere gli indirizzi IPv6 incorporati e, in caso affermativo, come verranno gestiti e visualizzati? Quando si visualizzano le informazioni sull'indirizzo per l'utente, è possibile discernere tra gli indirizzi compatibili con IPv4 e gli indirizzi IPv6 con mapping IPv4?

Esistono anche altre considerazioni e gli sviluppatori devono considerare attentamente i destinatari dei clienti quando sviluppano interfacce utente di indirizzi IP.

Procedure consigliate

-   Gli sviluppatori devono considerare l'approccio appropriato per ogni interfaccia utente quando modificano l'applicazione in modo da supportare IPv6. Verificare che l'interfaccia utente contenga una lunghezza sufficiente per visualizzare gli indirizzi IPv6 è imperativa, in quanto determina se l'indirizzo è basato sul numero o sul nome.
-   Quando possibile, usare le funzioni di helper Winsock e IP esistenti quando si usano indirizzi IPv6 anziché implementare nuovamente questa logica. È ad esempio possibile utilizzare le funzioni [**RtlIpv6AddressToString**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa), [**RtlIpv6AddressToStringEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw), [**RtlIpv6StringToAddress**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)e [**RtlIpv6StringToAddressEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw) per eseguire la conversione tra gli indirizzi IPv6 e le rappresentazioni di stringa di questi indirizzi IPv6.

Codice da evitare

-   Gli elementi dell'interfaccia utente che dipendono da un indirizzo di dimensione IPv4 devono essere sottoposti a controllo e parte del controllo deve includere se le informazioni fornite (in IPv4) sono appropriate per IPv6.
-   La possibilità di specificare un indirizzo IP deve inoltre dipendere dal fatto che sia in uso IPv4 o che IPv6 sia disponibile. Se IPv6 è disponibile, è opportuno specificare indirizzi basati su numeri (esadecimali) o indirizzi basati sul nome?

Attività di codifica

**Per rivedere la codebase esistente da IPv4 a IPv4 e IPv6-interoperabilità**

1.  Eseguire una revisione visiva dell'interfaccia utente, cercando qualsiasi elemento che dipenda da una lunghezza specifica per la stringa dell'indirizzo IP. I controlli con la notazione decimale tratteggiata a quattro sezioni facilmente identificabili sono facili da individuare, mentre altri non lo sono. È possibile che vengano visualizzati indirizzi IP, ad esempio nelle finestre di dialogo, in cui un indirizzo IPv6 potrebbe esaurire lo spazio di visualizzazione.
2.  Quando si trova uno di questi controlli, verificare se è appropriato visualizzare l'indirizzo quando si utilizza IPv6. Se è possibile che sia in uso IPv4 o IPv6, assicurarsi che l'interfaccia utente sia in grado di supportare. Sostituire o aumentare i controlli con i controlli dell'interfaccia utente che possono visualizzare un intero indirizzo IPv6.
3.  Completamento del test dell'interfaccia utente per assicurarsi che le modifiche che consentono la visualizzazione degli indirizzi IPv6 mantengano l'usabilità prevista quando si utilizzano gli indirizzi IPv4. Testare anche le posizioni di visualizzazione degli indirizzi del protocollo, ad esempio le finestre di dialogo informative, per assicurarsi che gestiscano correttamente gli indirizzi IPv6.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida a IPv6 per le applicazioni Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Modifica delle strutture di dati per applicazioni Winsock IPv6](changing-data-structures-2.md)
</dt> <dt>

[Socket dual stack per applicazioni Winsock IPv6](dual-stack-sockets.md)
</dt> <dt>

[Chiamate di funzione per applicazioni Winsock IPv6](function-calls-2.md)
</dt> <dt>

[Utilizzo di indirizzi IPv4 hardcoded](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Protocolli sottostanti per applicazioni Winsock IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 
