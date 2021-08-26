---
description: Microsoft Network Monitor 3 (Netmon) è un analizzatore di pacchetti usato per controllare il traffico di rete.
ms.assetid: 015a6a6d-9e07-4f22-b931-dcce77051bef
title: Download di netmon e filtri DPWS di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a6f92f2680807101a3c82664f4b0b3ae5a877f0d9f5797da9c9c0b6ea2b158
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030221"
---
# <a name="downloading-netmon-and-sample-dpws-filters"></a>Download di netmon e filtri DPWS di esempio

Microsoft Network Monitor 3 (Netmon) è un analizzatore di pacchetti usato per controllare il traffico di rete. È necessario scaricare Netmon prima che sia possibile seguire la procedura di risoluzione dei problemi descritta in Inspecting Network Traces for UDP WS-Discovery and Inspecting Network Traces for HTTP Metadata Exchange.Netmon must be downloaded before the troubleshooting steps given in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) and [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md) can be followed. Dopo aver scaricato Netmon, è possibile usare i filtri DPWS per isolare il traffico di interesse.

## <a name="downloading-netmon"></a>Download di Netmon

Per scaricare Netmon, passare a [Microsoft Network Monitor](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) e seguire le istruzioni. Per altre informazioni su Netmon, vedere "Information about Network Monitor 3.0" (Informazioni su Network Monitor 3.0) nella Guida e supporto Knowledge Base all'indirizzo [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .

## <a name="sample-dpws-filters"></a>Filtri DPWS di esempio

A volte, WS-Discovery risoluzione dei problemi di scambio dei metadati e dei metadati devono essere esempe in una rete occupata. I filtri di esempio possono essere usati per limitare l'output di Netmon al traffico di interesse. Per altre informazioni sull'uso dei filtri Netmon, vedere [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .

Nell'esempio seguente viene illustrato un filtro che limita l'output a tutto il traffico WS-Discovery broadcast.

> [!Note]  
> Questo filtro non acquisisce il traffico dagli stack che non rispondono ai messaggi WS-Discovery multicast che hanno origine sulla porta 3702. Se viene usato uno stack di questo tipo, questo filtro di esempio deve essere modificato prima dell'uso.

 

``` syntax
// All broadcast WS-Discovery traffic
UDP.Port == 3702
```

Nell'esempio seguente viene illustrato un filtro che limita l'output ai messaggi HTTP inviati agli stack WSDAPI sulla porta predefinita.

> [!Note]  
> I servizi possono inviare messaggi HTTP pertinenti da porte diverse da 5357. Se il traffico proveniente da altre porte è di interesse, questo filtro di esempio deve essere modificato prima dell'uso.

 

``` syntax
// HTTP messages sent to WSDAPI stacks on default port
TCP.Port == 5357
```

L'esempio seguente illustra un filtro che limita l'output al traffico multicast IPv4.

``` syntax
// All IPv4 multicast traffic
IPv4.DestinationAddress == 239.255.255.250
```

L'esempio seguente illustra un filtro che limita l'output al traffico multicast IPv6.

``` syntax
// All IPv6 multicast traffic
IPv6.DestinationAddress == FF02::C
```

Alcuni filtri possono essere combinati per limitare ulteriormente i risultati. L'esempio seguente illustra un filtro che limita l'output al traffico multicast IPv4 WS-Discovery traffico.

``` syntax
// All IPv4 multicast WS-Discovery traffic
UDP.Port==3702 && IPv4.DestinationAddress=239.255.255.250
```

Quando vengono usati questi filtri, il traffico pertinente può essere escluso dai risultati di Netmon. L'esclusione può verificarsi quando i servizi risiedono in porte diverse da quelle predefinite (5357/5358) e quando uno stack DPWS non risponde ai messaggi usando la porta predefinita. In questi casi, i filtri devono essere modificati prima dell'uso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure di diagnostica WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Attività iniziali risoluzione dei problemi di WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



