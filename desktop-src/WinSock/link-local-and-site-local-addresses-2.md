---
description: Gli indirizzi IPv6 locali e locali del sito sono denominati indirizzi con ambito.
ms.assetid: d31882f6-b747-47c7-83cb-a9a03fe11cb8
title: Collegamento IPv6-indirizzi locali e locali del sito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80b8e201adf382b10dd31fe5607de903d6c588
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306936"
---
# <a name="ipv6-link-local-and-site-local-addresses"></a>Collegamento IPv6-indirizzi locali e locali del sito

Gli indirizzi IPv6 locali e locali del sito sono denominati indirizzi con ambito. L'API Windows Sockets (Winsock) supporta il membro **\_ \_ ID ambito sin6** nella [**struttura \_ IN6 di SOCKADDR**](sockaddr-2.md) per l'utilizzo con gli indirizzi con ambito. Per gli indirizzi di collegamento IPv6 (prefisso FE80::/10), il membro dell' **\_ \_ ID ambito sin6** nella **struttura \_ IN6 sockaddr** è il numero di interfaccia. Per gli indirizzi IP locali del sito IPv6 (prefisso FEC0::/10), il membro dell' **\_ \_ ID ambito sin6** nella struttura **sockaddr \_ IN6** è un identificatore di sito.

Di seguito è riportato un esempio di indirizzo IPv6 locale al collegamento nell'interfaccia \# 5:

``` syntax
fe80::208:74ff:feda:625c%5
```

Il seguente comando è disponibile in Windows XP con Service Pack 1 (SP1) e versioni successive per eseguire query e configurare IPv6 in un computer locale:

-   [Netsh.exe](netsh-exe.md)

Le modifiche di configurazione apportate utilizzando i comandi Netsh.exe sono permanenti e non vengono perse quando il computer o il protocollo IPv6 viene riavviato.

Prima di Windows XP con Service Pack 1 (SP1), la gestione e la configurazione di IPv6 utilizzavano diversi strumenti da riga di comando precedenti (Net.exe, Ipv6.exe e Ipsec6.exe) per la configurazione e la gestione di IPv6. Utilizzando questi strumenti obsoleti, le modifiche IPv6 non sono permanenti e vengono perse quando il computer o il protocollo IPv6 è stato riavviato. Questi strumenti da riga di comando precedenti sono supportati solo in Windows XP.

In Windows XP con SP1, il comando seguente visualizzerà l'elenco delle interfacce IPv6 in un computer locale, tra cui l'indice dell'interfaccia, il nome dell'interfaccia e diverse altre proprietà dell'interfaccia.

**netsh interface ipv6 show interface**

In Windows XP con SP1, il comando seguente modifica l'identificatore del sito associato a un indice di interfaccia.

**netsh interface ipv6 set interface <InterfaceIndex or Name> siteID = value**

In Windows XP il seguente comando precedente comporterà anche la modifica dell'identificatore del sito associato a un indirizzo locale del sito a 3.

**FEC0 RTU per IPv6::/10 3**

Se si invia o si connette a un indirizzo con ambito, il membro **dell' \_ \_ ID ambito sin6** nella struttura [**\_ IN6 di SOCKADDR**](sockaddr-2.md) può essere lasciato non specificato (zero) che rappresenta un indirizzo con ambito ambiguo. Ad esempio, il seguente indirizzo locale rispetto al collegamento è ambiguo:

``` syntax
fe80::10
```

Se si sta associando a un indirizzo con ambito, il membro dell' **\_ \_ ID ambito sin6** nella struttura [**sockaddr \_ IN6**](sockaddr-2.md) deve contenere un valore diverso da zero che specifica un numero di interfaccia valido per un indirizzo locale del collegamento o un identificatore di sito per un indirizzo locale del sito.

## <a name="ambiguous-scoped-addresses"></a>Indirizzi con ambito ambiguo

Se si sta inviando o eseguendo la connessione a un indirizzo con ambito e non è stato specificato il membro dell' **\_ \_ ID ambito sin6** nella struttura [**\_ IN6 di SOCKADDR**](sockaddr-2.md) , l'indirizzo con ambito è ambiguo. Per risolvere questo problema, il protocollo IPv6 determina innanzitutto se il socket è stato associato a un indirizzo di origine. In tal caso, l'indirizzo di origine associato risolve l'ambiguità fornendo un numero di interfaccia o un identificatore di sito.

Se si sta inviando o connettendosi a un indirizzo con ambito e non è stato specificato il membro dell' **\_ \_ ID ambito sin6** né associato un indirizzo di origine, il protocollo IPv6 controlla la tabella di routing. Il comando seguente, ad esempio, visualizzerà la tabella di routing IPv6 in un computer locale:

