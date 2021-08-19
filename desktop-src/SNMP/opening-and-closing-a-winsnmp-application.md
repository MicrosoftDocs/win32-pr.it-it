---
title: Apertura e chiusura di un'applicazione WinSNMP
description: L'applicazione WinSNMP deve chiamare correttamente la funzione SnmpStartup prima di chiamare qualsiasi altra funzione WinSNMP.
ms.assetid: ff2b99c9-c2fd-4bb7-8fd5-799e72c4560d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4aa18f437f8b1a430ad27b40b838859d2e00641bcb4532602715548b370acce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009249"
---
# <a name="opening-and-closing-a-winsnmp-application"></a>Apertura e chiusura di un'applicazione WinSNMP

L'applicazione WinSNMP deve chiamare correttamente la [**funzione SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) prima di chiamare qualsiasi altra funzione WinSNMP. La **funzione SnmpStartup** consente all'implementazione Microsoft WinSNMP di eseguire procedure di inizializzazione. La funzione restituisce anche all'applicazione la versione dell'API WinSNMP supportata dall'implementazione, il livello di comunicazioni SNMP supportate e le modalità di conversione e ritrasmissione predefinite dell'implementazione.

L'applicazione WinSNMP deve chiamare la [**funzione SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) quando l'applicazione non richiede più i servizi dell'implementazione. Anche se **SnmpCleanup** consente all'implementazione di deallocare tutte le risorse allocate all'applicazione, è consigliabile che l'applicazione chiami prima la funzione [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) una volta per ogni sessione WinSNMP aperta, per ottimizzare le prestazioni dell'implementazione. L'applicazione WinSNMP deve chiamare [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) come ultima funzione WinSNMP prima che termini.

 

 




