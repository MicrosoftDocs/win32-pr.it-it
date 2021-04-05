---
title: Novità in SNMP
description: SNMP supporta l'utilizzo di IPv6 a partire da Windows Vista.
ms.assetid: 38d71c0a-8de1-45a7-958c-aa44411451bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913f71cdf0b23800340f2c43f7b7fa22f45883a2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729783"
---
# <a name="new-in-snmp"></a><span data-ttu-id="a972c-103">Novità in SNMP</span><span class="sxs-lookup"><span data-stu-id="a972c-103">New in SNMP</span></span>

<span data-ttu-id="a972c-104">\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="a972c-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a972c-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="a972c-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a972c-106">Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="a972c-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="a972c-107">SNMP supporta l'utilizzo di IPv6 a partire da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a972c-107">SNMP supports the use of IPv6 starting with Windows Vista.</span></span> <span data-ttu-id="a972c-108">Tuttavia, SNMP supporta solo IPv6 per le reti che eseguono Windows Server 2008 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a972c-108">However, SNMP supports IPv6 only for networks running Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="a972c-109">Questo perché SNMP richiede che lo stack di protocolli aggiornato sia disponibile in questi sistemi operativi per il supporto IPv6.</span><span class="sxs-lookup"><span data-stu-id="a972c-109">This is because SNMP requires the updated protocol stack available in these operating systems for its IPv6 support.</span></span>

<span data-ttu-id="a972c-110">A meno che la rete non sia solo una rete Windows Server 2008, le comunicazioni IPv6 avranno esito negativo, anche se uno stack di protocolli IPv6 è installato separatamente nei computer che eseguono versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="a972c-110">Unless your network is solely a Windows Server 2008 network, IPv6 communications will fail, even if an IPv6 protocol stack is separately installed on those computers that run earlier versions of Windows.</span></span> <span data-ttu-id="a972c-111">Ad esempio, gli agenti SNMP eseguiti in Windows Server 2003 o Windows XP o Windows 2000 rispondono solo alle query eseguite sui rispettivi indirizzi IPv4.</span><span class="sxs-lookup"><span data-stu-id="a972c-111">For example, SNMP agents that run on Windows Server 2003, or Windows XP, or Windows 2000, respond only to queries that are made to their IPv4 addresses.</span></span>

 

 