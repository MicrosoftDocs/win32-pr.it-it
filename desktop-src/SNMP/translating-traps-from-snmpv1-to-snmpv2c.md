---
title: Conversione di trap da SNMPv1 a SNMPv2C
description: Quando l'implementazione Microsoft WinSNMP riceve trap da un'entità che opera nel framework SNMPv1, converte le trap nel formato SNMPv2C.
ms.assetid: 472f67ba-05d5-46f7-a2f1-1cef6182574e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f70ddbdfb779f6b06f8ed26490c6fabd2421ae96f0006b4af5b7f1ab18f7d5d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885861"
---
# <a name="translating-traps-from-snmpv1-to-snmpv2c"></a>Conversione di trap da SNMPv1 a SNMPv2C

Quando l'implementazione Microsoft WinSNMP riceve trap da un'entità che opera nel framework SNMPv1, converte le trap nel formato SNMPv2C. Pertanto, quando [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) recapita una trap, è sempre nel formato SNMPv2C. RFC 1908, "Coesistenza tra la versione 1 e la versione 2 di Internet-standard Network Management Framework", specifica le regole per la conversione da SNMPv1 al formato trap SNMPv2C.

Un'applicazione WinSNMP può controllare l'ultima voce di associazione di variabili in un elenco di associazioni di variabili per determinare se la voce è una trap convertita dal formato SNMPv1 al formato SNMPv2C. In questo caso, l'ultima associazione di variabili sarà sempre uguale al valore "snmpTrapEnterpriseOID.0".

Per altre informazioni, vedere [Gestione di trap e notifiche.](managing-traps-and-notifications.md)

 

 




