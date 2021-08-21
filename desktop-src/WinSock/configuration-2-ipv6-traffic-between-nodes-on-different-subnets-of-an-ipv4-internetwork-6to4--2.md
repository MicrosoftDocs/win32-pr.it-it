---
description: 6to4 è un metodo per la connessione di host o siti IPv6 tramite l'infrastruttura Internet IPv4 esistente.
ms.assetid: 3ca8518d-42f0-428c-b94c-ff244d17b314
title: 'Configurazione 2: traffico IPv6 tra nodi in subnet diverse di un internetwork IPv4 (6to4)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d976aa3ea21d990ea22f861fbf05a816866e6b0d21502211e23a0e331a2f851
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112502"
---
# <a name="configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4"></a>Configurazione 2: traffico IPv6 tra nodi in subnet diverse di un internetwork IPv4 (6to4)

6to4 è un metodo per la connessione di host o siti IPv6 tramite l'infrastruttura Internet IPv4 esistente. Usa un prefisso di indirizzo univoco per assegnare ai siti IPv6 isolati il proprio spazio indirizzi IPv6. 6to4 è simile a uno "pseudo-ISP" che fornisce connettività IPv6. È possibile usare 6to4 per comunicare direttamente con altri siti 6to4. 6to4 non richiede l'uso di router IPv6 e il relativo traffico IPv6 è incapsulato con un'intestazione IPv4.

La figura seguente illustra la configurazione di due nodi in subnet separate che usano 6to4 per comunicare tra un router IPv4.

![nodi che usano 6to4 per comunicare attraverso un router ipv4.](images/v6mig-2.png)

Il requisito principale per l'uso di 6to4 è un indirizzo IPv4 instradabile a livello globale per il sito. Si supponga che il sito sia costituito da una raccolta di computer IPv6 gestiti (alcuni che eseguono il protocollo IPv6 Microsoft e altri che eseguono altre implementazioni IPv6). Si supponga anche che tutti i computer IPv6 siano connessi direttamente tramite Ethernet o 6 su 4. L'indirizzo IPv4 instradabile a livello globale deve essere assegnato a uno dei computer che eseguono il protocollo IPv6 Microsoft. Questo computer sarà il gateway 6to4.

