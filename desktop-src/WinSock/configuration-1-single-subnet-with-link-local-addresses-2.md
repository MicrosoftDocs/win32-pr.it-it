---
description: Per la prima configurazione non è necessaria alcuna configurazione aggiuntiva oltre all'installazione del protocollo Microsoft IPv6 Technology Preview.
ms.assetid: ceed4983-e088-44e8-9cfc-26afb3c35ba0
title: 'Configurazione 1: singola subnet con indirizzi locali rispetto al collegamento'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d09feb44c222b7213da18a6745fc632f3903209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049490"
---
# <a name="configuration-1-single-subnet-with-link-local-addresses"></a>Configurazione 1: singola subnet con indirizzi locali rispetto al collegamento

Per la prima configurazione non è necessaria alcuna configurazione aggiuntiva oltre all'installazione del protocollo Microsoft IPv6 Technology Preview. Questa configurazione è costituita da almeno due nodi nella stessa subnet. Nella terminologia IPv6, i due nodi si trovano nello stesso collegamento senza router intermedi.

Nella figura seguente viene illustrata la configurazione di due nodi in una singola subnet usando indirizzi locali al collegamento.

![due nodi che usano indirizzi locali al collegamento.](images/v6mig-1.png)

Per impostazione predefinita, IPv6 configura indirizzi IP locali al collegamento per ogni interfaccia corrispondente a schede di rete Ethernet installate. Gli indirizzi locali al collegamento hanno il prefisso FE80::/64. Gli ultimi 64 bit dell'indirizzo IPv6 sono noti come identificatori di interfaccia ed è derivato dall'indirizzo MAC a 48 bit della scheda di rete.

Per creare l'identificatore di interfaccia IPv6 dall'indirizzo MAC Ethernet a 48 bit (6 byte):

-   Le cifre esadecimali 0xFF-Fe vengono inserite tra il terzo e il quarto byte dell'indirizzo MAC.
-   Il bit universale/locale, il secondo bit di ordine inferiore del primo byte dell'indirizzo MAC, è complementare. Se è 1, viene convertito in 0 e, se è 0, viene trasformato in 1.

Ad esempio, per l'indirizzo MAC 00-60-08-52-F9-D8:

-   Le cifre esadecimali 0xFF-Fe vengono inserite tra 0x08 (il terzo byte) e 0x52 (il quarto byte) dell'indirizzo MAC, formando l'indirizzo 64 bit 00-60-08-FF-FE-52-F9-D8.
-   Il bit universale/locale, il secondo bit di ordine inferiore di 0x00 (il primo byte) dell'indirizzo MAC è complementare. Il secondo bit di ordine inferiore di 0x00 è 0 che, quando complementato, diventa 1. Il risultato è che, per il primo byte, 0x00 diventa 0x02.

Pertanto, l'identificatore di interfaccia IPv6 corrispondente all'indirizzo MAC Ethernet 00-60-08-52-F9-D8 è 02-60-08-FF-FE-52-F9-D8.

L'indirizzo locale del collegamento di un nodo è la combinazione del prefisso FE80::/64 e dell'identificatore di interfaccia a 64 bit espresso nella notazione esadecimale con due punti IPv6. Pertanto, l'indirizzo locale rispetto al collegamento del nodo di esempio con il prefisso FE80::/64 e l'identificatore di interfaccia 02-60-08-FF-FE-52-F9-D8 è FE80:: 260:8FF: FE52: F9D8.

È possibile visualizzare l'indirizzo locale del collegamento usando IPv6 se, come illustrato nell'esempio seguente:

**IPv6 se**

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

Interfaccia 4 è un'interfaccia corrispondente a una scheda Ethernet installata con un indirizzo locale rispetto al collegamento FE80:: 210:5AFF: FEAA: 20A2.

Per ulteriori informazioni sull'indirizzamento IPv6 e una panoramica dei concetti relativi a IPv6, vedere Introduzione a IPv6 white paper.

## <a name="testing-connectivity-between-two-link-local-hosts"></a>Test della connettività tra due host locali di collegamento

È possibile eseguire un semplice ping (uno scambio di messaggi di richiesta echo ICMPv6 e di risposta echo) usando IPv6 tra due host locali al collegamento.

**Per eseguire il ping usando IPv6 tra due host locali al collegamento**

1.  Installare Microsoft IPv6 Technology Preview per Windows in due host Windows (host A e host B) che si trovano nello stesso collegamento (subnet).
2.  Usare IPv6 se sull'host a per ottenere l'indirizzo locale del collegamento per l'interfaccia Ethernet.

    Esempio: l'indirizzo locale del collegamento dell'host A è FE80:: 210:5AFF: FEAA: 20A2.

3.  Usare IPv6 se sull'host B per ottenere l'indirizzo locale del collegamento per l'interfaccia Ethernet.

    Esempio: l'indirizzo locale del collegamento dell'host B è FE80:: 260:97FF: FE02:6EA5.

4.  Dall'host A eseguire il ping dell'host B utilizzando Ping6.exe.

    Esempio: ping6 FE80:: 260:97FF: FE02:6EA5

Per specificare l'indirizzo di origine da cui vengono inviati i messaggi di richiesta echo, è anche possibile usare l'opzione Ping6.exe-s. Ad esempio, per inviare richieste echo all'host B dall'indirizzo IPv6 di FE80:: 210:5AFF: FEAA: 20A2, usare il comando seguente:

**ping6-s FE80:: 210:5AFF: FEAA: 20A2% 4 FE80:: 260:97FF: FE02:6EA5**

Quando si esegue il ping di un indirizzo locale rispetto al collegamento o al sito, è consigliabile specificare l'ID ambito in modo che l'indirizzo di destinazione non sia ambiguo. La notazione per specificare l'ID ambito è Address% scope-ID. Per gli indirizzi locali al collegamento, l'ID ambito è uguale al numero di interfaccia visualizzato nel comando IPv6 if. Per gli indirizzi locali del sito, l'ID ambito è uguale al numero del sito come visualizzato nel comando IPv6 if. Ad esempio, per inviare messaggi di richiesta echo all'host B utilizzando l'ID ambito 4, utilizzare il comando seguente:

**ping6 FE80:: 260:97FF: FE02:6EA5% 4**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazioni consigliate per IPv6](recommended-configurations-2.md)
</dt> </dl>

 

 



