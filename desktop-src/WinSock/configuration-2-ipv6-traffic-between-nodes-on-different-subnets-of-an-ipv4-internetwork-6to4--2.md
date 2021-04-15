---
description: 6to4 è un metodo per la connessione di host o siti IPv6 tramite l'infrastruttura Internet IPv4 esistente.
ms.assetid: 3ca8518d-42f0-428c-b94c-ff244d17b314
title: 'Configurazione 2: traffico IPv6 tra nodi in subnet diverse di un Internet (6to4) IPv4'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1abd5477005e6a1e71c13aaf19a734e9191097d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484949"
---
# <a name="configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4"></a>Configurazione 2: traffico IPv6 tra nodi in subnet diverse di un Internet (6to4) IPv4

6to4 è un metodo per la connessione di host o siti IPv6 tramite l'infrastruttura Internet IPv4 esistente. Usa un prefisso di indirizzo univoco per fornire ai siti IPv6 isolati il proprio spazio di indirizzi IPv6. 6to4 è come uno "pseudo-ISP" che fornisce la connettività IPv6. È possibile utilizzare 6to4 per comunicare direttamente con altri siti 6to4. 6to4 non richiede l'utilizzo di router IPv6 e il traffico IPv6 è incapsulato con un'intestazione IPv4.

Nella figura seguente viene illustrata la configurazione di due nodi in subnet separate mediante 6to4 per la comunicazione attraverso un router IPv4.

![nodi che usano 6to4 per comunicare attraverso un router IPv4.](images/v6mig-2.png)

Il requisito principale per l'utilizzo di 6to4 è un indirizzo IPv4 instradabile a livello globale per il sito. Si supponga che il sito sia costituito da una raccolta di computer IPv6 gestiti (alcuni eseguono il protocollo IPv6 Microsoft e altre implementazioni IPv6). Si supponga inoltre che tutti i computer IPv6 siano connessi direttamente tramite Ethernet o 6-over-4. L'indirizzo IPv4 instradabile a livello globale deve essere assegnato a uno dei computer in cui è in esecuzione il protocollo IPv6 Microsoft. Il computer sarà il gateway 6to4.

Se si dispone di un indirizzo IPv4 che fa parte dello spazio di indirizzi privato (10.0.0.0/8, 172.16.0.0/12 o 192.168.0.0/16) o dello spazio di indirizzi APIPA (Automatic Private IP Addressing) di 169.254.0.0/16 usato da Windows 2000, non è instradabile a livello globale. In caso contrario, si tratta probabilmente di un indirizzo IP pubblico ed è instradabile a livello globale. Per ulteriori informazioni su come determinare se la connessione ISP supporta 6to4, vedere l'argomento [debug di configurazione 6to4](#debugging-6to4-configuration) in questo documento.

## <a name="the-6to4cfgexe-tool"></a>Strumento 6to4cfg.exe

Lo strumento 6to4cfg.exe automatizza la configurazione 6to4, individuando automaticamente l'indirizzo IPv4 instradabile a livello globale e creando un prefisso 6to4. Esegue direttamente la configurazione oppure può scrivere uno script di configurazione che può essere ispezionato ed eseguito in un secondo momento.

Di seguito è riportata la sintassi di base del comando 6to4cfg.exe.

``` syntax
6to4cfg [-r] [-s] [-u] [-R relay] [-b] [-S address] [filename]
```

<dl> <dt>

<span id="_filename_"></span><span id="_FILENAME_"></span>\[*filename*\]
</dt> <dd>

Scrive lo script di configurazione in un file, se si specifica un nome file. Lo script di configurazione utilizza Ipv6.exe.

È possibile specificare con per il nome file per scrivere lo script di configurazione nell'output della console, che risulta utile per vedere quali 6to4cfg.exe eseguiranno in uno scenario di test.

Se non si specifica un nome di file, 6to4cfg.exe aggiorna direttamente la configurazione IPv6 nel computer.

</dd> <dt>

<span id="-r"></span><span id="-R"></span>-r
</dt> <dd>

Diventa un router del gateway 6to4 per la rete locale, abilitando il routing su tutte le interfacce e i prefissi di subnet assegnati.

</dd> <dt>

<span id="-s"></span><span id="-S"></span>-s
</dt> <dd>

Abilita l'indirizzamento locale del sito nel sito 6to4. Questo comando è utile solo se utilizzato in combinazione con-r.

</dd> <dt>

<span id="-u"></span><span id="-U"></span>-u
</dt> <dd>

Specifica che la configurazione 6to4 deve essere invertita. Pertanto 6to4cfg-u inverte l'effetto di 6to4cfg e 6to4cfg-r-u inverte l'effetto di 6to4cfg-r e così via.

</dd> <dt>

<span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>- *Inoltro* R
</dt> <dd>

