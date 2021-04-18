---
description: Microsoft Network Monitor 3 (Netmon) è un analizzatore di pacchetti usato per controllare il traffico di rete.
ms.assetid: 015a6a6d-9e07-4f22-b931-dcce77051bef
title: Download dei filtri Netmon e DPWS di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47790b26164ec0ed2792d1d1e1f2ad4ba5d77d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310312"
---
# <a name="downloading-netmon-and-sample-dpws-filters"></a>Download dei filtri Netmon e DPWS di esempio

Microsoft Network Monitor 3 (Netmon) è un analizzatore di pacchetti usato per controllare il traffico di rete. È necessario scaricare Netmon prima di eseguire le procedure di risoluzione dei problemi fornite nel [controllo delle tracce di rete per UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) ed [esaminare le tracce di rete per lo scambio di metadati http](inspecting-network-traces-for-http-metadata-exchange.md) . Dopo aver scaricato Netmon, è possibile usare i filtri DPWS per isolare il traffico di interesse.

## <a name="downloading-netmon"></a>Download di Netmon

Per scaricare Netmon, passare a [Microsoft Network Monitor](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) e seguire le istruzioni. Per ulteriori informazioni su Netmon, vedere "informazioni su Network Monitor 3,0" nella Knowledge base relativa alla guida e al supporto tecnico all'indirizzo [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .

## <a name="sample-dpws-filters"></a>Filtri DPWS di esempio

In alcuni casi, la risoluzione dei problemi relativi a WS-Discovery e scambio di metadati deve essere eseguita in una rete occupata. I filtri di esempio possono essere usati per limitare l'output di Netmon al traffico di interesse. Per ulteriori informazioni sull'utilizzo dei filtri Netmon, vedere [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .

Nell'esempio seguente viene illustrato un filtro che limita l'output a tutto il traffico di trasmissione WS-Discovery.

> [!Note]  
> Questo filtro non acquisisce il traffico da stack che non rispondono a multicast WS-Discovery messaggi originati dalla porta 3702. Se viene utilizzato uno stack di questo tipo, è necessario modificare questo filtro di esempio prima dell'utilizzo.

 

``` syntax
// All broadcast WS-Discovery traffic
UDP.Port == 3702
```

Nell'esempio seguente viene illustrato un filtro che limita l'output ai messaggi HTTP inviati agli stack WSDAPI sulla porta predefinita.

> [!Note]  
> I servizi possono inviare messaggi HTTP rilevanti da porte diverse da 5357. Se il traffico da altre porte è di interesse, questo filtro di esempio deve essere modificato prima dell'utilizzo.

 

``` syntax
// HTTP messages sent to WSDAPI stacks on default port
TCP.Port == 5357
```

Nell'esempio seguente viene illustrato un filtro che limita l'output al traffico multicast IPv4.

``` syntax
// All IPv4 multicast traffic
IPv4.DestinationAddress == 239.255.255.250
```

Nell'esempio seguente viene illustrato un filtro che limita l'output al traffico multicast IPv6.

``` syntax
// All IPv6 multicast traffic
IPv6.DestinationAddress == FF02::C
```

È possibile combinare alcuni filtri per limitare ulteriormente i risultati. Nell'esempio seguente viene illustrato un filtro che limita l'output al traffico multicast IPv4 WS-Discovery.

``` syntax
// All IPv4 multicast WS-Discovery traffic
UDP.Port==3702 && IPv4.DestinationAddress=239.255.255.250
```

Quando si utilizzano questi filtri, il traffico pertinente può essere escluso dai risultati di Netmon. L'esclusione può verificarsi quando i servizi si trovano in porte diverse dalle porte predefinite (5357/5358) e quando uno stack DPWS non risponde ai messaggi utilizzando la porta predefinita. In questi casi, è necessario modificare i filtri prima dell'utilizzo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure di diagnostica WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Introduzione con la risoluzione dei problemi di WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



