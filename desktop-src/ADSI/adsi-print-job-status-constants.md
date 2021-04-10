---
title: Costanti di stato del processo di stampa ADSI (Adssts. h)
description: Le costanti seguenti vengono utilizzate con la proprietà IADsPrintJobOperations. status per indicare lo stato di un processo di stampa.
ms.assetid: 44a981cc-1098-4b6d-8332-e678953c9112
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- ADS_JOB_PAUSED
- ADS_JOB_ERROR
- ADS_JOB_DELETING
- ADS_JOB_SPOOLING
- ADS_JOB_PRINTING
- ADS_JOB_OFFLINE
- ADS_JOB_PAPEROUT
- ADS_JOB_PRINTED
- ADS_JOB_DELETED
api_location:
- Adssts.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51e83393aa0322ef142ee45b4a893f980293ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964666"
---
# <a name="adsi-print-job-status-constants"></a><span data-ttu-id="0aea4-103">Costanti di stato del processo di stampa ADSI</span><span class="sxs-lookup"><span data-stu-id="0aea4-103">ADSI Print Job Status Constants</span></span>

<span data-ttu-id="0aea4-104">Le costanti seguenti vengono utilizzate con la proprietà [**IADsPrintJobOperations. status**](iadsprintjoboperations-property-methods.md) per indicare lo stato di un processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="0aea4-104">The following constants are used with the [**IADsPrintJobOperations.Status**](iadsprintjoboperations-property-methods.md) property to indicate the status of a print job.</span></span>

<dl> <dt>

<span data-ttu-id="0aea4-105"><span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**\_processo ads \_ sospeso**</span><span class="sxs-lookup"><span data-stu-id="0aea4-105"><span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**ADS\_JOB\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0aea4-106">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0aea4-106">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="0aea4-107">Il processo di stampa è in pausa.</span><span class="sxs-lookup"><span data-stu-id="0aea4-107">The print job is paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0aea4-108"><span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**\_errore del processo ads \_**</span><span class="sxs-lookup"><span data-stu-id="0aea4-108"><span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**ADS\_JOB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0aea4-109">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="0aea4-109">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="0aea4-110">Si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="0aea4-110">An error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0aea4-111"><span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**\_eliminazione del processo ads \_**</span><span class="sxs-lookup"><span data-stu-id="0aea4-111"><span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**ADS\_JOB\_DELETING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0aea4-112">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="0aea4-112">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="0aea4-113">È in corso l'eliminazione del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="0aea4-113">The print job is being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0aea4-114"><span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**\_spooling del processo ads \_**</span><span class="sxs-lookup"><span data-stu-id="0aea4-114"><span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**ADS\_JOB\_SPOOLING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0aea4-115">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="0aea4-115">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="0aea4-116">È in corso lo spooling del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="0aea4-116">The print job is being spooled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0aea4-117"><span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**\_stampa del processo ads \_**</span><span class="sxs-lookup"><span data-stu-id="0aea4-117"><span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**ADS\_JOB\_PRINTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0aea4-118">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="0aea4-118">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="0aea4-119">È in corso la stampa del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="0aea4-119">The print job is being printed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0aea4-120"><span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**\_processo ads \_ offline**</span><span class="sxs-lookup"><span data-stu-id="0aea4-120"><span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**ADS\_JOB\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0aea4-121">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="0aea4-121">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="0aea4-122">La stampante non è in linea.</span><span class="sxs-lookup"><span data-stu-id="0aea4-122">The printer is offline.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0aea4-123"><span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**\_stampa del processo ads \_**</span><span class="sxs-lookup"><span data-stu-id="0aea4-123"><span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**ADS\_JOB\_PAPEROUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0aea4-124">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="0aea4-124">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="0aea4-125">La stampante ha esaurito la carta.</span><span class="sxs-lookup"><span data-stu-id="0aea4-125">The printer is out of paper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0aea4-126"><span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**\_processo ads \_ stampato**</span><span class="sxs-lookup"><span data-stu-id="0aea4-126"><span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**ADS\_JOB\_PRINTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0aea4-127">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="0aea4-127">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="0aea4-128">Il processo di stampa è stato stampato.</span><span class="sxs-lookup"><span data-stu-id="0aea4-128">The print job has been printed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0aea4-129"><span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**\_processo ads \_ eliminato**</span><span class="sxs-lookup"><span data-stu-id="0aea4-129"><span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**ADS\_JOB\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0aea4-130">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="0aea4-130">256 (0x100)</span></span>
</dt> <dt>



<span data-ttu-id="0aea4-131">Il processo di stampa è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="0aea4-131">The print job has been deleted.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0aea4-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0aea4-132">Requirements</span></span>



| <span data-ttu-id="0aea4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aea4-133">Requirement</span></span> | <span data-ttu-id="0aea4-134">Valore</span><span class="sxs-lookup"><span data-stu-id="0aea4-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0aea4-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0aea4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0aea4-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0aea4-136">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="0aea4-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0aea4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0aea4-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0aea4-138">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="0aea4-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0aea4-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aea4-140"><dt>Adssts. h</dt></span><span class="sxs-lookup"><span data-stu-id="0aea4-140"><dt>Adssts.h</dt></span></span> </dl> |



 

 





