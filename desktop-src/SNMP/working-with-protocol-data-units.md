---
title: Utilizzo delle unità dati del protocollo
description: Il Simple Network Management Protocol (SNMP) Invia le richieste e le risposte dell'operazione come messaggi SNMP.
ms.assetid: 0928981c-4d60-4583-9eef-8127e05b1ba8
keywords:
- Utilizzo di SNMP (Protocol Data Unit)
- Unità dati protocollo SNMP, utilizzo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e40f36fa28f7ff17974d79f4f8ac29b8b6130b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045033"
---
# <a name="working-with-protocol-data-units"></a>Utilizzo delle unità dati del protocollo

Il Simple Network Management Protocol (SNMP) Invia le richieste e le risposte dell'operazione come messaggi SNMP. Un messaggio SNMP è un'unità dati del protocollo SNMP, oltre a elementi di intestazione del messaggio aggiuntivi definiti dalla relativa RFC. Una PDU include un elenco di associazioni variabili.

La struttura di una PDU è limitata all'implementazione di Microsoft WinSNMP. Un'applicazione WinSNMP può accedere a una PDU con un handle del tipo **HSNMP \_ PDU**. L'applicazione WinSNMP deve creare una PDU prima di chiamare la funzione [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) o la funzione [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) .

L'applicazione può estrarre e aggiornare gli elementi dati di una PDU e rilasciare le risorse allocate per PDU. Per eseguire queste operazioni, l'applicazione usa le [funzioni PDU](winsnmp-functions.md)WinSNMP. La tabella seguente elenca gli argomenti che illustrano l'uso di PDU nell'ambiente di programmazione WinSNMP.



| Argomento                                                                        | Descrizione                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Creazione di una PDU](creating-a-pdu.md)                                         | Viene descritto come creare una PDU.                                     |
| [Aggiornamento di una PDU](updating-a-pdu.md)                                         | Viene descritto come recuperare e aggiornare i campi PDU.                   |
| [Duplicazione di una PDU](duplicating-a-pdu.md)                                   | Viene descritto come duplicare una PDU.                                  |
| [Convalida di una PDU](validating-a-pdu.md)                                     | Viene descritta la convalida di una PDU.                                 |
| [PDU di risposta e richiesta corrispondenti](matching-response-and-request-pdus.md) | Viene descritto il processo di corrispondenza di una PDU di risposta a un PDU della richiesta. |



 

Per ulteriori informazioni, vedere [utilizzo di elenchi di associazione variabili](working-with-variable-binding-lists.md) e di [oggetti handle di risorsa](resource-handle-objects.md).

 

 




