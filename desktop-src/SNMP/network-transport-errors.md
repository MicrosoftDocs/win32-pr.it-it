---
title: Errori di trasporto di rete
description: L'implementazione Microsoft WinSNMP può rilevare un errore di trasporto di rete dopo la trasmissione di un messaggio SNMP.
ms.assetid: 2ff535b1-76cb-42aa-baeb-14c1a1bc41ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15284bba97f2dda8d2fb4224dc2c94bd14050afb9463c73b4d297c1647ec273f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009309"
---
# <a name="network-transport-errors"></a>Errori di trasporto di rete

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece Windows [gestione remota](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

L'implementazione Microsoft WinSNMP può rilevare un errore di trasporto di rete dopo la trasmissione di un messaggio SNMP. In questo caso, l'implementazione invia una notifica di ricezione dei dati alla sessione WinSNMP che ha avviato la richiesta di comunicazione. L'implementazione restituisce anche SNMPAPI FAILURE alla chiamata \_ successiva alla [**funzione SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) per la sessione. La **funzione SnmpRecvMsg** ha esito negativo con un codice di errore esteso che indica un errore del livello di trasporto di rete.

Per un elenco di errori specifici del livello di trasporto, vedere le pagine di riferimento per le funzioni [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)e [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) .

 

 