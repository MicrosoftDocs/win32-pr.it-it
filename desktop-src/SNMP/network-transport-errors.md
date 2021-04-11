---
title: Errori di trasporto di rete
description: L'implementazione di Microsoft WinSNMP è in grado di rilevare un errore di trasporto di rete dopo la trasmissione di un messaggio SNMP.
ms.assetid: 2ff535b1-76cb-42aa-baeb-14c1a1bc41ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cf6b7610fbfe8d19a375bd3e3146263b9e9f0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872834"
---
# <a name="network-transport-errors"></a>Errori di trasporto di rete

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

L'implementazione di Microsoft WinSNMP è in grado di rilevare un errore di trasporto di rete dopo la trasmissione di un messaggio SNMP. Quando si verifica questa situazione, l'implementazione invia una notifica di ricezione dati alla sessione WinSNMP che ha avviato la richiesta di comunicazione. L'implementazione restituisce anche un \_ errore snmpapi alla chiamata successiva alla funzione [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) per la sessione. La funzione **SnmpRecvMsg** ha esito negativo con un codice di errore esteso che indica un errore di livello del trasporto di rete.

Per un elenco di errori specifici del livello di trasporto, vedere le pagine di riferimento per le funzioni [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)e [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) .

 

 