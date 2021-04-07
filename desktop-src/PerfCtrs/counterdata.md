---
description: La tabella CounterData contiene una riga per ogni contatore raccolto in un determinato momento. Il numero di queste righe sarà elevato.
ms.assetid: 1253a9c7-b440-4ff2-b68c-c52b9b42a58b
title: CounterData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4604ce9886a6c4e3caa847dcf41a2d50b46d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881770"
---
# <a name="counterdata"></a><span data-ttu-id="aecda-104">CounterData</span><span class="sxs-lookup"><span data-stu-id="aecda-104">CounterData</span></span>

<span data-ttu-id="aecda-105">La tabella **counterData** contiene una riga per ogni contatore raccolto in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="aecda-105">The **CounterData** table contains a row for each counter that is collected at a particular time.</span></span> <span data-ttu-id="aecda-106">Il numero di queste righe sarà elevato.</span><span class="sxs-lookup"><span data-stu-id="aecda-106">There will be a large number of these rows.</span></span>

<span data-ttu-id="aecda-107">La tabella **counterData** definisce i campi seguenti:</span><span class="sxs-lookup"><span data-stu-id="aecda-107">The **CounterData** table defines the following fields:</span></span>

-   <span data-ttu-id="aecda-108">**GUID:** GUID per questo set di dati.</span><span class="sxs-lookup"><span data-stu-id="aecda-108">**GUID:** GUID for this data set.</span></span> <span data-ttu-id="aecda-109">Usare questa chiave per unire in join la tabella [**DisplayToID**](displaytoid.md) .</span><span class="sxs-lookup"><span data-stu-id="aecda-109">Use this key to join with the [**DisplayToID**](displaytoid.md) table.</span></span>
-   <span data-ttu-id="aecda-110">**CounterID:** Identifica il contatore.</span><span class="sxs-lookup"><span data-stu-id="aecda-110">**CounterID:** Identifies the counter.</span></span> <span data-ttu-id="aecda-111">Usare questa chiave per unire in join la tabella [**CounterDetails**](counterdetails.md) .</span><span class="sxs-lookup"><span data-stu-id="aecda-111">Use this key to join with the [**CounterDetails**](counterdetails.md) table.</span></span>
-   <span data-ttu-id="aecda-112">**RecordIndex:** Indice di esempio per un identificatore del contatore e un GUID della raccolta specifici.</span><span class="sxs-lookup"><span data-stu-id="aecda-112">**RecordIndex:** The sample index for a specific counter identifier and collection GUID.</span></span> <span data-ttu-id="aecda-113">Il valore aumenta per ogni esempio successivo in questo file di log.</span><span class="sxs-lookup"><span data-stu-id="aecda-113">The value increases for each successive sample in this log file.</span></span>
-   <span data-ttu-id="aecda-114">**CounterDateTime:** Ora in cui è stata avviata la raccolta, in ora UTC.</span><span class="sxs-lookup"><span data-stu-id="aecda-114">**CounterDateTime:** The time the collection was started, in UTC time.</span></span>
-   <span data-ttu-id="aecda-115">**CounterValue:** Valore formattato del contatore.</span><span class="sxs-lookup"><span data-stu-id="aecda-115">**CounterValue:** The formatted value of the counter.</span></span> <span data-ttu-id="aecda-116">Questo valore può essere zero per il primo record se il contatore richiede due esempi per calcolare un valore visualizzabile.</span><span class="sxs-lookup"><span data-stu-id="aecda-116">This value may be zero for the first record if the counter requires two sample to compute a displayable value.</span></span>
-   <span data-ttu-id="aecda-117">**FirstValueA:** Combinare questo valore a 32 bit con il valore di **FirstValueB** per creare il membro **FirstValue** del [**\_ \_ contatore PDH RAW**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span><span class="sxs-lookup"><span data-stu-id="aecda-117">**FirstValueA:** Combine this 32-bit value with the value of **FirstValueB** to create the **FirstValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="aecda-118">**FirstValueA** contiene i bit di ordine inferiore.</span><span class="sxs-lookup"><span data-stu-id="aecda-118">**FirstValueA** contains the low order bits.</span></span>
-   <span data-ttu-id="aecda-119">**FirstValueB:** Combinare questo valore a 32 bit con il valore di **FirstValueA** per creare il membro **FirstValue** del [**\_ \_ contatore PDH RAW**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span><span class="sxs-lookup"><span data-stu-id="aecda-119">**FirstValueB:** Combine this 32-bit value with the value of **FirstValueA** to create the **FirstValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="aecda-120">**FirstValueB** contiene i bit di ordine superiore.</span><span class="sxs-lookup"><span data-stu-id="aecda-120">**FirstValueB** contains the high order bits.</span></span>
-   <span data-ttu-id="aecda-121">**SecondValueA:** Combinare questo valore a 32 bit con il valore di **SecondValueB** per creare il membro **SecondValue** del [**\_ \_ contatore PDH RAW**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span><span class="sxs-lookup"><span data-stu-id="aecda-121">**SecondValueA:** Combine this 32-bit value with the value of **SecondValueB** to create the **SecondValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="aecda-122">**SecondValueA** contiene i bit di ordine inferiore.</span><span class="sxs-lookup"><span data-stu-id="aecda-122">**SecondValueA** contains the low order bits.</span></span>
-   <span data-ttu-id="aecda-123">**SecondValueB:** Combinare questo valore a 32 bit con il valore di **SecondValueA** per creare il membro **SecondValue** del [**\_ \_ contatore PDH RAW**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span><span class="sxs-lookup"><span data-stu-id="aecda-123">**SecondValueB:** Combine this 32-bit value with the value of **SecondValueA** to create the **SecondValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="aecda-124">**SecondValueB** contiene i bit di ordine superiore.</span><span class="sxs-lookup"><span data-stu-id="aecda-124">**SecondValueB** contains the high order bits.</span></span>

<span data-ttu-id="aecda-125">I campi **GUID**, **CounterID** e **RecordIndex** costituiscono la chiave primaria per questa tabella.</span><span class="sxs-lookup"><span data-stu-id="aecda-125">The **GUID**, **CounterID**, and **RecordIndex** fields make up the primary key for this table.</span></span>

 

 



