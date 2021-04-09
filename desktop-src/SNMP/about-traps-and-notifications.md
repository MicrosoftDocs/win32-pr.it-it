---
title: Informazioni su trap e notifiche
description: Un tipo di messaggio che un'applicazione dell'agente SNMP può inviare a un'applicazione WinSNMP è un messaggio asincrono che informa l'applicazione di un evento significativo.
ms.assetid: 5249c5a5-9260-4a67-b00f-a12214012bb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bacc6a92de2cb5a12aaf09f5caa629f28338f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856193"
---
# <a name="about-traps-and-notifications"></a>Informazioni su trap e notifiche

Un tipo di messaggio che un'applicazione dell'agente SNMP può inviare a un'applicazione WinSNMP è un messaggio asincrono che informa l'applicazione di un evento significativo. Un esempio di un evento significativo è quando un collegamento di rete viene arrestato o quando si verifica un errore di autenticazione.

Questi tipi di messaggi sono denominati trap in SNMPv1 e notifiche in SNMPv2C. L'implementazione di Microsoft WinSNMP converte sempre i trap SNMPv1 nel formato SNMPv2C, come definito da RFC 1908.

Quando si chiama la funzione [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) per creare una PDU trap, è possibile creare solo una PDU trap SNMPv2C. L'unico tipo di Trap PDU che è possibile aggiornare con una chiamata alla funzione [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) è una PDU trap SNMPv2C.

Per ulteriori informazioni, vedere gli argomenti seguenti.



| Argomento                                                                                    | Descrizione |
|------------------------------------------------------------------------------------------|-------------|
| [Conversione di trap da SNMPv1 a SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md) |             |
| [Formati trap](trap-formats.md)                                                         |             |



 

 

 




