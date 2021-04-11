---
title: Formati trap
description: Il formato di Trap PDU è diverso da quello di altre PDU. Anche il formato di trap SNMPv1 e trap SNMPv2C è diverso.
ms.assetid: 2d2b4520-28b7-4a2e-8dee-456e17d9d6f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87adc3222808fcc7e81904ade07c09afa13bc6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044369"
---
# <a name="trap-formats"></a>Formati trap

Il formato di Trap PDU è diverso da quello di altre PDU. Anche il formato di trap SNMPv1 e trap SNMPv2C è diverso.

In SNMPv2C Framework il formato di Trap PDU è un elenco di associazioni variabili di *n* voci di binding variabili organizzate nel modo seguente:

-   La prima voce di associazione variabile contiene un timestamp.
-   La seconda voce di associazione variabile è un identificatore di oggetto che identifica la trap.
-   Le terze e *n* voci di associazione variabili, se presenti, contengono informazioni aggiuntive associate al trap.

In SNMPv1 Framework il formato di Trap PDU è il seguente.

| Campo                      | Descrizione                                                      |
|----------------------------|------------------------------------------------------------------|
| Connettori                 | Identifica il tipo di dispositivo che ha generato la trap.           |
| Agent-addr                 | Identifica l'indirizzo IP del dispositivo che ha generato la trap. |
| Trap/Trap generico | Identifica un tipo trap predefinito.                               |
| timestamp                 | Identifica il momento in cui è stata generata la trap.                          |
| associazioni di variabili          | Contiene informazioni aggiuntive associate al trap.        |



 

La funzione [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) restituisce sempre un messaggio nel formato SNMPv2C. Se il messaggio contiene il tipo di **operazione \_ \_ trap SNMP PDU**, l'applicazione può leggere le voci di associazione variabili del messaggio e recuperare le informazioni associate alla trap.

 

 




