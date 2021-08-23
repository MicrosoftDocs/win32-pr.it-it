---
title: Informazioni su trap e notifiche
description: Un tipo di messaggio che un'applicazione agente SNMP può inviare a un'applicazione WinSNMP è un messaggio asincrono che informa l'applicazione di un evento significativo.
ms.assetid: 5249c5a5-9260-4a67-b00f-a12214012bb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60739041237dad462e516e43c71d552446357f3ddc188d6609de2eef508b9658
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009809"
---
# <a name="about-traps-and-notifications"></a>Informazioni su trap e notifiche

Un tipo di messaggio che un'applicazione agente SNMP può inviare a un'applicazione WinSNMP è un messaggio asincrono che informa l'applicazione di un evento significativo. Un esempio di evento significativo è quando un collegamento di rete si arresta o quando si verifica un errore di autenticazione.

Questi tipi di messaggi sono denominati trap in SNMPv1 e notifiche in SNMPv2C. L'implementazione Di Microsoft WinSNMP converte sempre le trap SNMPv1 nel formato SNMPv2C, come definito da RFC 1908.

Quando si chiama la [**funzione SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) per creare una PDU trap, è possibile creare solo una PDU trap SNMPv2C. L'unico tipo di PDU trap che è possibile aggiornare con una chiamata alla [**funzione SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) è una PDU trap SNMPv2C.

Per ulteriori informazioni, vedere gli argomenti seguenti.



| Argomento                                                                                    | Descrizione |
|------------------------------------------------------------------------------------------|-------------|
| [Conversione di trap da SNMPv1 a SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md) |             |
| [Formati trap](trap-formats.md)                                                         |             |



 

 

 




