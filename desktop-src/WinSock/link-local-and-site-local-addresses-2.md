---
description: Gli indirizzi IPv6 link-local e site-local sono denominati indirizzi con ambito.
ms.assetid: d31882f6-b747-47c7-83cb-a9a03fe11cb8
title: Indirizzi IPv6 link-local e site-local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22220adb2c1b0338462f7ed87b3937a97c3d0b8a8b0aa2d9858d5c5efc8b4f54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794781"
---
# <a name="ipv6-link-local-and-site-local-addresses"></a>Indirizzi IPv6 link-local e site-local

Gli indirizzi IPv6 link-local e site-local sono denominati indirizzi con ambito. L'API Windows Sockets (Winsock) supporta il membro **\_ \_ ID** ambito sin6 nella struttura [**sockaddr \_ in6**](sockaddr-2.md) per l'uso con indirizzi con ambito. Per gli indirizzi locali di collegamento IPv6 (prefisso fe80::/10), il membro **\_ \_ ID** ambito sin6 nella struttura **sockaddr \_ in6** è il numero di interfaccia. Per gli indirizzi locali del sito IPv6 (prefisso fec0::/10), il membro **\_ \_ ID** ambito sin6 nella struttura **sockaddr \_ in6** è un identificatore del sito.

Un esempio di indirizzo IPv6 locale di collegamento \# sull'interfaccia 5 è il seguente:

``` syntax
fe80::208:74ff:feda:625c%5
```

Il comando seguente è disponibile in Windows XP con Service Pack 1 (SP1) e versioni successive per eseguire query e configurare IPv6 in un computer locale:

-   [Netsh.exe](netsh-exe.md)

Le modifiche di configurazione apportate Netsh.exe comandi sono permanenti e non vengono perse al riavvio del computer o del protocollo IPv6.

Prima di Windows XP con Service Pack 1 (SP1), la configurazione e la gestione IPv6 usava diversi strumenti da riga di comando meno recenti (Net.exe, Ipv6.exe e Ipsec6.exe) per configurare e gestire IPv6. Usando questi strumenti precedenti, le modifiche IPv6 non sono permanenti e vengono perse quando il computer o il protocollo IPv6 è stato riavviato. Questi strumenti da riga di comando precedenti sono supportati solo in Windows XP.

In Windows XP con SP1, il comando seguente visualizza l'elenco delle interfacce IPv6 in un computer locale, inclusi l'indice dell'interfaccia, il nome dell'interfaccia e varie altre proprietà dell'interfaccia.

**Interfaccia netsh ipv6 show interface**

In Windows XP con SP1, il comando seguente modificherà l'identificatore del sito associato a un indice di interfaccia.

**netsh interface ipv6 set interface <InterfaceIndex or Name> siteid=value**

In Windows XP, il comando precedente seguente modifica anche l'identificatore del sito associato a un indirizzo locale del sito in 3.

**ipv6 rtu fec0::/10 3**

Se si invia o si esegue la connessione a un indirizzo con ambito, il membro ID ambito **sin6 \_ \_** nella struttura [**sockaddr \_ in6**](sockaddr-2.md) può essere lasciato non specificato (zero) che rappresenta un indirizzo con ambito ambiguo. Ad esempio, l'indirizzo locale del collegamento seguente è ambiguo:

``` syntax
fe80::10
```

Se si sta associando a un indirizzo con ambito, il membro ID ambito **sin6 \_ \_** nella struttura [**sockaddr \_ in6**](sockaddr-2.md) deve contenere un valore diverso da zero che specifica un numero di interfaccia valido per un indirizzo locale del collegamento o un identificatore del sito per un indirizzo locale del sito.

## <a name="ambiguous-scoped-addresses"></a>Indirizzi con ambito ambiguo

Se si invia o si esegue la connessione a un indirizzo con ambito e non è stato specificato il membro ID ambito **sin6 \_ \_** nella struttura [**sockaddr \_ in6,**](sockaddr-2.md) l'indirizzo con ambito è ambiguo. Per risolvere questo problema, il protocollo IPv6 determina innanzitutto se il socket è stato associato a un indirizzo di origine. In tal caso, l'indirizzo di origine associato risolve l'ambiguità fornendo un numero di interfaccia o un identificatore del sito.

Se si sta inviando o ci si connette a un indirizzo con ambito e non è stato specificato il membro ID ambito **sin6 \_ \_** né è stato associato un indirizzo di origine, il protocollo IPv6 controlla la tabella di routing. Ad esempio, il comando seguente visualizza la tabella di routing IPv6 in un computer locale:

**netsh interface ipv6 show route**

``` syntax
No   Manual   256  fe80::/64      13  Local Area Connection
No   Manual   256  fe80::/64      14  Wireless Network Connection
```

Ciò indica che gli indirizzi locali del collegamento vengono considerati come collegamento all'interfaccia \# 13 e \# 14 per impostazione predefinita.

L'ambiguità si verifica quando un computer locale ha più schede di rete. Ad esempio, il **comando netsh** precedente indica che sono presenti due interfacce di rete (Connessione alla rete locale e Connessione di rete wireless). Quando un'applicazione specifica un indirizzo locale di collegamento di destinazione (ad esempio fe80::10) senza un ID ambito, non è chiaro quale adattatore usare per inviare il pacchetto. Solo un unicast locale di collegamento (fe80::/64) o un indirizzo di destinazione IPv6 con ambito di collegamento (ff00::/8) può non avere un ID ambito durante l'invio di un pacchetto.

## <a name="neighbor-discovery"></a>Individuazione router adiacenti

Se non è stato specificato il membro id ambito **sin6 \_ \_** nella struttura [**sockaddr \_ in6,**](sockaddr-2.md) non è stato associato un indirizzo di origine e non è stata specificata una route per gli indirizzi locali del collegamento, il protocollo IPv6 tenterà l'individuazione adiacente per risolvere l'indirizzo locale del collegamento di destinazione. Per un determinato pacchetto inviato, viene tentata un'interfaccia. Questa prima interfaccia che viene tentata è considerata l'interfaccia più preferita. Se l'individuazione adiacente non riesce a risolvere l'indirizzo locale del collegamento in un'interfaccia, il pacchetto da inviare viene eliminato e il sistema ricorda che l'indirizzo locale del collegamento di destinazione non è raggiungibile su tale interfaccia. Nel pacchetto successivo da inviare in tutte le stesse condizioni, viene tentata un'interfaccia diversa per l'individuazione adiacente. Questo processo continua attraverso ogni interfaccia in un computer locale per ogni nuovo pacchetto fino a quando l'individuazione adiacente non risponde per l'indirizzo locale del collegamento di destinazione o tutte le interfacce possibili sono state tentate e non sono state tentate. Ogni volta che un tentativo di risolvere il router adiacente ha esito negativo, viene eliminata un'interfaccia per tale adiacente.

Se l'indirizzo link-local di destinazione viene risolto, tale interfaccia viene usata per inviare il pacchetto corrente. Questa interfaccia viene usata anche per eventuali pacchetti con ambito ambiguo successivi inviati allo stesso indirizzo di destinazione locale del collegamento.

Se l'individuazione adiacente non riesce a risolvere l'indirizzo locale del collegamento di destinazione in tutte le interfacce, il sistema prova a inviare il pacchetto sull'interfaccia preferita (la prima interfaccia è stata tentata). Lo stack di rete continua a tentare di risolvere l'indirizzo locale del collegamento di destinazione nell'interfaccia preferita. Dopo un periodo di tempo dopo che l'individuazione adiacente non è riuscita in tutte le interfacce, lo stack di rete riavvierà nuovamente il processo e tenterà di risolvere l'indirizzo locale del collegamento di destinazione in tutte le interfacce. Attualmente, questo intervallo di tempo in cui l'individuazione adiacente viene nuovamente tentata su tutte le interfacce è di 60 secondi. Tuttavia, questo intervallo di tempo può cambiare nelle versioni Windows e non deve essere assunto da un'applicazione.

> [!Note]  
> Se un'applicazione associa lo stesso indirizzo locale del collegamento a un'interfaccia diversa dopo che l'individuazione adiacente ha risolto l'indirizzo locale del collegamento, l'interfaccia non eseguirà l'override dell'interfaccia con l'indirizzo di destinazione locale del collegamento restituito dall'individuazione adiacente.

 

Per altre informazioni su Neighbor Discovery per IP versione 6, vedere [RFC4861](https://tools.ietf.org/html/rfc4861) pubblicato da IETF.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Prefissi del sito IPv6](site-prefixes-2.md)
</dt> <dt>

[Ipv6.exe](ipv6-exe-2.md)
</dt> <dt>

[Netsh.exe](netsh-exe.md)
</dt> <dt>

[Utilizzo di IPv6](using-ipv6-2.md)
</dt> </dl>

 

 