Specifica il nome o l'indirizzo IPv4 di un router di inoltro 6to4. Il nome predefinito è 6to4.ipv6.microsoft.com, il router di inoltro 6to4 su Internet.

</dd> <dt>

<span id="-b"></span><span id="-B"></span>-b
</dt> <dd>

Specifica che 6to4cfg.exe seleziona l'indirizzo di inoltro "migliore" anziché il primo.

</dd> <dt>

<span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>-S *Indirizzo*
</dt> <dd>

Specifica l'indirizzo IPv4 locale per il prefisso 6to4.

</dd> </dl>

## <a name="manual-6to4-configuration"></a>Configurazione di 6to4 manuale

In questo esempio l'indirizzo del gateway 6to4 è 172.31.42.239. Per usare 6to4, è necessario un indirizzo IPv4 instradabile a livello globale.

> [!Note]  
> L'indirizzo IP 172.31.42.239 viene usato solo a scopo esemplificativo. Si tratta di un indirizzo privato e non è instradabile a livello globale su Internet.

 

L'indirizzo IPv4 instradabile a 32 bit viene combinato con il prefisso 2002::/16 a 16 bit per formare un prefisso di indirizzo IPv6 a 48 bit per il sito. In questo esempio, il prefisso del sito 6to4 è 2002: ac1f: 2AEF::/48. Si noti che ac1f: 2AEF è la codifica esadecimale di 172.31.42.239 (ovviamente, si userà un prefisso diverso in base all'indirizzo IPv4 instradabile a livello globale). Utilizzando il prefisso del sito 6to4, è possibile assegnare indirizzi e prefissi di subnet all'interno del sito.

Questo esempio presuppone che si usi la subnet 0 per configurare manualmente un indirizzo 6to4 nel computer gateway 6to4 e che si usi la subnet 1 per la configurazione automatica degli indirizzi nel segmento di rete Ethernet. Sono tuttavia possibili altre scelte.

1.  Utilizzare Ipv6.exe per abilitare 6to4 nel computer gateway 6to4:

    **RTU 2002::/16 2 IPv6**

    Il comando **RTU IPv6** esegue un aggiornamento della tabella di routing. Può essere usato per aggiungere, rimuovere o aggiornare una route. In questo caso viene abilitato 6to4.

    L'argomento 2002::/16 è il prefisso della route, che specifica il prefisso 6to4 univoco.

    L'argomento 2 specifica l'interfaccia in collegamento per questo prefisso. \#L'interfaccia 2 è la "pseudo-interfaccia" usata per i tunnel configurati, il tunneling automatico e 6to4. Quando un indirizzo di destinazione IPv6 corrisponde al prefisso 2002::/16, vengono estratti i 32 bit che seguono il prefisso nell'indirizzo di destinazione per formare un indirizzo di destinazione IPv4. Il pacchetto viene incapsulato con un'intestazione IPv4 e inviato all'indirizzo di destinazione IPv4.

2.  Configurare un indirizzo 6to4 nel computer gateway 6to4:

    **IPv6 Adu 2/2002: ac1f: 2AEF:: ac1f: 2AEF**

    Il comando **Adu di IPv6** esegue un aggiornamento degli indirizzi. Può essere usato per aggiungere, rimuovere o aggiornare un indirizzo in un'interfaccia. In questa istanza viene configurato l'indirizzo 6to4 del computer.

    L'argomento 2/2002: ac1f: 2AEF:: ac1f: 2AEF specifica sia l'interfaccia che l'indirizzo. È necessario configurare Address 2002: ac1f: 2AEF:: ac1f: 2AEF sull'interfaccia \# 2. L'indirizzo viene creato usando il prefisso del sito 2002: ac1f: 2AEF::/48, subnet 0 per assegnare un prefisso di subnet 2002: ac1f: 2AEF::/64 e un identificatore di interfaccia a 64 bit. La convenzione illustrata usa l'indirizzo IPv4 del computer per l'identificatore di interfaccia per gli indirizzi assegnati all'interfaccia \# 2. Per l'uso, ac1f: 2AEF deve essere sostituito dalla codifica esadecimale dell'indirizzo IPv4 instradabile a livello globale.

I due comandi precedenti sono sufficienti per consentire la comunicazione con altri siti 6to4. Ad esempio, è possibile provare a effettuare il ping del sito Microsoft 6to4:

**ping6 2002:836b: 9820:: 836b: 9820**

Per abilitare la comunicazione con backbone 6bone, è necessario creare un tunnel configurato predefinito per un inoltro 6to4. È possibile utilizzare il router di inoltro Microsoft 6to4, 131.107.152.32:

**RTU IPv6::/0 2/:: 131.107.152.32 pub vita 1800**

Il comando **RTU IPv6** esegue un aggiornamento della tabella di routing, stabilendo, in questa istanza, una route predefinita al relay 6to4.

L'argomento::/0 è il prefisso della route. Il prefisso di lunghezza zero indica che si tratta di una route predefinita.

