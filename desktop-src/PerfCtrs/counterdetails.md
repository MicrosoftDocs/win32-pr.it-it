---
description: La tabella CounterDetails descrive un contatore specifico in un determinato computer.
ms.assetid: e2a16a6e-8cd4-4fd3-adeb-461faed948e4
title: CounterDetails
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 751073cdc2f2646ad1f2351bff0bdc02c498d428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967522"
---
# <a name="counterdetails"></a><span data-ttu-id="e1e7b-103">CounterDetails</span><span class="sxs-lookup"><span data-stu-id="e1e7b-103">CounterDetails</span></span>

<span data-ttu-id="e1e7b-104">La tabella **CounterDetails** descrive un contatore specifico in un determinato computer.</span><span class="sxs-lookup"><span data-stu-id="e1e7b-104">The **CounterDetails** table describes a specific counter on a particular computer.</span></span>

<span data-ttu-id="e1e7b-105">La tabella **CounterDetails** definisce i campi seguenti:</span><span class="sxs-lookup"><span data-stu-id="e1e7b-105">The **CounterDetails** table defines the following fields:</span></span>

-   <span data-ttu-id="e1e7b-106">**CounterID:** Identificatore univoco nel database di cui viene eseguito il mapping a una stringa di testo specifica del nome del contatore.</span><span class="sxs-lookup"><span data-stu-id="e1e7b-106">**CounterID:** A unique identifier in the database that maps to a specific counter name text string.</span></span> <span data-ttu-id="e1e7b-107">Questo campo è la chiave primaria della tabella.</span><span class="sxs-lookup"><span data-stu-id="e1e7b-107">This field is the primary key of this table.</span></span>
-   <span data-ttu-id="e1e7b-108">**Nomecomputer:** Nome del computer che ha registrato il set di dati.</span><span class="sxs-lookup"><span data-stu-id="e1e7b-108">**MachineName:** The name of the computer that logged this data set.</span></span>
-   <span data-ttu-id="e1e7b-109">**ObjectName:** Nome dell'oggetto prestazioni.</span><span class="sxs-lookup"><span data-stu-id="e1e7b-109">**ObjectName:** The name of the performance object.</span></span>
-   <span data-ttu-id="e1e7b-110">**CounterName:** Nome del contatore.</span><span class="sxs-lookup"><span data-stu-id="e1e7b-110">**CounterName:** The name of the counter.</span></span>
-   <span data-ttu-id="e1e7b-111">**CounterType:** Tipo di contatore.</span><span class="sxs-lookup"><span data-stu-id="e1e7b-111">**CounterType:** The counter type.</span></span> <span data-ttu-id="e1e7b-112">Per un elenco dei tipi di contatori e delle relative formule, vedere la sezione relativa ai tipi di contatore del [Kit di distribuzione di Windows Server 2003](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="e1e7b-112">For a list of counter types and their formulas, see the Counter Types section of the [Windows Server 2003 Deployment Kit](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).</span></span>
-   <span data-ttu-id="e1e7b-113">**DefaultScale:** Ridimensionamento predefinito da applicare ai dati del contatore delle prestazioni non elaborati.</span><span class="sxs-lookup"><span data-stu-id="e1e7b-113">**DefaultScale:** The default scaling to be applied to the raw performance counter data.</span></span>
-   <span data-ttu-id="e1e7b-114">**Nomeistanza:** Nome dell'istanza del contatore.</span><span class="sxs-lookup"><span data-stu-id="e1e7b-114">**InstanceName:** The name of the counter instance.</span></span>
-   <span data-ttu-id="e1e7b-115">**InstanceIndex:** Numero di indice dell'istanza del contatore.</span><span class="sxs-lookup"><span data-stu-id="e1e7b-115">**InstanceIndex:** The index number of the counter instance.</span></span>
-   <span data-ttu-id="e1e7b-116">**Padrename:** Alcuni contatori sono associati logicamente ad altri e vengono definiti elementi padre.</span><span class="sxs-lookup"><span data-stu-id="e1e7b-116">**ParentName:** Some counters are logically associated with others, and are referred to as parents.</span></span> <span data-ttu-id="e1e7b-117">Ad esempio, l'elemento padre di un thread è un processo e l'elemento padre di un driver del disco logico è un'unità fisica.</span><span class="sxs-lookup"><span data-stu-id="e1e7b-117">For example, the parent of a thread is a process and the parent of a logical disk driver is a physical drive.</span></span> <span data-ttu-id="e1e7b-118">Questo campo contiene il nome dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="e1e7b-118">This field contains the name of the parent.</span></span> <span data-ttu-id="e1e7b-119">Il valore in questo campo o nel campo **ID oggetto padre** identifica un'istanza padre specifica.</span><span class="sxs-lookup"><span data-stu-id="e1e7b-119">Either the value in this field or the **ParentObjectID** field identifies a specific parent instance.</span></span> <span data-ttu-id="e1e7b-120">Se il valore di questo campo è **null**, è necessario controllare il valore nel campo **ID oggetto padre** per identificare l'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="e1e7b-120">If the value in this field is **NULL**, the value in the **ParentObjectID** field must be checked to identify the parent.</span></span> <span data-ttu-id="e1e7b-121">Se i valori in entrambi i campi sono **null**, il contatore non ha un elemento padre.</span><span class="sxs-lookup"><span data-stu-id="e1e7b-121">If the values in both fields are **NULL**, the counter does not have a parent.</span></span>
-   <span data-ttu-id="e1e7b-122">**ID oggetto padre:** Identificatore univoco dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="e1e7b-122">**ParentObjectID:** The unique identifier of the parent.</span></span> <span data-ttu-id="e1e7b-123">Il valore in questo campo o nel campo **ParentName** identifica un'istanza padre specifica.</span><span class="sxs-lookup"><span data-stu-id="e1e7b-123">The value in either this field or the **ParentName** field identifies a specific parent instance.</span></span> <span data-ttu-id="e1e7b-124">Se il valore di questo campo è **null**, è necessario controllare il valore nel campo **ParentName** per identificare l'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="e1e7b-124">If the value in this field is **NULL**, the value in the **ParentName** field must be checked to identify the parent.</span></span>

 

 
