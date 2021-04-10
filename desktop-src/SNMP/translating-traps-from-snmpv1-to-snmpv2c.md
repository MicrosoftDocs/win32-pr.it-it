---
title: Conversione di trap da SNMPv1 a SNMPv2C
description: Quando l'implementazione di Microsoft WinSNMP riceve trap da un'entità che opera nel Framework SNMPv1, converte i trap nel formato SNMPv2C.
ms.assetid: 472f67ba-05d5-46f7-a2f1-1cef6182574e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d36870bda9b434bcc19f42332f2751020689591
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855746"
---
# <a name="translating-traps-from-snmpv1-to-snmpv2c"></a>Conversione di trap da SNMPv1 a SNMPv2C

Quando l'implementazione di Microsoft WinSNMP riceve trap da un'entità che opera nel Framework SNMPv1, converte i trap nel formato SNMPv2C. Pertanto, quando [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) recapita un trap, è sempre nel formato SNMPv2C. RFC 1908, "coesistenza tra la versione 1 e la versione 2 del Framework di gestione della rete Internet standard", specifica le regole per la conversione dal SNMPv1 al formato trap SNMPv2C.

Un'applicazione WinSNMP può controllare l'ultima voce di associazione di variabili in un elenco di associazioni variabili per determinare se la voce è una trap tradotta da SNMPv1 nel formato SNMPv2C. In tal caso, l'ultima associazione di variabili sarà sempre uguale al valore "snmpTrapEnterpriseOID. 0".

Per altre informazioni, vedere [gestione di trap e notifiche](managing-traps-and-notifications.md).

 

 




