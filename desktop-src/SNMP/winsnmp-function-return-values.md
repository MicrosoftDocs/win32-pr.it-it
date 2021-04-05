---
title: Valori restituiti dalla funzione WinSNMP
description: Il valore restituito da una chiamata di funzione WinSNMP può essere un handle per una risorsa allocata dall'implementazione di Microsoft WinSNMP per l'applicazione WinSNMP.
ms.assetid: f0723cc7-fa3b-4a72-93a0-49d40a1fedd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a8e42e7d27b1079398efb2970b385bfc4e732c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047238"
---
# <a name="winsnmp-function-return-values"></a><span data-ttu-id="8f41e-103">Valori restituiti dalla funzione WinSNMP</span><span class="sxs-lookup"><span data-stu-id="8f41e-103">WinSNMP Function Return Values</span></span>

<span data-ttu-id="8f41e-104">\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="8f41e-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8f41e-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="8f41e-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="8f41e-106">Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="8f41e-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="8f41e-107">Il valore restituito da una chiamata di funzione WinSNMP può essere un handle per una risorsa allocata dall'implementazione di Microsoft WinSNMP per l'applicazione WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="8f41e-107">The return value from a WinSNMP function call can be a handle to a resource that the Microsoft WinSNMP implementation allocates for the WinSNMP application.</span></span>

<span data-ttu-id="8f41e-108">Nella tabella seguente sono elencati i cinque tipi di handle di risorsa allocati dall'implementazione.</span><span class="sxs-lookup"><span data-stu-id="8f41e-108">The following table lists the five types of resource handles that the implementation allocates.</span></span>



| <span data-ttu-id="8f41e-109">Tipo di handle</span><span class="sxs-lookup"><span data-stu-id="8f41e-109">Handle type</span></span>    | <span data-ttu-id="8f41e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f41e-110">Description</span></span>                       |
|----------------|-----------------------------------|
| <span data-ttu-id="8f41e-111">\_sessione HSNMP</span><span class="sxs-lookup"><span data-stu-id="8f41e-111">HSNMP\_SESSION</span></span> | <span data-ttu-id="8f41e-112">Handle per una sessione WinSNMP</span><span class="sxs-lookup"><span data-stu-id="8f41e-112">Handle to a WinSNMP session</span></span>       |
| <span data-ttu-id="8f41e-113">\_entità HSNMP</span><span class="sxs-lookup"><span data-stu-id="8f41e-113">HSNMP\_ENTITY</span></span>  | <span data-ttu-id="8f41e-114">Handle per un'entità SNMP</span><span class="sxs-lookup"><span data-stu-id="8f41e-114">Handle to an SNMP entity</span></span>          |
| <span data-ttu-id="8f41e-115">\_contesto HSNMP</span><span class="sxs-lookup"><span data-stu-id="8f41e-115">HSNMP\_CONTEXT</span></span> | <span data-ttu-id="8f41e-116">Handle per un contesto SNMP</span><span class="sxs-lookup"><span data-stu-id="8f41e-116">Handle to an SNMP context</span></span>         |
| <span data-ttu-id="8f41e-117">\_PDU HSNMP</span><span class="sxs-lookup"><span data-stu-id="8f41e-117">HSNMP\_PDU</span></span>     | <span data-ttu-id="8f41e-118">Handle per un'unità dati del protocollo</span><span class="sxs-lookup"><span data-stu-id="8f41e-118">Handle to a protocol data unit</span></span>    |
| <span data-ttu-id="8f41e-119">\_VBL HSNMP</span><span class="sxs-lookup"><span data-stu-id="8f41e-119">HSNMP\_VBL</span></span>     | <span data-ttu-id="8f41e-120">Handle per un elenco di associazioni variabili</span><span class="sxs-lookup"><span data-stu-id="8f41e-120">Handle to a variable binding list</span></span> |



 

<span data-ttu-id="8f41e-121">Per altre informazioni, vedere [oggetti handle di risorsa](resource-handle-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8f41e-121">For more information, see [Resource Handle Objects](resource-handle-objects.md).</span></span>

<span data-ttu-id="8f41e-122">Il valore restituito può essere anche un valore long integer senza segno del tipo **smiUINT32** che rappresenta un \_ valore di stato snmpapi.</span><span class="sxs-lookup"><span data-stu-id="8f41e-122">The return value can also be an unsigned long integer value of the **smiUINT32** type that represents an SNMPAPI\_STATUS value.</span></span>

<span data-ttu-id="8f41e-123">Nella tabella seguente sono elencati i valori di stato di WinSNMP e il relativo significato.</span><span class="sxs-lookup"><span data-stu-id="8f41e-123">The following table lists the WinSNMP status values and their meaning.</span></span>



| <span data-ttu-id="8f41e-124">Stato</span><span class="sxs-lookup"><span data-stu-id="8f41e-124">Status</span></span>           | <span data-ttu-id="8f41e-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f41e-125">Description</span></span>                                                                      |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8f41e-126">\_errore snmpapi</span><span class="sxs-lookup"><span data-stu-id="8f41e-126">SNMPAPI\_FAILURE</span></span> | <span data-ttu-id="8f41e-127">Indica un errore.</span><span class="sxs-lookup"><span data-stu-id="8f41e-127">Indicates an error.</span></span> <span data-ttu-id="8f41e-128">Equivale a 0 o **null**.</span><span class="sxs-lookup"><span data-stu-id="8f41e-128">Equates to 0 or **NULL**.</span></span>                                    |
| <span data-ttu-id="8f41e-129">SNMPAPI \_ riuscito</span><span class="sxs-lookup"><span data-stu-id="8f41e-129">SNMPAPI\_SUCCESS</span></span> | <span data-ttu-id="8f41e-130">Indica che la funzione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="8f41e-130">Indicates the function completed successfully.</span></span> <span data-ttu-id="8f41e-131">Equivale a 1 o a un conteggio positivo.</span><span class="sxs-lookup"><span data-stu-id="8f41e-131">Equates to 1 or a positive count.</span></span> |



 

 

 