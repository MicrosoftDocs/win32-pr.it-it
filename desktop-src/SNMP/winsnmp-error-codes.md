---
title: Codici di errore WinSNMP
description: Codici di errore WinSNMP
ms.assetid: 03b13b82-a31c-47e2-8b4d-17dcc4d19e56
keywords:
- WinSNMP codici di errore SNMP
- Codici di errore SNMP, WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d3cff7bd1e534f5f9c1fb0ae2ea2687d2ba99a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473966"
---
# <a name="winsnmp-error-codes"></a><span data-ttu-id="b5e0d-105">Codici di errore WinSNMP</span><span class="sxs-lookup"><span data-stu-id="b5e0d-105">WinSNMP Error Codes</span></span>

<span data-ttu-id="b5e0d-106">\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="b5e0d-106">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b5e0d-107">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="b5e0d-107">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b5e0d-108">Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="b5e0d-108">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

> [!Note]  
> <span data-ttu-id="b5e0d-109">Gli errori descritti in questo argomento sono distinti dai codici di errore SNMP definiti dalle RFC pertinenti.</span><span class="sxs-lookup"><span data-stu-id="b5e0d-109">The errors described in this topic are distinct from the SNMP error codes defined by the relevant RFCs.</span></span>

 

<span data-ttu-id="b5e0d-110">Tutte le funzioni WinSNMP restituiscono il valore **snmpapi \_ Failure** se la funzione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b5e0d-110">All WinSNMP functions return the value **SNMPAPI\_FAILURE** if the function fails.</span></span> <span data-ttu-id="b5e0d-111">L'applicazione WinSNMP deve chiamare immediatamente la funzione [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) per recuperare le informazioni estese sugli errori quando una funzione WinSNMP ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b5e0d-111">The WinSNMP application must immediately call the [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) function to retrieve extended error information when a WinSNMP function fails.</span></span> <span data-ttu-id="b5e0d-112">Nella tabella seguente sono elencati gli argomenti che illustrano i codici di errore estesi restituiti dalle funzioni WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="b5e0d-112">The following table lists topics that discuss extended error codes returned by WinSNMP functions.</span></span>



| <span data-ttu-id="b5e0d-113">Argomento</span><span class="sxs-lookup"><span data-stu-id="b5e0d-113">Topic</span></span>                                                        | <span data-ttu-id="b5e0d-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5e0d-114">Description</span></span>                                             |
|--------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="b5e0d-115">Codici di errore comuni di WinSNMP</span><span class="sxs-lookup"><span data-stu-id="b5e0d-115">WinSNMP Common Error Codes</span></span>](winsnmp-common-error-codes.md) | <span data-ttu-id="b5e0d-116">Vengono descritti i codici di errore comuni per l'API WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="b5e0d-116">Describes common error codes for the WinSNMP API.</span></span>       |
| [<span data-ttu-id="b5e0d-117">Errori di trasporto di rete</span><span class="sxs-lookup"><span data-stu-id="b5e0d-117">Network Transport Errors</span></span>](network-transport-errors.md)     | <span data-ttu-id="b5e0d-118">Descrive gli errori di trasporto di rete per l'API WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="b5e0d-118">Describes network transport errors for the WinSNMP API.</span></span> |



 

<span data-ttu-id="b5e0d-119">Gli errori WinSNMP che comportano informazioni specifiche del contesto sono inclusi nella pagina di riferimento per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="b5e0d-119">The WinSNMP errors that convey context-specific information are included in the function reference page.</span></span>

 

 