Se si dispone di un indirizzo IPv4 che fa parte dello spazio indirizzi privato (10.0.0.0/8, 172.16.0.0/12 o 192.168.0.0/16) o lo spazio degli indirizzi APIPA (Automatic Private IP Addressing) di 169.254.0.0/16 usato da Windows 2000, non è instradabile a livello globale. In caso contrario, è probabilmente un indirizzo IP pubblico ed è instradabile a livello globale. Per altre informazioni su come determinare se la connessione ISP supporta [6to4,](#debugging-6to4-configuration) vedere l'argomento Debug della configurazione 6to4 in questo documento.

## <a name="the-6to4cfgexe-tool"></a>Strumento 6to4cfg.exe

Lo 6to4cfg.exe consente di automatizzare la configurazione 6to4, individuando automaticamente l'indirizzo IPv4 instradabile a livello globale e creando un prefisso 6to4. Esegue direttamente la configurazione oppure può scrivere uno script di configurazione che è possibile esaminare ed eseguire in un secondo momento.

La sintassi 6to4cfg.exe comando di base è la seguente.

``` syntax
6to4cfg [-r] [-s] [-u] [-R relay] [-b] [-S address] [filename]
```

<dl> <dt>

<span id="_filename_"></span><span id="_FILENAME_"></span>\[*Filename*\]
</dt> <dd>

Scrive lo script di configurazione in un file, se si specifica un nome file. Lo script di configurazione usa Ipv6.exe.

È possibile specificare con per il nome file per scrivere lo script di configurazione nell'output della console, utile per visualizzare le 6to4cfg.exe in uno scenario di test.

Se non si specifica un nome file, 6to4cfg.exe aggiornare direttamente la configurazione IPv6 nel computer.

</dd> <dt>

<span id="-r"></span><span id="-R"></span>-r
</dt> <dd>

Diventa un router gateway 6to4 per la rete locale, abilitando il routing su tutte le interfacce e i prefissi di subnet assegnati.

</dd> <dt>

<span id="-s"></span><span id="-S"></span>-s
</dt> <dd>

Abilita l'indirizzamento locale del sito nel sito 6to4. Questo comando è utile solo se usato in combinazione con -r.

</dd> <dt>

<span id="-u"></span><span id="-U"></span>-u
</dt> <dd>

Specifica che la configurazione 6to4 deve essere inversa. Pertanto, 6to4cfg -u inverte l'effetto di 6to4cfg e 6to4cfg -r -u inverte l'effetto di 6to4cfg -r e così via.

</dd> <dt>

<span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>Inoltro *-R*
</dt> <dd>

Specifica il nome o l'indirizzo IPv4 di un router di inoltro 6to4. Il nome predefinito è 6to4.ipv6.microsoft.com router di inoltro 6to4 su Internet.

</dd> <dt>

<span id="-b"></span><span id="-B"></span>-b
</dt> <dd>

Specifica che 6to4cfg.exe l'indirizzo di inoltro "migliore" anziché il primo.

</dd> <dt>

<span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>-S *indirizzo*
</dt> <dd>

Specifica l'indirizzo IPv4 locale per il prefisso 6to4.

</dd> </dl>

## <a name="manual-6to4-configuration"></a>Configurazione manuale 6to4

In questo esempio l'indirizzo del gateway 6to4 è 172.31.42.239. Per usare 6to4 è necessario un indirizzo IPv4 instradabile a livello globale.

> [!Note]  
> L'indirizzo IP 172.31.42.239 viene usato solo a scopo di esempio. Si tratta di un indirizzo privato e non è instradabile a livello globale su Internet.

 

L'indirizzo IPv4 instradabile a livello globale a 32 bit viene combinato con il prefisso a 16 bit 2002::/16 per formare un prefisso di indirizzo IPv6 a 48 bit per il sito. In questo esempio il prefisso del sito 6to4 è 2002:ac1f:2aef::/48. Si noti che ac1f:2aef è la codifica esadecimale di 172.31.42.239 (naturalmente, si userà un prefisso diverso in base al proprio indirizzo IPv4 instradabile a livello globale). Usando il prefisso del sito 6to4, è possibile assegnare indirizzi e prefissi di subnet all'interno del sito.

Questo esempio presuppone che si usi la subnet 0 per configurare manualmente un indirizzo 6to4 nel computer gateway 6to4 e che si usi la subnet 1 per la configurazione automatica degli indirizzi nel segmento di rete Ethernet. Tuttavia, sono possibili altre scelte.

1.  Usare Ipv6.exe per abilitare 6to4 nel computer gateway 6to4:

    **ipv6 rtu 2002::/16 2**

    Il **comando ipv6 rtu** esegue un aggiornamento della tabella di routing. Può essere usato per aggiungere, rimuovere o aggiornare una route. In questo caso abilita 6to4.

    L'argomento 2002::/16 è il prefisso della route, specificando il prefisso 6to4 univoco.

    L'argomento 2 specifica l'interfaccia on-link per questo prefisso. \#L'interfaccia 2 è la "pseudo-interfaccia" usata per tunnel configurati, tunneling automatico e 6to4. Quando un indirizzo di destinazione IPv6 corrisponde al prefisso 2002::/16, i 32 bit che seguono il prefisso nell'indirizzo di destinazione vengono estratti per formare un indirizzo di destinazione IPv4. Il pacchetto viene incapsulato con un'intestazione IPv4 e inviato all'indirizzo di destinazione IPv4.

2.  Configurare un indirizzo 6to4 nel computer gateway 6to4:

    **ipv6 adu 2/2002:ac1f:2aef::ac1f:2aef::ac1f:2aef**

    Il **comando ipv6 adu** esegue un aggiornamento dell'indirizzo. Può essere usato per aggiungere, rimuovere o aggiornare un indirizzo in un'interfaccia. In questo caso, sta configurando l'indirizzo 6to4 del computer.

    L'argomento 2/2002:ac1f:2aef::ac1f:2aef specifica sia l'interfaccia che l'indirizzo. È necessario configurare l'indirizzo 2002:ac1f:2aef::ac1f:2aef \# sull'interfaccia 2. L'indirizzo viene creato usando il prefisso del sito 2002:ac1f:2aef::/48, la subnet 0 per assegnare un prefisso di subnet 2002:ac1f:2aef::/64 e un identificatore di interfaccia a 64 bit. La convenzione illustrata usa l'indirizzo IPv4 del computer per l'identificatore di interfaccia per gli indirizzi assegnati \# all'interfaccia 2. Per l'uso, ac1f:2aef deve essere sostituito dalla codifica esadecimale del proprio indirizzo IPv4 instradabile a livello globale.

I due comandi precedenti sono sufficienti per consentire la comunicazione con altri siti 6to4. Ad esempio, è possibile provare a eseguire il ping del sito di Microsoft 6to4:

**ping6 2002:836b:9820::836b:9820**

Per abilitare la comunicazione con il 6bone, è necessario creare un tunnel configurato predefinito per un inoltro 6to4. È possibile usare il router di inoltro Microsoft 6to4, 131.107.152.32:

**ipv6 rtu ::/0 2/::131.107.152.32 pub life 1800**

Il **comando ipv6 rtu** esegue un aggiornamento della tabella di routing, stabilendo, in questo caso, una route predefinita per l'inoltro 6to4.

L'argomento ::/0 è il prefisso della route. Il prefisso di lunghezza zero indica che si tratta di una route predefinita.

L'argomento 2/::131.107.152.32 specifica l'hop successivo adiacente per questo prefisso. È necessario che i pacchetti corrispondenti al prefisso siano inoltrati all'indirizzo ::131.107.152.32 usando \# l'interfaccia 2. L'inoltro di un pacchetto a ::131.107.152.32 sull'interfaccia 2 ne determina l'incapsulamento con un'intestazione v4 e l'invio a \# 131.107.152.32.

L'argomento pub rende questa route pubblicata. Poiché è rilevante solo per i router, non ha alcun effetto fino a quando non viene abilitato il routing. Analogamente, la durata di 30 minuti riguarda solo se il routing è abilitato.

Dovrebbe essere possibile accedere ai siti 6bone e 6to4. Per testare questa operazione, è possibile usare il comando seguente:

**ping6 3ffe:1cff:0:f5::1**

Il passaggio finale consiste nell'abilitare il routing nel gateway 6to4. Questo esempio presuppone che l'interfaccia 3 nel computer gateway sia un'interfaccia Ethernet e che l'interfaccia \# \# 4 sia 6 su 4. Il computer potrebbe numerare le interfacce in modo diverso. I due comandi seguenti assegnano i prefissi di subnet ai due collegamenti. I prefissi di subnet derivano dal prefisso 6to4 del sito 2002:ac1f:2aef::/48:

**ipv6 rtu 2002:ac1f:2aef:1::/64 3 pub life 1800**

**ipv6 rtu 2002:ac1f:2aef:2::/64 4 pub life 1800**

Il **comando ipv6 rtu** specifica che il prefisso 2002:ac1f:2aef:1::/64 è in collegamento all'interfaccia \# 3. Sta configurando il primo prefisso di subnet nell'interfaccia Ethernet. La route viene pubblicata con una durata di 30 minuti.

Analogamente, il prefisso 2002:ac1f:2aef:2::/64 viene configurato nell'interfaccia 6-over-4.

I tre comandi successivi consentono al computer gateway 6to4 di funzionare come router:

**ipv6 ifc 2 forw**

**ipv6 ifc 3 forw adv**

**ipv6 ifc 4 forw adv**

Il **comando ifc ipv6** controlla gli attributi di un'interfaccia. Un router inoltra i pacchetti e invia annunci router. Nell'implementazione microsoft IPv6 questi attributi per interfaccia vengono controllati separatamente.

\#L'interfaccia 2 non è necessaria per la pubblicità perché è una pseudo-interfaccia.

Se il computer dispone di interfacce aggiuntive, devono essere configurate anche per l'inoltro e la pubblicità.

Dopo aver eseguito questi comandi, il protocollo Microsoft IPv6 configurerà automaticamente gli indirizzi nelle interfacce 3 e 4 usando i rispettivi prefissi di subnet e le due interfacce inizieranno a inviare annunci router a intervalli da 3 a \# \# 10 minuti circa.

Gli host che ricevono questi annunci router si configureranno automaticamente con una route predefinita e un indirizzo 6to4 derivato dal prefisso della subnet del collegamento. Avranno la comunicazione con altri siti 6to4 e il 6bone tramite il computer gateway.

## <a name="debugging-6to4-configuration"></a>Debug della configurazione 6to4

**Per eseguire il debug della configurazione 6to4**

1.  Controllare la connettività IPv4 al router di inoltro 6to4:

    **ping 6to4.ipv6.microsoft.com**

    Se l'operazione non riesce, la connettività Internet globale non è disponibile.

2.  Controllare l'incapsulamento IPv6 tramite tunneling automatico:

    **ping6 ::131.107.152.32**

    In caso di errore, potrebbe essere presente un firewall o nat (Network Address Translator) tra il computer e Internet. Se l'operazione ha esito positivo, la connessione Internet può supportare 6to4.

3.  Controllare la visualizzazione del comando ipv6 rt. Verrà visualizzata una route 2002::/16 -> 2. Controllare la visualizzazione del comando ipv6 se 2. Verrà visualizzato un indirizzo preferito con un prefisso 2002::/16.

> [!Note]  
> L'indirizzo IPv4 del router di inoltro Microsoft 6to4 131.107.152.32 è soggetto a modifiche. Se il passaggio 2 precedente non funziona, controllare l'output del comando ping nel passaggio 1 per verificare l'indirizzo IPv4 del router di inoltro Microsoft 6to4.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazioni consigliate per IPv6](recommended-configurations-2.md)
</dt> <dt>

[Subnet singola con indirizzi locali di collegamento](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[Uso di IPsec tra due host di collegamento locale](configuration-4-using-ipsec-between-two-local-link-hosts-2.md)
</dt> </dl>

 

 



