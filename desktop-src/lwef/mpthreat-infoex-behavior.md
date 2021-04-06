---
title: Struttura MPTHREAT_INFOEX_BEHAVIOR (MpClient. h)
description: Contiene informazioni specifiche relative alla modifica del comportamento.
ms.assetid: 762E755F-5BA1-476D-B395-6617093309C5
keywords:
- Struttura MPTHREAT_INFOEX_BEHAVIOR le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPTHREAT_INFOEX_BEHAVIOR
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_BEHAVIOR
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0bc00aeb56aec38b88f2590211c705079834f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743175"
---
# <a name="mpthreat_infoex_behavior-structure"></a><span data-ttu-id="ea51d-105">\_Struttura del comportamento INFOEX di MPTHREAT \_</span><span class="sxs-lookup"><span data-stu-id="ea51d-105">MPTHREAT\_INFOEX\_BEHAVIOR structure</span></span>

<span data-ttu-id="ea51d-106">Contiene informazioni specifiche relative alla modifica del comportamento.</span><span class="sxs-lookup"><span data-stu-id="ea51d-106">Contains behavior modification-specific information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea51d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea51d-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFOEX_BEHAVIOR {
  ULARGE_INTEGER         SignatureID;
  ULONGLONG              EngineVersion;
  ULONGLONG              ASDeltaSignatureVersion;
  ULONGLONG              AVDeltaSignatureVersion;
  MP_HASH_TYPE           HashType;
  DWORD                  FidelityValue;
  MP_MIDL_STRING  LPWSTR HashValue;
  MP_MIDL_STRING  LPWSTR TargetFileName;
  MP_MIDL_STRING  LPWSTR TargetFileHash;
} MPTHREAT_INFOEX_BEHAVIOR, *PMPTHREAT_INFOEX_BEHAVIOR;
```



## <a name="members"></a><span data-ttu-id="ea51d-108">Members</span><span class="sxs-lookup"><span data-stu-id="ea51d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ea51d-109">**SignatureID**</span><span class="sxs-lookup"><span data-stu-id="ea51d-109">**SignatureID**</span></span>
</dt> <dd>

<span data-ttu-id="ea51d-110">Tipo: **ULARGE \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="ea51d-110">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="ea51d-111">ID firma della modifica del comportamento fornito dal motore al momento del rilevamento.</span><span class="sxs-lookup"><span data-stu-id="ea51d-111">Behavior modification signature ID given by the engine at the time of detection.</span></span>

</dd> <dt>

<span data-ttu-id="ea51d-112">**EngineVersion**</span><span class="sxs-lookup"><span data-stu-id="ea51d-112">**EngineVersion**</span></span>
</dt> <dd>

<span data-ttu-id="ea51d-113">Tipo: **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="ea51d-113">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="ea51d-114">Versione del modulo del motore.</span><span class="sxs-lookup"><span data-stu-id="ea51d-114">Engine module version.</span></span>

</dd> <dt>

<span data-ttu-id="ea51d-115">**ASDeltaSignatureVersion**</span><span class="sxs-lookup"><span data-stu-id="ea51d-115">**ASDeltaSignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="ea51d-116">Tipo: **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="ea51d-116">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="ea51d-117">Versione della firma antispyware.</span><span class="sxs-lookup"><span data-stu-id="ea51d-117">Antispyware signature version.</span></span>

</dd> <dt>

<span data-ttu-id="ea51d-118">**AVDeltaSignatureVersion**</span><span class="sxs-lookup"><span data-stu-id="ea51d-118">**AVDeltaSignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="ea51d-119">Tipo: **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="ea51d-119">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="ea51d-120">Versione della firma antivirus</span><span class="sxs-lookup"><span data-stu-id="ea51d-120">Antivirus signature version</span></span>

</dd> <dt>

<span data-ttu-id="ea51d-121">**HashType**</span><span class="sxs-lookup"><span data-stu-id="ea51d-121">**HashType**</span></span>
</dt> <dd>

<span data-ttu-id="ea51d-122">Tipo: **[ **\_ \_ tipo di hash MP**](mp-hash-type.md)**</span><span class="sxs-lookup"><span data-stu-id="ea51d-122">Type: **[**MP\_HASH\_TYPE**](mp-hash-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ea51d-123">Tipo di hash utilizzato.</span><span class="sxs-lookup"><span data-stu-id="ea51d-123">Hash type used.</span></span> <span data-ttu-id="ea51d-124">Vedere [**\_ \_ tipo di hash MP**](mp-hash-type.md).</span><span class="sxs-lookup"><span data-stu-id="ea51d-124">See [**MP\_HASH\_TYPE**](mp-hash-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea51d-125">**FidelityValue**</span><span class="sxs-lookup"><span data-stu-id="ea51d-125">**FidelityValue**</span></span>
</dt> <dd>

<span data-ttu-id="ea51d-126">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ea51d-126">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="ea51d-127">Valore fedeltà.</span><span class="sxs-lookup"><span data-stu-id="ea51d-127">Fidelity value.</span></span>

</dd> <dt>

<span data-ttu-id="ea51d-128">**HashValue**</span><span class="sxs-lookup"><span data-stu-id="ea51d-128">**HashValue**</span></span>
</dt> <dd>

<span data-ttu-id="ea51d-129">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="ea51d-129">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="ea51d-130">Hash del file.</span><span class="sxs-lookup"><span data-stu-id="ea51d-130">The hash of the file.</span></span>

</dd> <dt>

<span data-ttu-id="ea51d-131">**TargetFileName**</span><span class="sxs-lookup"><span data-stu-id="ea51d-131">**TargetFileName**</span></span>
</dt> <dd>

<span data-ttu-id="ea51d-132">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="ea51d-132">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="ea51d-133">Il percorso e il nome del file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ea51d-133">The path and name of the targeted file.</span></span>

</dd> <dt>

<span data-ttu-id="ea51d-134">**TargetFileHash**</span><span class="sxs-lookup"><span data-stu-id="ea51d-134">**TargetFileHash**</span></span>
</dt> <dd>

<span data-ttu-id="ea51d-135">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="ea51d-135">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="ea51d-136">Hash del file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ea51d-136">The hash of the targeted file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea51d-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea51d-137">Requirements</span></span>



| <span data-ttu-id="ea51d-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea51d-138">Requirement</span></span> | <span data-ttu-id="ea51d-139">Valore</span><span class="sxs-lookup"><span data-stu-id="ea51d-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea51d-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea51d-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ea51d-141">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ea51d-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ea51d-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea51d-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ea51d-143">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ea51d-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea51d-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea51d-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea51d-145"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea51d-145"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea51d-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea51d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea51d-147">**\_tipo di hash MP \_**</span><span class="sxs-lookup"><span data-stu-id="ea51d-147">**MP\_HASH\_TYPE**</span></span>](mp-hash-type.md)
</dt> </dl>

 

 





