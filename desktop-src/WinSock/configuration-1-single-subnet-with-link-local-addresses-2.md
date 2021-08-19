---
description: La prima configurazione non richiede alcuna configurazione aggiuntiva oltre all'installazione del protocollo Microsoft IPv6 Technology Preview.
ms.assetid: ceed4983-e088-44e8-9cfc-26afb3c35ba0
title: 'Configurazione 1: subnet singola con indirizzi locali di collegamento'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a541edd96175dc61ec0aba3b1358c2bbd9464668e6aa1a11aeb6f2097e5b13bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051735"
---
# <a name="configuration-1-single-subnet-with-link-local-addresses"></a>Configurazione 1: subnet singola con indirizzi locali di collegamento

La prima configurazione non richiede alcuna configurazione aggiuntiva oltre all'installazione del protocollo Microsoft IPv6 Technology Preview. Questa configurazione è costituita da almeno due nodi nella stessa subnet. Nella terminologia IPv6, i due nodi sono sullo stesso collegamento senza router intermedi.

La figura seguente illustra la configurazione di due nodi in una singola subnet usando indirizzi locali di collegamento.

![due nodi che usano indirizzi locali di collegamento.](images/v6mig-1.png)

Per impostazione predefinita, IPv6 configura gli indirizzi IP locali del collegamento per ogni interfaccia corrispondente alle schede di rete Ethernet installate. Gli indirizzi locali del collegamento hanno il prefisso fe80::/64. Gli ultimi 64 bit dell'indirizzo IPv6 sono noti come identificatore di interfaccia ed è derivato dall'indirizzo MAC a 48 bit della scheda di rete.

Per creare l'identificatore di interfaccia IPv6 dall'indirizzo MAC Ethernet a 48 bit (6 byte):

-   Le cifre esadecimali 0xff-fe vengono inserite tra il terzo e il quarto byte dell'indirizzo MAC.
-   Il bit universale/locale, il secondo bit meno significativo del primo byte dell'indirizzo MAC, è complementare. Se è 1, viene impostata su 0 e, se è 0, viene impostata su 1.

Ad esempio, per l'indirizzo MAC 00-60-08-52-f9-d8:

-   Le cifre esadecimali 0xff-fe vengono inserite tra 0x08 (terzo byte) e 0x52 (il quarto byte) dell'indirizzo MAC, formando l'indirizzo a 64 bit 00-60-08-ff-fe-52-f9-d8.
-   Il bit universale/locale, il secondo bit meno significativo 0x00 (il primo byte) dell'indirizzo MAC è complementare. Il secondo bit meno importante di 0x00 è 0 che, se integrato, diventa 1. Il risultato è che per il primo byte, 0x00 diventa 0x02.

Pertanto, l'identificatore di interfaccia IPv6 corrispondente all'indirizzo MAC Ethernet di 00-60-08-52-f9-d8 è 02-60-08-ff-fe-52-f9-d8.

L'indirizzo locale del collegamento di un nodo è la combinazione del prefisso fe80::/64 e dell'identificatore di interfaccia a 64 bit espresso nella notazione i due punti-esadecimale IPv6. Di conseguenza, l'indirizzo locale di collegamento di questo nodo di esempio con il prefisso fe80::/64 e l'identificatore di interfaccia 02-60-08-ff-fe-52-f9-d8 è fe80::260:8ff:fe52:f9d8.

È possibile visualizzare l'indirizzo locale del collegamento usando ipv6 se, come illustrato nell'esempio seguente:

**ipv6 se**

``` syntax
Interface 4 (site 1): Local Area Connection
  uses Neighbor Discovery
  link-level address: 00-10-5a-aa-20-a2
    preferred address fe80::210:5aff:feaa:20a2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ffaa:20a2, 1 refs, last reporter
  link MTU 1500 (true link MTU 1500)
  current hop limit 128
  reachable time 43500ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 3 (site 1): 6-over-4 Virtual Interface
  uses Neighbor Discovery
  link-level address: 10.0.0.2
    preferred address fe80::a00:2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ff00:2, 1 refs, last reporter
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 34000ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 2 (site 0): Tunnel Pseudo-Interface
  does not use Neighbor Discovery
  link-level address: 0.0.0.0
    preferred address ::10.0.0.2, infinite/infinite
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
Interface 1 (site 0): Loopback Pseudo-Interface
  does not use Neighbor Discovery
  link-level address:
    preferred address ::1, infinite/infinite
  link MTU 1500 (true link MTU 1500)
  current hop limit 1
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
```

L'interfaccia 4 è un'interfaccia corrispondente a una scheda Ethernet installata con indirizzo locale di collegamento fe80::210:5aff:feaa:20a2.

Per altre informazioni sull'indirizzamento IPv6 e una panoramica dei concetti relativi a IPv6, vedere Introduzione a IPv6 white paper.

## <a name="testing-connectivity-between-two-link-local-hosts"></a>Test della connettività tra due host locali del collegamento

È possibile eseguire un semplice ping (uno scambio di messaggi Echo Request e Echo Reply ICMPv6) usando IPv6 tra due host locali del collegamento.

**Per effettuare il ping usando IPv6 tra due host locali del collegamento**

1.  Installare Microsoft IPv6 Technology Preview per Windows in due host Windows (Host A e Host B) nello stesso collegamento (subnet).
2.  Usare ipv6 se nell'Host A per ottenere l'indirizzo locale del collegamento per l'interfaccia Ethernet.

    Esempio: l'indirizzo locale del collegamento dell'host A è fe80::210:5aff:feaa:20a2.

3.  Usare ipv6 se nell'host B per ottenere l'indirizzo locale del collegamento per l'interfaccia Ethernet.

    Esempio: l'indirizzo locale del collegamento dell'host B è fe80::260:97ff:fe02:6ea5.

4.  Dall'host A eseguire il ping dell'host B Ping6.exe.

    Esempio: ping6 fe80::260:97ff:fe02:6ea5

Per specificare l'indirizzo di origine da cui vengono inviati i messaggi Echo Request, è anche possibile usare l'opzione Ping6.exe -s . Ad esempio, per inviare richieste Echo all'host B dall'indirizzo IPv6 fe80::210:5aff:feaa:20a2, usare il comando seguente:

**ping6 -s fe80::210:5aff:feaa:20a2%4 fe80::260:97ff:fe02:6ea5**

Quando si effettua il ping di un indirizzo locale del collegamento o del sito, è consigliabile specificare l'ID ambito per rendere non ambiguo l'indirizzo di destinazione. La notazione per specificare l'ID ambito è address%scope-ID. Per gli indirizzi locali di collegamento, scope-ID è uguale al numero di interfaccia visualizzato nel comando ipv6 if. Per gli indirizzi locali del sito, scope-ID è uguale al numero del sito visualizzato nel comando ipv6 if. Ad esempio, per inviare messaggi Echo Request all'host B usando scope-ID 4, usare il comando seguente:

**ping6 fe80::260:97ff:fe02:6ea5%4**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazioni consigliate per IPv6](recommended-configurations-2.md)
</dt> </dl>

 

 