L'argomento 2/:: 131.107.152.32 specifica il prossimo hop successivo per questo prefisso. Richiede che i pacchetti corrispondenti al prefisso vengano inoltrati a address:: 131.107.152.32 usando Interface \# 2. L'invio di un pacchetto a:: 131.107.152.32 sull'interfaccia \# 2 ne determina l'incapsulamento con un'intestazione V4 e l'invio a 131.107.152.32.

L'argomento pub rende questa una route pubblicata. Poiché questo è pertinente solo per i router, non ha alcun effetto fino a quando non viene abilitato il routing. Analogamente, la durata di 30 minuti riguarda solo se il routing è abilitato.

Dovrebbe essere possibile accedere ai siti di backbone 6bone e ai siti 6to4. Per eseguire il test, è possibile usare il comando seguente:

**ping6 3FFE: 1CFF: 0: F5:: 1**

Il passaggio finale consiste nell'abilitare il routing sul gateway 6to4. Questo esempio si basa sul presupposto che l'interfaccia \# 3 sul computer gateway sia un'interfaccia Ethernet e che l'interfaccia \# 4 sia 6-over-4. Il computer potrebbe numerare le interfacce in modo diverso. I due comandi seguenti assegnano i prefissi di subnet ai due collegamenti. I prefissi di subnet sono derivati dal prefisso 6to4 del sito 2002: ac1f: 2AEF::/48:

**IPv6 RTU 2002: ac1f: 2AEF: 1::/64 3 pub vita 1800**

**IPv6 RTU 2002: ac1f: 2AEF: 2::/64 4 pub vita 1800**

Il comando **RTU IPv6** specifica che il prefisso 2002: ac1f: 2AEF: 1::/64 è in collegamento all'interfaccia \# 3. Viene configurato il prefisso della prima subnet sull'interfaccia Ethernet. La route viene pubblicata con una durata di 30 minuti.

Analogamente, il prefisso 2002: ac1f: 2AEF: 2::/64 è configurato sull'interfaccia 6-over-4.

I tre comandi successivi abilitano il funzionamento del computer gateway 6to4 come router:

**FORW IFC 2 IPv6**

**FORW ADV di IPv6 IFC 3**

**FORW ADV IPv6 IFC 4**

Il comando **IFC IPv6** controlla gli attributi di un'interfaccia. Un router inoltra i pacchetti e invia annunci router. Nell'implementazione di Microsoft IPv6, questi attributi per interfaccia sono controllati separatamente.

\#L'interfaccia 2 non è necessaria per la pubblicità perché si tratta di una pseudo-interfaccia.

Se il computer dispone di interfacce aggiuntive, è necessario configurarle anche per l'invio e la pubblicità.

Dopo l'esecuzione di questi comandi, il protocollo IPv6 Microsoft configurerà automaticamente gli indirizzi sulle interfacce \# 3 e \# 4 usando i rispettivi prefissi di subnet e le due interfacce inizieranno a inviare annunci router a intervalli approssimativamente da 3 a 10 minuti.

Gli host che ricevono questi annunci router si configureranno automaticamente con una route predefinita e un indirizzo 6to4 derivato dal prefisso della subnet del collegamento. Avranno la comunicazione con altri siti 6to4 e backbone 6bone tramite il computer gateway.

## <a name="debugging-6to4-configuration"></a>Debug della configurazione 6to4

**Per eseguire il debug della configurazione 6to4**

1.  Verificare la connettività IPv4 al router di inoltro 6to4:

    **ping 6to4.ipv6.microsoft.com**

    Se l'operazione ha esito negativo, non si dispone della connettività Internet globale.

2.  Controllare l'incapsulamento IPv6 usando il tunneling automatico:

    **ping6:: 131.107.152.32**

    Se il problema persiste, è possibile che sia presente un firewall o un Network Address Translator (NAT) tra il computer e Internet. Se l'operazione ha esito positivo, la connessione Internet può supportare 6to4.

3.  Controllare la visualizzazione del comando IPv6 RT. Verrà visualizzata una route 2002::/16-> 2. Controllare la visualizzazione del comando IPv6 If 2. Verrà visualizzato un indirizzo preferito con un prefisso 2002::/16.

> [!Note]  
> L'indirizzo IPv4 del router di inoltro Microsoft 6to4 di 131.107.152.32 è soggetto a modifiche. Se il passaggio 2 precedente non funziona, controllare l'output del comando ping nel passaggio 1 per verificare l'indirizzo IPv4 del router di inoltro Microsoft 6to4.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazioni consigliate per IPv6](recommended-configurations-2.md)
</dt> <dt>

[Singola subnet con indirizzi locali rispetto al collegamento](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[Utilizzo di IPsec tra due host di collegamento locale](configuration-4-using-ipsec-between-two-local-link-hosts-2.md)
</dt> </dl>

 

 



