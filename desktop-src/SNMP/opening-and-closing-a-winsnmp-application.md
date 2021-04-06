---
title: Apertura e chiusura di un'applicazione WinSNMP
description: È necessario che l'applicazione WinSNMP chiami la funzione SnmpStartup correttamente prima di chiamare qualsiasi altra funzione WinSNMP.
ms.assetid: ff2b99c9-c2fd-4bb7-8fd5-799e72c4560d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f960a22a6155d3f3eeec770af361fac2c0eb036e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045040"
---
# <a name="opening-and-closing-a-winsnmp-application"></a>Apertura e chiusura di un'applicazione WinSNMP

È necessario che l'applicazione WinSNMP chiami la funzione [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) correttamente prima di chiamare qualsiasi altra funzione WinSNMP. La funzione **SnmpStartup** consente all'implementazione di Microsoft WinSNMP di eseguire le procedure di inizializzazione. La funzione restituisce anche all'applicazione la versione dell'API WinSNMP supportata dall'implementazione, il livello di comunicazione SNMP supportato e le modalità di conversione e ritrasmissione predefinite dell'implementazione.

L'applicazione WinSNMP deve chiamare la funzione [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) quando l'applicazione non richiede più i servizi dell'implementazione. Anche se **SnmpCleanup** consente all'implementazione di deallocare tutte le risorse allocate all'applicazione, è consigliabile che l'applicazione chiami prima la funzione [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) una volta per ogni sessione WinSNMP aperta, per ottimizzare le prestazioni dell'implementazione. L'applicazione WinSNMP deve chiamare [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) come ultima funzione WinSNMP prima di terminare.

 

 




