---
title: Mapping dei tipi di dati della descrizione del servizio ai tipi di dati IDL
description: Nella tabella seguente viene illustrato il mapping dei tipi di dati XML specificati in una descrizione del servizio ai tipi di dati corrispondenti utilizzati in IDL.
ms.assetid: eeb86177-8c3b-47f1-bbe1-f9aabd2dde76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b5fac697c41f54279ecde7436900434895ff23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045177"
---
# <a name="mapping-service-description-data-types-to-idl-data-types"></a><span data-ttu-id="ff0d3-103">Mapping dei tipi di dati della descrizione del servizio ai tipi di dati IDL</span><span class="sxs-lookup"><span data-stu-id="ff0d3-103">Mapping Service Description Data Types to IDL Data Types</span></span>

<span data-ttu-id="ff0d3-104">Nella tabella seguente viene illustrato il mapping dei tipi di dati XML specificati in una descrizione del servizio ai tipi di dati corrispondenti utilizzati in IDL.</span><span class="sxs-lookup"><span data-stu-id="ff0d3-104">The following table shows the mapping of XML data types specified in a service description to the corresponding data types used in IDL.</span></span>



| <span data-ttu-id="ff0d3-105">Tipo di dati XML</span><span class="sxs-lookup"><span data-stu-id="ff0d3-105">XML Data Type</span></span> | <span data-ttu-id="ff0d3-106">Tipo di dati IDL</span><span class="sxs-lookup"><span data-stu-id="ff0d3-106">IDL Data Type</span></span>  |
|---------------|----------------|
| <span data-ttu-id="ff0d3-107">bin.base64</span><span class="sxs-lookup"><span data-stu-id="ff0d3-107">bin.base64</span></span>    | <span data-ttu-id="ff0d3-108">SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="ff0d3-108">SAFEARRAY</span></span>      |
| <span data-ttu-id="ff0d3-109">bin.hex</span><span class="sxs-lookup"><span data-stu-id="ff0d3-109">bin.hex</span></span>       | <span data-ttu-id="ff0d3-110">SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="ff0d3-110">SAFEARRAY</span></span>      |
| <span data-ttu-id="ff0d3-111">boolean</span><span class="sxs-lookup"><span data-stu-id="ff0d3-111">boolean</span></span>       | <span data-ttu-id="ff0d3-112">\_bool Variant</span><span class="sxs-lookup"><span data-stu-id="ff0d3-112">VARIANT\_BOOL</span></span>  |
| <span data-ttu-id="ff0d3-113">char</span><span class="sxs-lookup"><span data-stu-id="ff0d3-113">char</span></span>          | <span data-ttu-id="ff0d3-114">WCHAR \_ t</span><span class="sxs-lookup"><span data-stu-id="ff0d3-114">wchar\_t</span></span>       |
| <span data-ttu-id="ff0d3-115">Data</span><span class="sxs-lookup"><span data-stu-id="ff0d3-115">date</span></span>          | <span data-ttu-id="ff0d3-116">DATE</span><span class="sxs-lookup"><span data-stu-id="ff0d3-116">DATE</span></span>           |
| <span data-ttu-id="ff0d3-117">dateTime</span><span class="sxs-lookup"><span data-stu-id="ff0d3-117">dateTime</span></span>      | <span data-ttu-id="ff0d3-118">DATE</span><span class="sxs-lookup"><span data-stu-id="ff0d3-118">DATE</span></span>           |
| <span data-ttu-id="ff0d3-119">dateTime.tz</span><span class="sxs-lookup"><span data-stu-id="ff0d3-119">dateTime.tz</span></span>   | <span data-ttu-id="ff0d3-120">DATE</span><span class="sxs-lookup"><span data-stu-id="ff0d3-120">DATE</span></span>           |
| <span data-ttu-id="ff0d3-121">fixed.14.4</span><span class="sxs-lookup"><span data-stu-id="ff0d3-121">fixed.14.4</span></span>    | <span data-ttu-id="ff0d3-122">CY</span><span class="sxs-lookup"><span data-stu-id="ff0d3-122">CY</span></span>             |
| <span data-ttu-id="ff0d3-123">float</span><span class="sxs-lookup"><span data-stu-id="ff0d3-123">float</span></span>         | <span data-ttu-id="ff0d3-124">float</span><span class="sxs-lookup"><span data-stu-id="ff0d3-124">float</span></span>          |
| <span data-ttu-id="ff0d3-125">i1</span><span class="sxs-lookup"><span data-stu-id="ff0d3-125">i1</span></span>            | <span data-ttu-id="ff0d3-126">char</span><span class="sxs-lookup"><span data-stu-id="ff0d3-126">char</span></span>           |
| <span data-ttu-id="ff0d3-127">i2</span><span class="sxs-lookup"><span data-stu-id="ff0d3-127">i2</span></span>            | <span data-ttu-id="ff0d3-128">short</span><span class="sxs-lookup"><span data-stu-id="ff0d3-128">short</span></span>          |
| <span data-ttu-id="ff0d3-129">i4</span><span class="sxs-lookup"><span data-stu-id="ff0d3-129">i4</span></span>            | <span data-ttu-id="ff0d3-130">long</span><span class="sxs-lookup"><span data-stu-id="ff0d3-130">long</span></span>           |
| <span data-ttu-id="ff0d3-131">INT</span><span class="sxs-lookup"><span data-stu-id="ff0d3-131">int</span></span>           | <span data-ttu-id="ff0d3-132">long</span><span class="sxs-lookup"><span data-stu-id="ff0d3-132">long</span></span>           |
| <span data-ttu-id="ff0d3-133">d'acquisto</span><span class="sxs-lookup"><span data-stu-id="ff0d3-133">number</span></span>        | <span data-ttu-id="ff0d3-134">BSTR</span><span class="sxs-lookup"><span data-stu-id="ff0d3-134">BSTR</span></span>           |
| <span data-ttu-id="ff0d3-135">r4</span><span class="sxs-lookup"><span data-stu-id="ff0d3-135">r4</span></span>            | <span data-ttu-id="ff0d3-136">float</span><span class="sxs-lookup"><span data-stu-id="ff0d3-136">float</span></span>          |
| <span data-ttu-id="ff0d3-137">r8</span><span class="sxs-lookup"><span data-stu-id="ff0d3-137">r8</span></span>            | <span data-ttu-id="ff0d3-138">double</span><span class="sxs-lookup"><span data-stu-id="ff0d3-138">double</span></span>         |
| <span data-ttu-id="ff0d3-139">string</span><span class="sxs-lookup"><span data-stu-id="ff0d3-139">string</span></span>        | <span data-ttu-id="ff0d3-140">BSTR</span><span class="sxs-lookup"><span data-stu-id="ff0d3-140">BSTR</span></span>           |
| <span data-ttu-id="ff0d3-141">time</span><span class="sxs-lookup"><span data-stu-id="ff0d3-141">time</span></span>          | <span data-ttu-id="ff0d3-142">DATE</span><span class="sxs-lookup"><span data-stu-id="ff0d3-142">DATE</span></span>           |
| <span data-ttu-id="ff0d3-143">time.tz</span><span class="sxs-lookup"><span data-stu-id="ff0d3-143">time.tz</span></span>       | <span data-ttu-id="ff0d3-144">DATE</span><span class="sxs-lookup"><span data-stu-id="ff0d3-144">DATE</span></span>           |
| <span data-ttu-id="ff0d3-145">ui1</span><span class="sxs-lookup"><span data-stu-id="ff0d3-145">ui1</span></span>           | <span data-ttu-id="ff0d3-146">unsigned char</span><span class="sxs-lookup"><span data-stu-id="ff0d3-146">unsigned char</span></span>  |
| <span data-ttu-id="ff0d3-147">ui2</span><span class="sxs-lookup"><span data-stu-id="ff0d3-147">ui2</span></span>           | <span data-ttu-id="ff0d3-148">unsigned short</span><span class="sxs-lookup"><span data-stu-id="ff0d3-148">unsigned short</span></span> |
| <span data-ttu-id="ff0d3-149">ui4</span><span class="sxs-lookup"><span data-stu-id="ff0d3-149">ui4</span></span>           | <span data-ttu-id="ff0d3-150">unsigned long</span><span class="sxs-lookup"><span data-stu-id="ff0d3-150">unsigned long</span></span>  |
| <span data-ttu-id="ff0d3-151">Uri</span><span class="sxs-lookup"><span data-stu-id="ff0d3-151">uri</span></span>           | <span data-ttu-id="ff0d3-152">BSTR</span><span class="sxs-lookup"><span data-stu-id="ff0d3-152">BSTR</span></span>           |
| <span data-ttu-id="ff0d3-153">uuid</span><span class="sxs-lookup"><span data-stu-id="ff0d3-153">uuid</span></span>          | <span data-ttu-id="ff0d3-154">BSTR</span><span class="sxs-lookup"><span data-stu-id="ff0d3-154">BSTR</span></span>           |



 

 

 




