---
title: Funzione MpFreeMemory (MpClient. h)
description: Libera la memoria per malware Protection Manager.
ms.assetid: D0B43AE5-756F-4E86-B8A5-8268A41901BC
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpFreeMemory
topic_type:
- apiref
api_name:
- MpFreeMemory
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a15a2845b034a3aa739b1ba2f33a023b742b4b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741010"
---
# <a name="mpfreememory-function"></a><span data-ttu-id="3eaa2-104">MpFreeMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="3eaa2-104">MpFreeMemory function</span></span>

<span data-ttu-id="3eaa2-105">Libera la memoria per malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="3eaa2-105">Frees memory for the malware protection manager.</span></span> <span data-ttu-id="3eaa2-106">Tutti i buffer allocati e restituiti dalle funzioni Malware Protection devono essere liberati dal chiamante tramite questa funzione.</span><span class="sxs-lookup"><span data-stu-id="3eaa2-106">All buffers allocated and returned by malware protection functions must be freed by the caller using this function.</span></span>

## <a name="syntax"></a><span data-ttu-id="3eaa2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3eaa2-107">Syntax</span></span>


```C++
void WINAPI MpFreeMemory(
  _In_ PVOID pMemory
);
```



## <a name="parameters"></a><span data-ttu-id="3eaa2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3eaa2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eaa2-109">*pMemory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3eaa2-109">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eaa2-110">Tipo: **PVOID**</span><span class="sxs-lookup"><span data-stu-id="3eaa2-110">Type: **PVOID**</span></span>

<span data-ttu-id="3eaa2-111">Puntatore alla memoria allocata da una funzione di protezione da malware.</span><span class="sxs-lookup"><span data-stu-id="3eaa2-111">A pointer to memory allocated by a malware protection function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eaa2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3eaa2-112">Return value</span></span>

<span data-ttu-id="3eaa2-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="3eaa2-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3eaa2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3eaa2-114">Remarks</span></span>

<span data-ttu-id="3eaa2-115">Per facilitare la gestione della memoria per i client, malware Protection Manager definisce anche le macro per liberare memoria associata alle varie strutture restituite dalle funzioni di malware Protection.</span><span class="sxs-lookup"><span data-stu-id="3eaa2-115">To facilitate memory management for clients, the malware protection manager also defines macros to free memory associated with various structures returned by malware protection functions.</span></span> <span data-ttu-id="3eaa2-116">Le macro seguenti sono definite nel file di intestazione mpmemfree. h:</span><span class="sxs-lookup"><span data-stu-id="3eaa2-116">The following macros are defined in the header file mpmemfree.h:</span></span>



| <span data-ttu-id="3eaa2-117">Nome</span><span class="sxs-lookup"><span data-stu-id="3eaa2-117">Name</span></span>                            | <span data-ttu-id="3eaa2-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3eaa2-118">Description</span></span>                                                                      |
|---------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3eaa2-119">\_informazioni MPRESOURCE \_ gratuite</span><span class="sxs-lookup"><span data-stu-id="3eaa2-119">MPRESOURCE\_INFO\_FREE</span></span>          | <span data-ttu-id="3eaa2-120">Libera le [**\_ informazioni MPRESOURCE**](mpresource-info.md)allocate.</span><span class="sxs-lookup"><span data-stu-id="3eaa2-120">Frees an allocated [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>                  |
| <span data-ttu-id="3eaa2-121">\_informazioni MPTHREAT \_ gratuite</span><span class="sxs-lookup"><span data-stu-id="3eaa2-121">MPTHREAT\_INFO\_FREE</span></span>            | <span data-ttu-id="3eaa2-122">Libera le [**\_ informazioni MPTHREAT**](mpthreat-info.md)allocate.</span><span class="sxs-lookup"><span data-stu-id="3eaa2-122">Frees an allocated [**MPTHREAT\_INFO**](mpthreat-info.md).</span></span>                      |
| <span data-ttu-id="3eaa2-123">MPTHREAT \_ informazioni localizzate \_ \_ gratuite</span><span class="sxs-lookup"><span data-stu-id="3eaa2-123">MPTHREAT\_LOCALIZED\_INFO\_FREE</span></span> | <span data-ttu-id="3eaa2-124">Libera le [**\_ \_ informazioni localizzate MPTHREAT**](mpthreat-localized-info.md)allocate.</span><span class="sxs-lookup"><span data-stu-id="3eaa2-124">Frees an allocated [**MPTHREAT\_LOCALIZED\_INFO**](mpthreat-localized-info.md).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="3eaa2-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3eaa2-125">Requirements</span></span>



| <span data-ttu-id="3eaa2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3eaa2-126">Requirement</span></span> | <span data-ttu-id="3eaa2-127">Valore</span><span class="sxs-lookup"><span data-stu-id="3eaa2-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3eaa2-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3eaa2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3eaa2-129">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3eaa2-129">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="3eaa2-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3eaa2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3eaa2-131">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3eaa2-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3eaa2-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3eaa2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3eaa2-133"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="3eaa2-133"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="3eaa2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="3eaa2-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3eaa2-135"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3eaa2-135"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3eaa2-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3eaa2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eaa2-137">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="3eaa2-137">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="3eaa2-138">**\_informazioni MPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="3eaa2-138">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="3eaa2-139">**\_informazioni MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="3eaa2-139">**MPTHREAT\_INFO**</span></span>](mpthreat-info.md)
</dt> <dt>

[<span data-ttu-id="3eaa2-140">**\_informazioni localizzate MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="3eaa2-140">**MPTHREAT\_LOCALIZED\_INFO**</span></span>](mpthreat-localized-info.md)
</dt> </dl>

 

 