**netsh interface ipv6 show route**

``` syntax
No   Manual   256  fe80::/64      13  Local Area Connection
No   Manual   256  fe80::/64      14  Wireless Network Connection
```

Ciò indica che gli indirizzi locali al collegamento vengono considerati come on-link per l'interfaccia \# 13 e \# 14 per impostazione predefinita.

L'ambiguità si verifica quando un computer locale dispone di più schede di rete. Ad esempio, il comando **netsh** precedente indica che sono presenti due interfacce di rete (connessione alla rete locale e connessione di rete wireless). Quando un'applicazione specifica un indirizzo locale del collegamento di destinazione (ad esempio, FE80:: 10) senza un ID ambito, non è chiaro quale adapter usare per inviare il pacchetto. Quando si invia un pacchetto, solo un indirizzo unicast locale del collegamento (FE80::/64) o un indirizzo di destinazione multicast con ambito di collegamento (FF00::/8) non può soffrire di un ID ambito.

## <a name="neighbor-discovery"></a>Individuazione router adiacenti

Se non è stato specificato il membro dell' **\_ \_ ID ambito sin6** nella [**struttura \_ IN6 di SOCKADDR**](sockaddr-2.md) , non è stato associato un indirizzo di origine e non è stata specificata una route per gli indirizzi locali al collegamento, il protocollo IPv6 tenterà l'individuazione Neighbor per risolvere l'indirizzo locale del collegamento di destinazione. Per un pacchetto specifico inviato, viene tentata un'interfaccia. Questa prima interfaccia tentata è considerata l'interfaccia più preferita. Se l'individuazione vicina non riesce a risolvere l'indirizzo locale rispetto al collegamento in un'interfaccia, il pacchetto da inviare viene eliminato e il sistema ricorda che l'indirizzo locale del collegamento di destinazione non è raggiungibile tramite tale interfaccia. Nel pacchetto successivo da inviare in tutte le stesse condizioni, viene tentata un'interfaccia diversa per l'individuazione dei router adiacenti. Questo processo continua con ognuna delle interfacce in un computer locale per ogni nuovo pacchetto fino a quando non viene rilevata l'individuazione vicina per l'indirizzo locale del collegamento di destinazione o se tutte le interfacce possibili sono state tentate e non sono riuscite. Ogni volta che un tentativo di risolvere il router adiacente ha esito negativo, viene eliminata un'interfaccia per quel router adiacente.

Se l'indirizzo locale del collegamento di destinazione viene risolto, l'interfaccia viene usata per inviare il pacchetto corrente. Questa interfaccia viene usata anche per tutti i successivi pacchetti con ambito ambiguo che vengono inviati allo stesso indirizzo di destinazione locale rispetto al collegamento.

Se l'individuazione router adiacenti non riesce a risolvere l'indirizzo locale del collegamento di destinazione su tutte le interfacce, il sistema tenta di inviare il pacchetto sull'interfaccia preferita (la prima interfaccia è stata tentata). Lo stack di rete continua a provare a risolvere l'indirizzo locale del collegamento di destinazione sull'interfaccia più preferita. Dopo un periodo di tempo in cui l'individuazione dei router adiacenti ha avuto esito negativo su tutte le interfacce, lo stack di rete riavvierà nuovamente il processo e tenterà di risolvere l'indirizzo locale del collegamento di destinazione su tutte le interfacce. Attualmente, questo intervallo di tempo quando l'individuazione del router adiacente viene nuovamente tentata su tutte le interfacce è di 60 secondi. Tuttavia, questo intervallo di tempo può cambiare nelle versioni di Windows e non deve essere presupposto da un'applicazione.

> [!Note]  
> Se un'applicazione associa lo stesso indirizzo locale al collegamento a un'interfaccia diversa dopo che l'individuazione del router adiacente ha risolto l'indirizzo locale rispetto al collegamento, che non eseguirà l'override dell'interfaccia con l'indirizzo di destinazione locale del collegamento restituito dall'individuazione vicina.

 

Per ulteriori informazioni sull'individuazione dei router adiacenti per IP versione 6, vedere [RFC4861](https://tools.ietf.org/html/rfc4861) pubblicato da IETF.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Prefissi di sito IPv6](site-prefixes-2.md)
</dt> <dt>

[Ipv6.exe](ipv6-exe-2.md)
</dt> <dt>

[Netsh.exe](netsh-exe.md)
</dt> <dt>

[Utilizzo di IPv6](using-ipv6-2.md)
</dt> </dl>

 

 



