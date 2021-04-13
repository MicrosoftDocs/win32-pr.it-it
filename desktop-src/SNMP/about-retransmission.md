---
title: Informazioni sulla ritrasmissione
description: Un'applicazione WinSNMP può eseguire richieste di operazioni SNMP in diversi modi.
ms.assetid: 71150a66-74a3-4957-bc70-3dd25c3b9c71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a26ba632cec096300927911c2277cbcf5911e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329116"
---
# <a name="about-retransmission"></a>Informazioni sulla ritrasmissione

Un'applicazione WinSNMP può eseguire richieste di operazioni SNMP in diversi modi. L'applicazione può inviare diverse richieste a un agente SNMP, senza attendere una risposta, oppure può emettere una singola richiesta e attendere la risposta. Poiché SNMP può essere implementato su più protocolli di trasporto, i meccanismi di recapito e le caratteristiche di affidabilità possono variare.

Quando si codifica l'applicazione WinSNMP, è necessario determinare il livello di affidabilità necessario per le operazioni di comunicazione, in base al modo in cui l'applicazione rilascia le richieste di operazione. Quindi, è necessario selezionare una strategia di ritrasmissione e implementare un criterio di ritrasmissione.

Un criterio di ritrasmissione include un periodo di timeout e un numero di tentativi. Un periodo di timeout è il tempo trascorso, in centesimi di secondo, tra il rilascio di un'applicazione di una richiesta [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) e la relativa ricezione del messaggio corrispondente. L'applicazione riceve il messaggio come risultato di una chiamata alla funzione [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) . Il valore di timeout corrisponde al periodo di tempo durante il quale l'implementazione di Microsoft WinSNMP attende che un'entità risponda a una richiesta di comunicazione. Se non è presente alcuna risposta entro il periodo di timeout, l'implementazione ritrasmette la richiesta se il valore del numero di tentativi specifica i tentativi di ritrasmissione o se la chiamata a [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)non riesce. Un numero di tentativi è il numero massimo di tentativi di ritrasmissione che l'implementazione esegue se una richiesta di trasmissione SNMP ha esito negativo.

L'implementazione archivia i valori di timeout e i conteggi dei tentativi nel database per l'applicazione. L'implementazione archivia singoli valori per ogni entità di destinazione.

Le applicazioni devono stabilire le proprie frequenze di polling e devono gestire le variabili del timer. Per ulteriori informazioni, vedere [gestione dei criteri di ritrasmissione](managing-the-retransmission-policy.md).

 

 




