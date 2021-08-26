---
title: Formati trap
description: Il formato delle PDU trap è diverso da quello degli altri PDU. Anche il formato delle trap SNMPv1 e delle trap SNMPv2C è diverso.
ms.assetid: 2d2b4520-28b7-4a2e-8dee-456e17d9d6f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b73e9cd2a5396bbe258fcb67c88cc207ea0243a9e8aff9f31e4866b9ee8adcc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885681"
---
# <a name="trap-formats"></a>Formati trap

Il formato delle PDU trap è diverso da quello degli altri PDU. Anche il formato delle trap SNMPv1 e delle trap SNMPv2C è diverso.

Nel framework SNMPv2C, il formato trap PDU è un elenco di associazione di variabili *di n* voci di associazione di variabili organizzate nel modo seguente:

-   La prima voce di associazione di variabili contiene un timestamp.
-   La seconda voce di associazione di variabili è un identificatore di oggetto che identifica il trap.
-   Le voci di associazione da terza a *n* variabili, se presenti, contengono informazioni aggiuntive associate al trap.

Nel framework SNMPv1 il formato trap PDU è il seguente.

| Campo                      | Descrizione                                                      |
|----------------------------|------------------------------------------------------------------|
| Connettori                 | Identifica il tipo di dispositivo che ha generato la trap.           |
| agent-addr                 | Identifica l'indirizzo IP del dispositivo che ha generato il trap. |
| generic-trap/specific-trap | Identifica un tipo di trap predefinito.                               |
| timestamp                 | Identifica quando è stata generata la trap.                          |
| associazioni di variabili          | Contiene informazioni aggiuntive associate alla trap.        |



 

La [**funzione SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) restituisce sempre un messaggio nel formato SNMPv2C. Se il messaggio contiene il tipo di **operazione SNMP \_ PDU \_ TRAP,** l'applicazione può leggere le voci di associazione delle variabili del messaggio e recuperare le informazioni associate al trap.

 

 




