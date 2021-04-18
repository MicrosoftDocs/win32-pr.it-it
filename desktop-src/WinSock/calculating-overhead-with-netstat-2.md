---
description: Calcolo del sovraccarico con netstat
ms.assetid: d96a8fba-8d76-443f-be49-81a8ad7050fa
title: Calcolo del sovraccarico con netstat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7843c3cd445bee66e25a9f191ae4b78093faea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307034"
---
# <a name="calculating-overhead-with-netstat"></a>Calcolo del sovraccarico con netstat

Il calcolo del sovraccarico con netstat deve essere eseguito in una rete non interattiva per evitare che il traffico di rete possa inclinare i dati, ad esempio il traffico broadcast o multicast.

**Per calcolare l'overhead di rete di un'applicazione con netstat**

1.  Recuperare le statistiche dell'interfaccia corrente usando netstat.
2.  Eseguire l'applicazione.
3.  Ottenere le statistiche dell'interfaccia usando nuovamente netstat.
4.  Calcolare il numero di byte ricevuti tra le due misure netstat.

## <a name="example"></a>Esempio

Nell'esempio seguente vengono illustrati questi passaggi, utilizzando TTCP per inviare 10 byte di dati, un byte alla volta.

In primo luogo, viene calcolato un sovraccarico teorico per l'applicazione. Per questo test, tutti i pacchetti sono 60 byte (valore minimo Ethernet). Questo trasferimento richiede tre pacchetti per configurare la connessione, 10 pacchetti di dati, 10 pacchetti di riconoscimento (ACK ritardati viene attivato quasi ogni volta) e quattro pacchetti per chiudere la connessione normalmente.

Questa operazione equivale a 27 pacchetti di 60 byte ciascuno o 1620 byte (3 + 4 + 10 + 10) \* 60 = 1620). Poiché vengono trasferiti solo 10 byte di dati, l'overhead è di 1610 byte, che è superiore al 99% del sovraccarico del protocollo.

### <a name="commands"></a>Comandi

**netstat-e**

``` syntax
Interface Statistics
                     Received     Sent
Bytes                392291400    444684566
Unicast packets      487627       570086
Non-unicast packets  1159163      11300
Discards             0            0
Errors               0            0
Unknown protocols    52812
```

**ttcp-t-H0-D-L1-N10-P9 172.31.71.99**

``` syntax
ttcp-t: 10 bytes in 2168 real milliseconds = 0 KB/sec
ttcp-t: 10 I/O calls, msec/call = 216, calls/sec = 4, bytes/call = 1
```

**netstat-e**

``` syntax
Interface Statistics
                      Received     Sent
Bytes                 39229207     444685382
Unicast packets       487641       570100
Non-unicast packets   1159164      11301
Discards              0            0
Errors                0            0
Unknown protocols     52812
```

### <a name="calculations"></a>Calcoli

**Inviati:** 816 byte

**Ricevuti:** 674 byte

**Byte totali:** 1490

**Byte utente:** 10

**Overhead:** 1480/1490 = 99,3%

* * Goodput: * * = 5 byte al secondo (o 40 bit/sec)

> [!Note]  
> I byte effettivi trasferiti non corrispondono ai valori teorici a causa dei byte di riempimento non contabilizzati nei valori netstat.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Comportamento dell'applicazione](application-behavior-2.md)
</dt> <dt>

[Applicazioni Windows Sockets a prestazioni elevate](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



