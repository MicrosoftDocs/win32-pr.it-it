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
# <a name="opening-and-closing-a-winsnmp-application"></a><span data-ttu-id="ab5c6-103">Apertura e chiusura di un'applicazione WinSNMP</span><span class="sxs-lookup"><span data-stu-id="ab5c6-103">Opening and Closing a WinSNMP Application</span></span>

<span data-ttu-id="ab5c6-104">È necessario che l'applicazione WinSNMP chiami la funzione [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) correttamente prima di chiamare qualsiasi altra funzione WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="ab5c6-104">The WinSNMP application must call the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function successfully before it calls any other WinSNMP function.</span></span> <span data-ttu-id="ab5c6-105">La funzione **SnmpStartup** consente all'implementazione di Microsoft WinSNMP di eseguire le procedure di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="ab5c6-105">The **SnmpStartup** function enables the Microsoft WinSNMP implementation to perform initialization procedures.</span></span> <span data-ttu-id="ab5c6-106">La funzione restituisce anche all'applicazione la versione dell'API WinSNMP supportata dall'implementazione, il livello di comunicazione SNMP supportato e le modalità di conversione e ritrasmissione predefinite dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="ab5c6-106">The function also returns to the application the version of the WinSNMP API that the implementation supports, the level of SNMP communications it supports, and the implementation's default translation and retransmission modes.</span></span>

<span data-ttu-id="ab5c6-107">L'applicazione WinSNMP deve chiamare la funzione [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) quando l'applicazione non richiede più i servizi dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="ab5c6-107">The WinSNMP application must call the [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) function when the application no longer requires the implementation's services.</span></span> <span data-ttu-id="ab5c6-108">Anche se **SnmpCleanup** consente all'implementazione di deallocare tutte le risorse allocate all'applicazione, è consigliabile che l'applicazione chiami prima la funzione [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) una volta per ogni sessione WinSNMP aperta, per ottimizzare le prestazioni dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="ab5c6-108">Even though **SnmpCleanup** enables the implementation to deallocate all resources allocated to the application, it is recommended that the application first call the [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) function once for each open WinSNMP session, to maximize the implementation's performance.</span></span> <span data-ttu-id="ab5c6-109">L'applicazione WinSNMP deve chiamare [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) come ultima funzione WinSNMP prima di terminare.</span><span class="sxs-lookup"><span data-stu-id="ab5c6-109">The WinSNMP application must call [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) as the last WinSNMP function before it terminates.</span></span>

 

 




