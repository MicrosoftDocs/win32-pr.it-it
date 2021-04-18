---
title: Struttura MPFASTPATH_DATA (MpClient. h)
description: Notifica di aggiornamento FastPath.
ms.assetid: E19F153D-DD46-4E27-9A4B-33586794DAC2
keywords:
- Struttura MPFASTPATH_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPFASTPATH_DATA
topic_type:
- apiref
api_name:
- MPFASTPATH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2850a48074fee6984564550683c7fe595d0779ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301408"
---
# <a name="mpfastpath_data-structure"></a><span data-ttu-id="72acb-105">\_Struttura dei dati MPFASTPATH</span><span class="sxs-lookup"><span data-stu-id="72acb-105">MPFASTPATH\_DATA structure</span></span>

<span data-ttu-id="72acb-106">Notifica di aggiornamento FastPath.</span><span class="sxs-lookup"><span data-stu-id="72acb-106">FastPath update notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="72acb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72acb-107">Syntax</span></span>


```C++
typedef struct tagMPFASTPATH_DATA {
  MP_SIGNATURE_TYPE         SignatureType;
  MP_FASTPATH_TYPE          FastPathSignatureType;
  MP_MIDL_STRING LPWSTR     FastPathSignatureVersion;
  ULARGE_INTEGER            CompilationTimestamp;
  MP_PERSISTENCE_LIMIT_TYPE PersistenceType;
  MP_MIDL_STRING LPWSTR     PersistenceValue;
  MP_MIDL_STRING LPWSTR     PersistencePath;
  MP_REMOVAL_REASON         Reason;
} MPFASTPATH_DATA, *PMPFASTPATH_DATA;
```



## <a name="members"></a><span data-ttu-id="72acb-108">Members</span><span class="sxs-lookup"><span data-stu-id="72acb-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="72acb-109">**SignatureType**</span><span class="sxs-lookup"><span data-stu-id="72acb-109">**SignatureType**</span></span>
</dt> <dd>

<span data-ttu-id="72acb-110">Tipo: **[ **\_ \_ tipo di firma MP**](mp-signature-type.md)**</span><span class="sxs-lookup"><span data-stu-id="72acb-110">Type: **[**MP\_SIGNATURE\_TYPE**](mp-signature-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="72acb-111">Tipo di firma.</span><span class="sxs-lookup"><span data-stu-id="72acb-111">Signature type.</span></span>

</dd> <dt>

<span data-ttu-id="72acb-112">**FastPathSignatureType**</span><span class="sxs-lookup"><span data-stu-id="72acb-112">**FastPathSignatureType**</span></span>
</dt> <dd>

<span data-ttu-id="72acb-113">Tipo: **[ **\_ FastPath MP \_**](mp-fastpath-type.md)**</span><span class="sxs-lookup"><span data-stu-id="72acb-113">Type: **[**MP\_FASTPATH\_TYPE**](mp-fastpath-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="72acb-114">Tipo di firma FastPath.</span><span class="sxs-lookup"><span data-stu-id="72acb-114">FastPath signature type.</span></span>

</dd> <dt>

<span data-ttu-id="72acb-115">**FastPathSignatureVersion**</span><span class="sxs-lookup"><span data-stu-id="72acb-115">**FastPathSignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="72acb-116">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="72acb-116">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="72acb-117">Versione della firma FastPath (facoltativa).</span><span class="sxs-lookup"><span data-stu-id="72acb-117">FastPath signature version (optional).</span></span>

</dd> <dt>

<span data-ttu-id="72acb-118">**CompilationTimestamp**</span><span class="sxs-lookup"><span data-stu-id="72acb-118">**CompilationTimestamp**</span></span>
</dt> <dd>

<span data-ttu-id="72acb-119">Tipo: **ULARGE \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="72acb-119">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="72acb-120">Timestamp compilazione (UTC).</span><span class="sxs-lookup"><span data-stu-id="72acb-120">Compilation timestamp (UTC).</span></span>

</dd> <dt>

<span data-ttu-id="72acb-121">**PersistenceType**</span><span class="sxs-lookup"><span data-stu-id="72acb-121">**PersistenceType**</span></span>
</dt> <dd>

<span data-ttu-id="72acb-122">Tipo: **[ **\_ limite di \_ \_ persistenza MP**](mp-persistence-limit-type.md)**</span><span class="sxs-lookup"><span data-stu-id="72acb-122">Type: **[**MP\_PERSISTENCE\_LIMIT\_TYPE**](mp-persistence-limit-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="72acb-123">Tipo di persistenza (facoltativo).</span><span class="sxs-lookup"><span data-stu-id="72acb-123">Persistence type (optional).</span></span>

</dd> <dt>

<span data-ttu-id="72acb-124">**PersistenceValue**</span><span class="sxs-lookup"><span data-stu-id="72acb-124">**PersistenceValue**</span></span>
</dt> <dd>

<span data-ttu-id="72acb-125">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="72acb-125">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="72acb-126">Valore di persistenza (facoltativo).</span><span class="sxs-lookup"><span data-stu-id="72acb-126">Persistence value (optional).</span></span>

</dd> <dt>

<span data-ttu-id="72acb-127">**PersistencePath**</span><span class="sxs-lookup"><span data-stu-id="72acb-127">**PersistencePath**</span></span>
</dt> <dd>

<span data-ttu-id="72acb-128">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="72acb-128">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="72acb-129">Percorso di persistenza (facoltativo).</span><span class="sxs-lookup"><span data-stu-id="72acb-129">Persistence path (optional).</span></span>

</dd> <dt>

<span data-ttu-id="72acb-130">**Motivo**</span><span class="sxs-lookup"><span data-stu-id="72acb-130">**Reason**</span></span>
</dt> <dd>

<span data-ttu-id="72acb-131">Tipo: **[ **\_ \_ motivo della rimozione MP**](mp-removal-reason.md)**</span><span class="sxs-lookup"><span data-stu-id="72acb-131">Type: **[**MP\_REMOVAL\_REASON**](mp-removal-reason.md)**</span></span>

</dd> <dd>

<span data-ttu-id="72acb-132">Motivo della rimozione della firma.</span><span class="sxs-lookup"><span data-stu-id="72acb-132">Reason for signature removal.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72acb-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72acb-133">Requirements</span></span>



| <span data-ttu-id="72acb-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="72acb-134">Requirement</span></span> | <span data-ttu-id="72acb-135">Valore</span><span class="sxs-lookup"><span data-stu-id="72acb-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72acb-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72acb-136">Minimum supported client</span></span><br/> | <span data-ttu-id="72acb-137">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="72acb-137">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="72acb-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72acb-138">Minimum supported server</span></span><br/> | <span data-ttu-id="72acb-139">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="72acb-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="72acb-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="72acb-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="72acb-141"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="72acb-141"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72acb-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72acb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72acb-143">**\_tipo di FastPath MP \_**</span><span class="sxs-lookup"><span data-stu-id="72acb-143">**MP\_FASTPATH\_TYPE**</span></span>](mp-fastpath-type.md)
</dt> <dt>

[<span data-ttu-id="72acb-144">**\_tipo limite di persistenza MP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="72acb-144">**MP\_PERSISTENCE\_LIMIT\_TYPE**</span></span>](mp-persistence-limit-type.md)
</dt> <dt>

[<span data-ttu-id="72acb-145">**\_tipo di firma MP \_**</span><span class="sxs-lookup"><span data-stu-id="72acb-145">**MP\_SIGNATURE\_TYPE**</span></span>](mp-signature-type.md)
</dt> </dl>

 

 





