---
title: Informazioni su SNMP
description: SNMP usa un'architettura distribuita costituita da Manager e agenti.
ms.assetid: 55be55a8-1968-4373-a969-f7e03b75a824
keywords:
- SNMP, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1dab65173c96dce4bbd2f30edbca2a91f6153d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047188"
---
# <a name="about-snmp"></a><span data-ttu-id="61451-104">Informazioni su SNMP</span><span class="sxs-lookup"><span data-stu-id="61451-104">About SNMP</span></span>

<span data-ttu-id="61451-105">\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="61451-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="61451-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="61451-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="61451-107">Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="61451-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="61451-108">SNMP usa un'architettura distribuita costituita da Manager e agenti.</span><span class="sxs-lookup"><span data-stu-id="61451-108">SNMP uses a distributed architecture consisting of managers and agents.</span></span> <span data-ttu-id="61451-109">Un agente è un'applicazione SNMP che risponde alle query dalle applicazioni di gestione SNMP.</span><span class="sxs-lookup"><span data-stu-id="61451-109">An agent is an SNMP application that responds to queries from SNMP manager applications.</span></span> <span data-ttu-id="61451-110">L'agente SNMP è responsabile del recupero e dell'aggiornamento delle informazioni di gestione locali in base alle richieste di gestione SNMP.</span><span class="sxs-lookup"><span data-stu-id="61451-110">The SNMP agent is responsible for retrieving and updating local management information based on the requests of the SNMP manager.</span></span> <span data-ttu-id="61451-111">L'agente invia inoltre una notifica ai responsabili registrati quando si verificano eventi o trap significativi.</span><span class="sxs-lookup"><span data-stu-id="61451-111">The agent also notifies registered managers when significant events or traps occur.</span></span> <span data-ttu-id="61451-112">Un Manager è un'applicazione SNMP che genera query per le applicazioni dell'agente SNMP e riceve trap dalle applicazioni dell'agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="61451-112">A manager is an SNMP application that generates queries to SNMP agent applications and receives traps from SNMP agent applications.</span></span>

<span data-ttu-id="61451-113">Nei computer che eseguono Microsoft Windows XP/Windows 2000/Windows NT, l'agente SNMP viene implementato dal servizio SNMP (SNMP.EXE).</span><span class="sxs-lookup"><span data-stu-id="61451-113">On computers running Microsoft Windows XP/Windows 2000/Windows NT, the SNMP agent is implemented by the SNMP service (SNMP.EXE).</span></span> <span data-ttu-id="61451-114">SNMP Manager è in genere un'applicazione console di gestione SNMP di terze parti.</span><span class="sxs-lookup"><span data-stu-id="61451-114">The SNMP manager is typically a third-party SNMP management console application.</span></span> <span data-ttu-id="61451-115">Non è necessario che l'applicazione console di gestione venga eseguita nello stesso host dell'agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="61451-115">The management console application does not need to run on the same host as the SNMP agent.</span></span> <span data-ttu-id="61451-116">Per utilizzare le informazioni fornite dal servizio SNMP Microsoft, è necessaria almeno un'applicazione console di gestione SNMP.</span><span class="sxs-lookup"><span data-stu-id="61451-116">To use the information the Microsoft SNMP service provides, you need at least one SNMP management console application.</span></span> <span data-ttu-id="61451-117">Il sistema include librerie che supportano le applicazioni console di gestione SNMP, ma in questo momento non include un'applicazione console di gestione SNMP.</span><span class="sxs-lookup"><span data-stu-id="61451-117">The system includes libraries that support SNMP management console applications, but it does not include an SNMP management console application at this time.</span></span>

 

 