---
title: Creazione di una PDU
description: Per creare e inizializzare una PDU, un'applicazione WinSNMP chiama la funzione SnmpCreatePdu.
ms.assetid: 7f02a2c6-19bc-456f-bf04-3297d19000f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aba7a4ca42e2a5d63169d2521410773ca018c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856186"
---
# <a name="creating-a-pdu"></a><span data-ttu-id="e5ebf-103">Creazione di una PDU</span><span class="sxs-lookup"><span data-stu-id="e5ebf-103">Creating a PDU</span></span>

<span data-ttu-id="e5ebf-104">Per creare e inizializzare una PDU, un'applicazione WinSNMP chiama la funzione [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) .</span><span class="sxs-lookup"><span data-stu-id="e5ebf-104">To create and initialize a PDU a WinSNMP application calls the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function.</span></span> <span data-ttu-id="e5ebf-105">L'applicazione deve chiamare **SnmpCreatePdu** prima di chiamare la funzione [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) per richiedere che l'implementazione di Microsoft WinSNMP trasmetta una PDU.</span><span class="sxs-lookup"><span data-stu-id="e5ebf-105">The application must call **SnmpCreatePdu** before it calls the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function to request that the Microsoft WinSNMP implementation transmit a PDU.</span></span> <span data-ttu-id="e5ebf-106">L'applicazione deve inoltre chiamare [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) prima di chiamare la funzione [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) per richiedere la codifica di un messaggio SNMP.</span><span class="sxs-lookup"><span data-stu-id="e5ebf-106">The application must also call [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) before it calls the [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) function to request encoding of an SNMP message.</span></span>

<span data-ttu-id="e5ebf-107">L'applicazione deve chiamare la funzione [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) per rilasciare le risorse allocate dalla funzione [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) per la nuova PDU.</span><span class="sxs-lookup"><span data-stu-id="e5ebf-107">The application must call the [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) function to release the resources that the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function allocates for new PDUs.</span></span>

 

 




