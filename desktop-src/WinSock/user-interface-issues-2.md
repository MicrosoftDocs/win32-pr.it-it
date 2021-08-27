---
description: Una delle modifiche più ovvie da IPv4 a IPv6 è la dimensione dell'indirizzo IP. Molte interfacce utente forniscono finestre di dialogo che consentono a un utente di immettere un indirizzo IP, come illustrato nella figura seguente.
ms.assetid: e2d7fd41-297a-400b-ae59-5d67db2be6f6
title: Interfaccia utente problemi relativi alle applicazioni Winsock IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae982504798789c928691bbf4932d5e6abdfabf1ba12077122bb6dab28eb47de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121187"
---
# <a name="user-interface-issues-for-ipv6-winsock-applications"></a>Interfaccia utente problemi relativi alle applicazioni Winsock IPv6

Una delle modifiche più ovvie da IPv4 a IPv6 è la dimensione dell'indirizzo IP. Molte interfacce utente forniscono finestre di dialogo che consentono a un utente di immettere un indirizzo IP, come illustrato nella figura seguente.

![Casella dell'indirizzo ipv4 comune in un'interfaccia utente](images/portingguide001.jpg)

L'indirizzamento in IPv6, a causa di molti fattori, ad esempio lunghezza, complessità e significato delle sezioni all'interno dello spazio di indirizzi IPv6, non è conducente alla modifica o alla specifica da parte degli utenti. Di conseguenza, la necessità di fornire agli utenti la possibilità di specificare il proprio indirizzo è ridotta. Inoltre, a causa della complessità associata all'indirizzamento IPv6, non è probabile che gli amministratori siano in grado di specificare le informazioni sull'indirizzo IPv6 in base al nodo.

La visualizzazione di un indirizzo IPv6 nell'interfaccia utente non è inconcepibile e pertanto gli sviluppatori devono considerare la variabilità nelle dimensioni di un indirizzo IPv6 quando si modifica un'applicazione per supportare IPv6.

Nella parte restante di questa sezione viene illustrata la differenza tra le considerazioni sulla prevedibilità della lunghezza degli indirizzi IPv4 e sulla lunghezza degli indirizzi IPv6. In questa sezione si presuppone che gli indirizzi IPv6 vengano visualizzati nella relativa rappresentazione esadecimale.

Gli indirizzi IPv4 hanno dimensioni prevedibili, perché seguono rigidamente la notazione decimale virgola, come illustrato nell'esempio di indirizzo seguente:

``` syntax
10.10.256.1
```

Gli indirizzi IPv6 non sono così prevedibili, a causa della convenzione degli indirizzi IPv6 che consente l'uso di due punti (::) per rappresentare una serie di zeri. Di conseguenza, le rappresentazioni degli indirizzi IPv6 seguenti equi equidominano allo stesso indirizzo IPv6:

``` syntax
1040:0:0:0:0:0:0:1
1040::1
```

La possibilità di rappresentare una serie di zeri con un doppio segno di due punti comporta una lunghezza imprevedibile per qualsiasi IPv6 specificato. È quindi necessario che i programmatori prendano in considerazione questa funzionalità durante la creazione di schermi dell'interfaccia utente di indirizzi IPv6. È certo che gli sviluppatori devono assicurarsi che l'interfaccia utente sia in grado di visualizzare gli indirizzi IP che non usano due punti per rappresentare una serie di zeri (il primo indirizzo riportato di seguito), nonché di visualizzare l'indirizzo IPv6 più lungo possibile (il secondo indirizzo riportato di seguito, con l'indirizzo IPv4 incorporato) durante la creazione dell'interfaccia utente con supporto per IPv6. Si noti anche che l'aggiunta dell'identificatore di ambito (ID) all'indirizzo seguente ne aumenta la lunghezza fino a un massimo di altri 11 caratteri:

``` syntax
21DA:00D3:0010:2F3B:02AA:00FF:FE28:9C5A
0000:0000:0000:0000:0000:ffff:123.123.123.123
```

Un'altra considerazione importante è se gli indirizzi basati sui nomi sono più appropriati rispetto agli indirizzi IPv6 basati su numeri. Se gli indirizzi basati sui nomi sono più appropriati, è necessario considerare le convenzioni di denominazione nell'interfaccia utente, incluso qualsiasi controllo degli errori di input appropriato per l'attività.

Esistono altre complessità associate alla visualizzazione di indirizzi IPv6 che gli sviluppatori devono prendere in considerazione quando modificano l'applicazione e quando progettano rappresentazioni dell'interfaccia utente di indirizzi IPv6. Di seguito sono riportate alcune considerazioni:

