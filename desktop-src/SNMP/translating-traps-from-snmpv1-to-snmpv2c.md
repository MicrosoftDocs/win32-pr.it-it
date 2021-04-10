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
# <a name="translating-traps-from-snmpv1-to-snmpv2c"></a><span data-ttu-id="cb6b4-103">Conversione di trap da SNMPv1 a SNMPv2C</span><span class="sxs-lookup"><span data-stu-id="cb6b4-103">Translating Traps from SNMPv1 to SNMPv2C</span></span>

<span data-ttu-id="cb6b4-104">Quando l'implementazione di Microsoft WinSNMP riceve trap da un'entità che opera nel Framework SNMPv1, converte i trap nel formato SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="cb6b4-104">When the Microsoft WinSNMP implementation receives traps from an entity operating under the SNMPv1 framework, it translates the traps to the SNMPv2C format.</span></span> <span data-ttu-id="cb6b4-105">Pertanto, quando [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) recapita un trap, è sempre nel formato SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="cb6b4-105">Therefore, when [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) delivers a trap it is always in the SNMPv2C format.</span></span> <span data-ttu-id="cb6b4-106">RFC 1908, "coesistenza tra la versione 1 e la versione 2 del Framework di gestione della rete Internet standard", specifica le regole per la conversione dal SNMPv1 al formato trap SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="cb6b4-106">RFC 1908, "Coexistence between Version 1 and Version 2 of the Internet-standard Network Management Framework," specifies the rules for translating from the SNMPv1 to the SNMPv2C trap format.</span></span>

<span data-ttu-id="cb6b4-107">Un'applicazione WinSNMP può controllare l'ultima voce di associazione di variabili in un elenco di associazioni variabili per determinare se la voce è una trap tradotta da SNMPv1 nel formato SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="cb6b4-107">A WinSNMP application can check the last variable binding entry in a variable binding list to determine if the entry is a trap translated from the SNMPv1 to the SNMPv2C format.</span></span> <span data-ttu-id="cb6b4-108">In tal caso, l'ultima associazione di variabili sarà sempre uguale al valore "snmpTrapEnterpriseOID. 0".</span><span class="sxs-lookup"><span data-stu-id="cb6b4-108">If so, the last variable binding will always be equal to the value "snmpTrapEnterpriseOID.0".</span></span>

<span data-ttu-id="cb6b4-109">Per altre informazioni, vedere [gestione di trap e notifiche](managing-traps-and-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="cb6b4-109">For more information, see [Managing Traps and Notifications](managing-traps-and-notifications.md).</span></span>

 

 




