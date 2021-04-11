---
title: Sintassi stringa (generalizzata-Time)
description: Formato di stringa dell'ora definito dagli standard ASN. 1. | Sintassi stringa (generalizzata-Time)
ms.assetid: c69ab29b-5877-47d4-b58d-4f103758dfac
ms.tgt_platform: multiple
keywords:
- Stringa (generalizzata-ora) sintassi di AD schema
topic_type:
- apiref
api_name:
- String(Generalized-Time)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e754fe622d3ff6f010521b7bc9b9e4ff7a5f34
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234705"
---
# <a name="stringgeneralized-time-syntax"></a><span data-ttu-id="4b90b-105">Sintassi stringa (generalizzata-Time)</span><span class="sxs-lookup"><span data-stu-id="4b90b-105">String(Generalized-Time) syntax</span></span>

<span data-ttu-id="4b90b-106">Formato di stringa dell'ora definito dagli standard ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="4b90b-106">A time string format defined by ASN.1 standards.</span></span> <span data-ttu-id="4b90b-107">Usare questa sintassi per archiviare i valori temporali nel formato Generalized-Time.</span><span class="sxs-lookup"><span data-stu-id="4b90b-107">Use this syntax for storing time values in Generalized-Time format.</span></span>

<span data-ttu-id="4b90b-108">Il formato della sintassi del Generalized-Time è "ad aaaammgghhmmss. 0Z".</span><span class="sxs-lookup"><span data-stu-id="4b90b-108">The format for the Generalized-Time syntax is "YYYYMMDDHHMMSS.0Z".</span></span> <span data-ttu-id="4b90b-109">Un esempio di valore accettabile è "20010928060000.0 Z".</span><span class="sxs-lookup"><span data-stu-id="4b90b-109">An example of an acceptable value is "20010928060000.0Z".</span></span> <span data-ttu-id="4b90b-110">"Z" indica nessun differenziale temporale.</span><span class="sxs-lookup"><span data-stu-id="4b90b-110">The "Z" indicates no time differential.</span></span> <span data-ttu-id="4b90b-111">Active Directory archivia data/ora come ora di Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="4b90b-111">Active Directory stores date/time as Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="4b90b-112">Se non viene specificato alcun intervallo di tempo, GMT è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="4b90b-112">If no time differential is specified, GMT is the default.</span></span>

<span data-ttu-id="4b90b-113">Se l'ora viene specificata in un fuso orario diverso da GMT, il differenziale tra il fuso orario e il GMT viene aggiunto alla stringa anziché "Z" nel formato "ad aaaammgghhmmss. 0 \[ +/- \] hhmm".</span><span class="sxs-lookup"><span data-stu-id="4b90b-113">If the time is specified in a time zone other than GMT, the differential between the time zone and GMT is appended to the string instead of "Z" in the form "YYYYMMDDHHMMSS.0\[+/-\]HHMM".</span></span> <span data-ttu-id="4b90b-114">Un esempio di valore accettabile è "20010928060000.0 + 0200".</span><span class="sxs-lookup"><span data-stu-id="4b90b-114">An example of an acceptable value is "20010928060000.0+0200".</span></span> <span data-ttu-id="4b90b-115">Il differenziale è basato sulla formula: GMT = local + differenziale.</span><span class="sxs-lookup"><span data-stu-id="4b90b-115">The differential is based on the formula: GMT=Local+differential.</span></span>

<span data-ttu-id="4b90b-116">Per ulteriori informazioni, vedere ISO 8601 e X680.</span><span class="sxs-lookup"><span data-stu-id="4b90b-116">For more information, see ISO 8601 and X680.</span></span>



| <span data-ttu-id="4b90b-117">Voce</span><span class="sxs-lookup"><span data-stu-id="4b90b-117">Entry</span></span> | <span data-ttu-id="4b90b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4b90b-118">Value</span></span> |
|--------------|----------------------------------------------------------------------------|
| <span data-ttu-id="4b90b-119">Nome</span><span class="sxs-lookup"><span data-stu-id="4b90b-119">Name</span></span>         | <span data-ttu-id="4b90b-120">String(Generalized-Time)</span><span class="sxs-lookup"><span data-stu-id="4b90b-120">String(Generalized-Time)</span></span>                                                   |
| <span data-ttu-id="4b90b-121">ID sintassi</span><span class="sxs-lookup"><span data-stu-id="4b90b-121">Syntax ID</span></span>    | <span data-ttu-id="4b90b-122">2.5.5.11</span><span class="sxs-lookup"><span data-stu-id="4b90b-122">2.5.5.11</span></span>                                                                   |
| <span data-ttu-id="4b90b-123">ID OM</span><span class="sxs-lookup"><span data-stu-id="4b90b-123">OM ID</span></span>        | <span data-ttu-id="4b90b-124">24</span><span class="sxs-lookup"><span data-stu-id="4b90b-124">24</span></span>                                                                         |
| <span data-ttu-id="4b90b-125">Tipo MAPI</span><span class="sxs-lookup"><span data-stu-id="4b90b-125">MAPI Type</span></span>    | <span data-ttu-id="4b90b-126">SYSTIME</span><span class="sxs-lookup"><span data-stu-id="4b90b-126">SYSTIME</span></span>                                                                    |
| <span data-ttu-id="4b90b-127">Tipo di annunci</span><span class="sxs-lookup"><span data-stu-id="4b90b-127">ADS Type</span></span>     | <span data-ttu-id="4b90b-128">ADSTYPE \_ \_ ora UTC</span><span class="sxs-lookup"><span data-stu-id="4b90b-128">ADSTYPE\_UTC\_TIME</span></span>                                                         |
| <span data-ttu-id="4b90b-129">Tipo Variant</span><span class="sxs-lookup"><span data-stu-id="4b90b-129">Variant Type</span></span> | <span data-ttu-id="4b90b-130">\_Data VT</span><span class="sxs-lookup"><span data-stu-id="4b90b-130">VT\_DATE</span></span>                                                                   |
| <span data-ttu-id="4b90b-131">Tipo SDS</span><span class="sxs-lookup"><span data-stu-id="4b90b-131">SDS Type</span></span>     | [<span data-ttu-id="4b90b-132">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="4b90b-132">System.DateTime</span></span>](/dotnet/api/system.datetime) |



## <a name="see-also"></a><span data-ttu-id="4b90b-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b90b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b90b-134">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="4b90b-134">System.DateTime</span></span>](/dotnet/api/system.datetime)
</dt> </dl>

 

 
