---
title: Informazioni sulla ritrasmissione
description: Un'applicazione WinSNMP può effettuare richieste di operazioni SNMP in vari modi.
ms.assetid: 71150a66-74a3-4957-bc70-3dd25c3b9c71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade0b2d58f371de87be5da855f26686a18518454c787c6a09e9701afbb731757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009959"
---
# <a name="about-retransmission"></a>Informazioni sulla ritrasmissione

Un'applicazione WinSNMP può effettuare richieste di operazioni SNMP in vari modi. L'applicazione può mettere diverse richieste a un agente SNMP, senza attendere una risposta, oppure può mettere una singola richiesta e attendere la risposta. Poiché SNMP può essere implementato su più protocolli di trasporto, i meccanismi di recapito e le caratteristiche di affidabilità possono variare.

Quando si codifica l'applicazione WinSNMP, è necessario determinare il livello di affidabilità necessario per le operazioni di comunicazione, in base al modo in cui l'applicazione genera richieste di operazioni. È quindi necessario selezionare una strategia di ritrasmissione e implementare un criterio di ritrasmissione.

I criteri di ritrasmissione includono un periodo di timeout e un numero di tentativi. Un periodo di timeout è il tempo trascorso, in centesimi di secondo, tra il rilascio di un'applicazione di una richiesta [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) e la ricezione del messaggio corrispondente. L'applicazione riceve il messaggio in seguito a una chiamata alla [**funzione SnmpRecvMsg.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) Il valore di timeout è il periodo di tempo in cui l'implementazione Microsoft WinSNMP attende che un'entità risponda a una richiesta di comunicazione. Se non è presente alcuna risposta entro il periodo di timeout, l'implementazione ritrasmette la richiesta se il valore del numero di tentativi specifica i tentativi di ritrasmissione oppure non riesce la chiamata a [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg). Un numero di tentativi è il numero massimo di tentativi di ritrasmissione emersi dall'implementazione in caso di errore di una richiesta di trasmissione SNMP.

L'implementazione archivia i valori di timeout e i conteggi dei tentativi nel relativo database per l'applicazione. L'implementazione archivia singoli valori per ogni entità di destinazione.

Le applicazioni devono stabilire le proprie frequenze di polling e devono gestire le variabili timer. Per altre informazioni, vedere [Gestione dei criteri di ritrasmissione](managing-the-retransmission-policy.md).

 

 




