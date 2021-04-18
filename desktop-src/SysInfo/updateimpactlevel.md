---
description: Indica un effetto elevato, medio o basso di un dispositivo che esegue un sistema operativo non aggiornato.
ms.assetid: C7F30B63-66B0-4F37-A05B-7D366A12B640
title: Enumerazione UpdateImpactLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateImpactLevel
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: c18cc7916abbc1dce595df9a21d2fdef3976af11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308091"
---
# <a name="updateimpactlevel-enumeration"></a><span data-ttu-id="96103-103">Enumerazione UpdateImpactLevel</span><span class="sxs-lookup"><span data-stu-id="96103-103">UpdateImpactLevel enumeration</span></span>

<span data-ttu-id="96103-104">Indica un effetto elevato, medio o basso di un dispositivo che esegue un sistema operativo non aggiornato.</span><span class="sxs-lookup"><span data-stu-id="96103-104">Indicates a high, medium, or low impact of a device running an out-of-date OS.</span></span> <span data-ttu-id="96103-105">Questa enumerazione viene in genere utilizzata dalle strutture [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) , che a sua volta sono annidate all'interno dell' [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) restituito da [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment).</span><span class="sxs-lookup"><span data-stu-id="96103-105">This enumeration is generally used by [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) structures, which is in turn nested inside the returned [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) from [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment).</span></span>

## <a name="syntax"></a><span data-ttu-id="96103-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96103-106">Syntax</span></span>


```C++
typedef enum TagUpdateImpactLevel { 
      UpdateImpactLevel_None    = 0,
  UpdateImpactLevel_Low         = 1,
      UpdateImpactLevel_Medium  = 2,
  UpdateImpactLevel_High        = 3
} UpdateImpactLevel;
```



## <a name="constants"></a><span data-ttu-id="96103-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="96103-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="96103-108"><span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span>**UpdateImpactLevel \_ Nessuna**</span><span class="sxs-lookup"><span data-stu-id="96103-108"><span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span> **UpdateImpactLevel\_None**</span></span>
</dt> <dd>

<span data-ttu-id="96103-109">Non è previsto alcun effetto sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="96103-109">There is no foreseeable impact to your device.</span></span> <span data-ttu-id="96103-110">Questo problema può essere dovuto al fatto che il dispositivo è aggiornato o non è aggiornato perché il dispositivo sta rispettando la Windows Update per i periodi di differimento aziendali oppure è obsoleto ma non ha ancora raggiunto la soglia **daysOutOfDate** per raggiungere un livello di inattività maggiore.</span><span class="sxs-lookup"><span data-stu-id="96103-110">This can be because the device is up-to-date, or is not up-to-date because the device is honoring its Windows Update for Business deferral periods, or is out-of-date but has not yet reached the **daysOutOfDate** threshold to reach a higher impact level.</span></span>

</dd> <dt>

<span data-ttu-id="96103-111"><span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**UpdateImpactLevel \_ basso**</span><span class="sxs-lookup"><span data-stu-id="96103-111"><span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**UpdateImpactLevel\_Low**</span></span>
</dt> <dd>

<span data-ttu-id="96103-112">Il dispositivo non esegue il sistema operativo più recente, ma ha un aggiornamento recente.</span><span class="sxs-lookup"><span data-stu-id="96103-112">The device is not running the latest OS, but has a recent update.</span></span>

</dd> <dt>

<span data-ttu-id="96103-113"><span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span>**UpdateImpactLevel \_ Media**</span><span class="sxs-lookup"><span data-stu-id="96103-113"><span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span> **UpdateImpactLevel\_Medium**</span></span>
</dt> <dd>

<span data-ttu-id="96103-114">Nel dispositivo è in esecuzione il sistema operativo più recente, ma è presente un aggiornamento moderatamente recente.</span><span class="sxs-lookup"><span data-stu-id="96103-114">The device is running the latest OS, but has a moderately recent update.</span></span>

</dd> <dt>

<span data-ttu-id="96103-115"><span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**UpdateImpactLevel- \_ alto**</span><span class="sxs-lookup"><span data-stu-id="96103-115"><span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**UpdateImpactLevel\_High**</span></span>
</dt> <dd>

<span data-ttu-id="96103-116">Il dispositivo è obsoleto per molto tempo.</span><span class="sxs-lookup"><span data-stu-id="96103-116">The device has been out-of-date for a long time.</span></span> <span data-ttu-id="96103-117">Questo dispositivo potrebbe avere vulnerabilità di sicurezza e potrebbero mancare correzioni importanti che rendono Windows migliore.</span><span class="sxs-lookup"><span data-stu-id="96103-117">This device may have security vulnerabilities and may be missing important fixes that make Windows run better.</span></span> <span data-ttu-id="96103-118">Quando un dispositivo esegue una versione di Windows che non è più supportata, viene sempre restituito **UpdateImpactLevel \_ High** .</span><span class="sxs-lookup"><span data-stu-id="96103-118">When a device is running a version of Windows that is no longer supported, **UpdateImpactLevel\_High** is always returned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96103-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="96103-119">Remarks</span></span>

<span data-ttu-id="96103-120">Quando viene chiamato [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) , viene restituita una struttura [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) .</span><span class="sxs-lookup"><span data-stu-id="96103-120">When [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) is called, an [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) structure is returned.</span></span> <span data-ttu-id="96103-121">All'interno della struttura sono presenti **assessmentForCurrent** e **assessmentForUpToDate**.</span><span class="sxs-lookup"><span data-stu-id="96103-121">Within the structure there is an **assessmentForCurrent** and **assessmentForUpToDate**.</span></span> <span data-ttu-id="96103-122">Entrambe sono strutture [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) .</span><span class="sxs-lookup"><span data-stu-id="96103-122">Both of these are [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) structures.</span></span> <span data-ttu-id="96103-123">Entrambi i membri hanno un'enumerazione **UpdateImpactLevel** , che indica un livello elevato, medio, basso o nessun effetto per un dispositivo che esegue un sistema operativo non aggiornato.</span><span class="sxs-lookup"><span data-stu-id="96103-123">Both members have an **UpdateImpactLevel** enumeration, which indicates a high, medium, low or no impact for a device running an out-of-date OS.</span></span> <span data-ttu-id="96103-124">Questi livelli sono determinati dal valore di **daysOutOfDate**.</span><span class="sxs-lookup"><span data-stu-id="96103-124">The These levels are determined by the value of **daysOutOfDate**.</span></span>

## <a name="requirements"></a><span data-ttu-id="96103-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96103-125">Requirements</span></span>



| <span data-ttu-id="96103-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="96103-126">Requirement</span></span> | <span data-ttu-id="96103-127">Valore</span><span class="sxs-lookup"><span data-stu-id="96103-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96103-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96103-128">Minimum supported client</span></span><br/> | <span data-ttu-id="96103-129">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="96103-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="96103-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96103-130">Minimum supported server</span></span><br/> | <span data-ttu-id="96103-131">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="96103-131">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="96103-132">IDL</span><span class="sxs-lookup"><span data-stu-id="96103-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="96103-133"><dt>WaaSAPI. idl</dt></span><span class="sxs-lookup"><span data-stu-id="96103-133"><dt>WaaSAPI.idl</dt></span></span> </dl> |



 

 




