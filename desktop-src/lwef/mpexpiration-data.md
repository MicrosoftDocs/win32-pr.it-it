---
title: Struttura MPEXPIRATION_DATA (MpClient. h)
description: Notifica sullo stato di scadenza del prodotto.
ms.assetid: BF464FFD-16AE-4F46-83CD-E0355478180C
keywords:
- Struttura MPEXPIRATION_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPEXPIRATION_DATA
topic_type:
- apiref
api_name:
- MPEXPIRATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df5e417b1ce6b1d1f4c15d646b44b0ea6c1fade2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301036"
---
# <a name="mpexpiration_data-structure"></a><span data-ttu-id="65e45-105">\_Struttura dei dati MPEXPIRATION</span><span class="sxs-lookup"><span data-stu-id="65e45-105">MPEXPIRATION\_DATA structure</span></span>

<span data-ttu-id="65e45-106">Notifica sullo stato di scadenza del prodotto.</span><span class="sxs-lookup"><span data-stu-id="65e45-106">Product expiration status notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="65e45-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65e45-107">Syntax</span></span>


```C++
typedef struct tagMPEXPIRATION_DATA {
  MP_EXPIRE_REASON       Reason;
  MP_EXPIRE_STATE_REPORT State;
} MPEXPIRATION_DATA, *PMPEXPIRATION_DATA;
```



## <a name="members"></a><span data-ttu-id="65e45-108">Members</span><span class="sxs-lookup"><span data-stu-id="65e45-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="65e45-109">**Motivo**</span><span class="sxs-lookup"><span data-stu-id="65e45-109">**Reason**</span></span>
</dt> <dd>

<span data-ttu-id="65e45-110">Tipo: **\_ \_ motivo scadenza MP**</span><span class="sxs-lookup"><span data-stu-id="65e45-110">Type: **MP\_EXPIRE\_REASON**</span></span>

</dd> <dd>

<span data-ttu-id="65e45-111">Motivo della scadenza.</span><span class="sxs-lookup"><span data-stu-id="65e45-111">Expiration reason.</span></span> <span data-ttu-id="65e45-112">Si tratta di uno dei valori possibili seguenti:</span><span class="sxs-lookup"><span data-stu-id="65e45-112">This is one of the following possible values:</span></span>



| <span data-ttu-id="65e45-113">Valore</span><span class="sxs-lookup"><span data-stu-id="65e45-113">Value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="65e45-114">Significato</span><span class="sxs-lookup"><span data-stu-id="65e45-114">Meaning</span></span>                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| <span id="MP_EXPIRED_UNKNOWN"></span><span id="mp_expired_unknown"></span><dl> <span data-ttu-id="65e45-115"><dt>**MP \_ SCADUTO \_ sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="65e45-115"><dt>**MP\_EXPIRED\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="65e45-116">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="65e45-116">Unknown.</span></span><br/>    |
| <span id="MP_EXPIRED_EVAL"></span><span id="mp_expired_eval"></span><dl> <span data-ttu-id="65e45-117"><dt>**MP \_ Valutazione \_ scaduta**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="65e45-117"><dt>**MP\_EXPIRED\_EVAL**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="65e45-118">Valutazione.</span><span class="sxs-lookup"><span data-stu-id="65e45-118">Evaluation.</span></span><br/> |
| <span id="MP_EXPIRED_WAT"></span><span id="mp_expired_wat"></span><dl> <span data-ttu-id="65e45-119"><dt>**MP \_ \_Wat**</dt> <dt>2</dt> scaduti</span><span class="sxs-lookup"><span data-stu-id="65e45-119"><dt>**MP\_EXPIRED\_WAT**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="65e45-120">Wat.</span><span class="sxs-lookup"><span data-stu-id="65e45-120">WAT.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="65e45-121">**State**</span><span class="sxs-lookup"><span data-stu-id="65e45-121">**State**</span></span>
</dt> <dd>

<span data-ttu-id="65e45-122">Tipo: **\_ \_ \_ report stato di scadenza MP**</span><span class="sxs-lookup"><span data-stu-id="65e45-122">Type: **MP\_EXPIRE\_STATE\_REPORT**</span></span>

</dd> <dd>

<span data-ttu-id="65e45-123">Stato di scadenza.</span><span class="sxs-lookup"><span data-stu-id="65e45-123">Expiration state.</span></span> <span data-ttu-id="65e45-124">Si tratta di uno dei valori possibili seguenti:</span><span class="sxs-lookup"><span data-stu-id="65e45-124">This is one of the following possible values:</span></span>



| <span data-ttu-id="65e45-125">Valore</span><span class="sxs-lookup"><span data-stu-id="65e45-125">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="65e45-126">Significato</span><span class="sxs-lookup"><span data-stu-id="65e45-126">Meaning</span></span>                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| <span id="MP_EXPIRE_STATE_REPORT_UNKNOWN"></span><span id="mp_expire_state_report_unknown"></span><dl> <span data-ttu-id="65e45-127"><dt>**MP \_ \_Rapporto stato scadenza \_ \_ sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="65e45-127"><dt>**MP\_EXPIRE\_STATE\_REPORT\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="65e45-128">Stato sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="65e45-128">State unknown.</span></span><br/> |
| <span id="MP_EXPIRE_STATE_REPORT_VALID"></span><span id="mp_expire_state_report_valid"></span><dl> <span data-ttu-id="65e45-129"><dt>**MP \_ \_Rapporto stato scadenza \_ \_ valido**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="65e45-129"><dt>**MP\_EXPIRE\_STATE\_REPORT\_VALID**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="65e45-130">Nessuna scadenza.</span><span class="sxs-lookup"><span data-stu-id="65e45-130">No expiration.</span></span><br/> |
| <span id="MP_EXPIRE_STATE_REPORT_WARNING"></span><span id="mp_expire_state_report_warning"></span><dl> <span data-ttu-id="65e45-131"><dt>**MP \_ \_ \_ \_ Avviso rapporto di stato scadenza**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="65e45-131"><dt>**MP\_EXPIRE\_STATE\_REPORT\_WARNING**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="65e45-132">Quasi scaduto.</span><span class="sxs-lookup"><span data-stu-id="65e45-132">Near expired.</span></span><br/>  |
| <span id="MP_EXPIRE_STATE_REPORT_EXPIRED"></span><span id="mp_expire_state_report_expired"></span><dl> <span data-ttu-id="65e45-133"><dt>**MP \_ Il \_ report sullo stato di scadenza è \_ \_ scaduto**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="65e45-133"><dt>**MP\_EXPIRE\_STATE\_REPORT\_EXPIRED**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="65e45-134">Scaduto.</span><span class="sxs-lookup"><span data-stu-id="65e45-134">Expired.</span></span><br/>       |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65e45-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65e45-135">Requirements</span></span>



| <span data-ttu-id="65e45-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="65e45-136">Requirement</span></span> | <span data-ttu-id="65e45-137">Valore</span><span class="sxs-lookup"><span data-stu-id="65e45-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65e45-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65e45-138">Minimum supported client</span></span><br/> | <span data-ttu-id="65e45-139">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="65e45-139">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="65e45-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65e45-140">Minimum supported server</span></span><br/> | <span data-ttu-id="65e45-141">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="65e45-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="65e45-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="65e45-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="65e45-143"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="65e45-143"><dt>MpClient.h</dt></span></span> </dl> |



 

 