-   L'indirizzo deve contenere tutte le sequenze di zeri o usare la notazione con due punti?
-   È più appropriato usare una rappresentazione dell'indirizzo basata su numeri o una rappresentazione basata sul nome?
-   L'utente è interessato a distinguere un determinato aspetto dello schema di indirizzamento, ad esempio il prefisso della subnet, l'identificatore di ambito o altri sottocampi?
-   L'utente è interessato a determinare altri aspetti dell'indirizzo, ad esempio l'identificatore TLA, l'identificatore NLA o l'identificatore sla?
-   L'interfaccia utente sarà in grado di distinguere gli indirizzi IPv6 incorporati e, in tal caso, come verranno gestiti e visualizzati? Si distinguerà tra gli indirizzi compatibili con IPv4 e gli indirizzi IPv6 mappati a IPv4 quando si visualizzano le informazioni sugli indirizzi per l'utente?

Esistono anche altre considerazioni e gli sviluppatori devono considerare attentamente i destinatari dei clienti quando sviluppano interfacce utente degli indirizzi IP.

Procedure consigliate

-   Gli sviluppatori devono considerare l'approccio appropriato a ogni interfaccia utente quando modificano l'applicazione per supportare IPv6. Assicurarsi che l'interfaccia utente contenga una lunghezza sufficiente per visualizzare gli indirizzi IPv6 è fondamentale, così come determinare se tale indirizzo è basato sul numero o sul nome.
-   Quando possibile, usare le funzioni winsock e helper IP esistenti quando si usano indirizzi IPv6 anziché implementare nuovamente questa logica. Ad esempio, le funzioni [**RtlIpv6AddressToString**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa), [**RtlIpv6AddressToStringEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw), [**RtlIpv6StringToAddress**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)e [**RtlIpv6StringToAddressEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw) possono essere usate per la conversione tra indirizzi IPv6 e rappresentazioni di stringa di questi indirizzi IPv6.

Codice da evitare

-   Gli elementi dell'interfaccia utente che dipendono da un indirizzo di dimensioni IPv4 devono essere sottoposti a controllo e parte di tale controllo deve includere se le informazioni fornite (in IPv4) sono appropriate per IPv6.
-   La possibilità di specificare un indirizzo IP deve anche dipendere dal fatto che IPv4 sia in uso o che IPv6 sia disponibile. Se IPv6 è disponibile, è opportuno specificare indirizzi basati su numeri (esadecimali) o indirizzi basati sul nome?

Attività di codifica

**Per rivedere la codebase esistente da IPv4 all'interoperabilità IPv4 e IPv6**

1.  Eseguire una revisione visiva dell'interfaccia utente, cercando qualsiasi elemento che dipende da una lunghezza specifica per la stringa dell'indirizzo IP. I controlli con notazione decimale a quattro sezioni facilmente identificabili sono facili da individuare, mentre altri no. In alcuni casi è possibile che gli indirizzi IP siano visualizzati, ad esempio nelle finestre di dialogo, in cui un indirizzo IPv6 potrebbe non essere più visualizzato.
2.  Dopo aver trovato uno di questi controlli, verificare se è appropriato visualizzare l'indirizzo quando si usa IPv6. Se è possibile che sia in uso IPv4 o IPv6, assicurarsi che l'interfaccia utente sia in grado di supportare entrambi. Sostituire o aumentare i controlli con controlli dell'interfaccia utente in grado di visualizzare un intero indirizzo IPv6.
3.  Completare i test dell'interfaccia utente per assicurarsi che le modifiche che abilitano la visualizzazione degli indirizzi IPv6 mantengano l'usabilità prevista quando si usano indirizzi IPv4. Testare anche i percorsi di visualizzazione degli indirizzi del protocollo, ad esempio le finestre di dialogo in formato informativo, per assicurarsi che gestiranno correttamente gli indirizzi IPv6.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida a IPv6 per Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Modifica delle strutture dei dati per le applicazioni Winsock IPv6](changing-data-structures-2.md)
</dt> <dt>

[Dual-Stack Sockets per applicazioni Winsock IPv6](dual-stack-sockets.md)
</dt> <dt>

[Chiamate di funzione per applicazioni Winsock IPv6](function-calls-2.md)
</dt> <dt>

[Uso di indirizzi IPv4 hardcoded](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Protocolli sottostanti per applicazioni Winsock IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 
