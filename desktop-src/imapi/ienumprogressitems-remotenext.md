---
title: Metodo IEnumProgressItems RemoteNext
description: Supporta un client remoto che desidera recuperare un numero specificato di elementi nella sequenza di enumerazione. | Metodo IEnumProgressItems RemoteNext
ms.assetid: c5f85ca3-1bad-49fd-9e67-d41135cd837d
keywords:
- Metodo RemoteNext IMAPi
- Metodo RemoteNext IMAPi, interfaccia IEnumProgressItems
- Interfaccia IEnumProgressItems IMAPi, Metodo RemoteNext
topic_type:
- apiref
api_name:
- IEnumProgressItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a088a1be640c6653a8a8ccd8b00cf21bd027ecd7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321631"
---
# <a name="ienumprogressitemsremotenext-method"></a><span data-ttu-id="65aee-107">Metodo IEnumProgressItems:: RemoteNext</span><span class="sxs-lookup"><span data-stu-id="65aee-107">IEnumProgressItems::RemoteNext method</span></span>

<span data-ttu-id="65aee-108">Supporta un client remoto che desidera recuperare un numero specificato di elementi nella sequenza di enumerazione</span><span class="sxs-lookup"><span data-stu-id="65aee-108">Supports a remote client that wants to retrieve a specified number of items in the enumeration sequence</span></span>

## <a name="syntax"></a><span data-ttu-id="65aee-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65aee-109">Syntax</span></span>


```C++
HRESULT RemoteNext(
  [in]  ULONG         celt,
  [out] IProgressItem **rgelt,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="65aee-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="65aee-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65aee-111">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65aee-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65aee-112">Numero di elementi da recuperare.</span><span class="sxs-lookup"><span data-stu-id="65aee-112">Number of items to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="65aee-113">*rgelt* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="65aee-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65aee-114">Matrice di interfacce [**IProgressItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem) .</span><span class="sxs-lookup"><span data-stu-id="65aee-114">Array of [**IProgressItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem) interfaces.</span></span> <span data-ttu-id="65aee-115">Al termine, è necessario rilasciare ogni interfaccia in rgelt.</span><span class="sxs-lookup"><span data-stu-id="65aee-115">You must release each interface in rgelt when done.</span></span>

</dd> <dt>

<span data-ttu-id="65aee-116">*pceltFetched* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="65aee-116">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65aee-117">Numero di elementi restituiti in rgelt.</span><span class="sxs-lookup"><span data-stu-id="65aee-117">Number of elements returned in rgelt.</span></span> <span data-ttu-id="65aee-118">Se *celt* è uno, è possibile impostare *pceltFetched* su **null** .</span><span class="sxs-lookup"><span data-stu-id="65aee-118">You can set *pceltFetched* to **NULL** if *celt* is one.</span></span> <span data-ttu-id="65aee-119">In caso contrario, inizializzare il valore di *pceltFetched* su 0 prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="65aee-119">Otherwise, initialize the value of *pceltFetched* to 0 before calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65aee-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="65aee-120">Return value</span></span>

<span data-ttu-id="65aee-121">\_Viene restituito S OK quando il numero di elementi richiesti (*celt*) viene restituito correttamente o il numero di elementi restituiti (*pceltFetched*) è inferiore al numero di elementi richiesti.</span><span class="sxs-lookup"><span data-stu-id="65aee-121">S\_OK is returned when the number of requested elements (*celt*) are returned successfully or the number of returned items (*pceltFetched*) is less than the number of requested elements.</span></span>

<span data-ttu-id="65aee-122">Altri codici di riuscita possono essere restituiti come risultato dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="65aee-122">Other success codes may be returned as a result of implementation.</span></span> <span data-ttu-id="65aee-123">I codici di errore seguenti vengono in genere restituiti in caso di errore dell'operazione, ma non rappresentano solo i possibili valori di errore:</span><span class="sxs-lookup"><span data-stu-id="65aee-123">The following error codes are commonly returned on operation failure, but do not represent the only possible error values:</span></span>



| <span data-ttu-id="65aee-124">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="65aee-124">Return code</span></span>                                                                                   | <span data-ttu-id="65aee-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65aee-125">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="65aee-126"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="65aee-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="65aee-127">Puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="65aee-127">Pointer is not valid.</span></span><br/> <span data-ttu-id="65aee-128">Valore: 0x80004003</span><span class="sxs-lookup"><span data-stu-id="65aee-128">Value: 0x80004003</span></span><br/>                   |
| <dl> <span data-ttu-id="65aee-129"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="65aee-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="65aee-130">Impossibile allocare la memoria necessaria.</span><span class="sxs-lookup"><span data-stu-id="65aee-130">Failed to allocate the required memory.</span></span><br/> <span data-ttu-id="65aee-131">Valore: 0x8007000E</span><span class="sxs-lookup"><span data-stu-id="65aee-131">Value: 0x8007000E</span></span><br/> |
| <dl> <span data-ttu-id="65aee-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="65aee-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="65aee-133">Uno o più argomenti non sono validi.</span><span class="sxs-lookup"><span data-stu-id="65aee-133">One or more arguments are not valid.</span></span><br/> <span data-ttu-id="65aee-134">Valore: 0x80070057</span><span class="sxs-lookup"><span data-stu-id="65aee-134">Value: 0x80070057</span></span><br/>    |
| <dl> <span data-ttu-id="65aee-135"><dt>**E \_ Non previsto**</dt></span><span class="sxs-lookup"><span data-stu-id="65aee-135"><dt> **E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="65aee-136">Errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="65aee-136">An unexpected failure occurred.</span></span><br/> <span data-ttu-id="65aee-137">Valore: 0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="65aee-137">Value: 0x8000FFFF</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="65aee-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="65aee-138">Remarks</span></span>

<span data-ttu-id="65aee-139">Se il numero di elementi rimasti nella sequenza è inferiore a quello richiesto, vengono recuperati gli elementi rimanenti.</span><span class="sxs-lookup"><span data-stu-id="65aee-139">If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="65aee-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65aee-140">Requirements</span></span>



| <span data-ttu-id="65aee-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="65aee-141">Requirement</span></span> | <span data-ttu-id="65aee-142">Valore</span><span class="sxs-lookup"><span data-stu-id="65aee-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65aee-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65aee-143">Minimum supported client</span></span><br/> | <span data-ttu-id="65aee-144">Windows Vista, \[ solo app desktop Windows XP con SP2\]</span><span class="sxs-lookup"><span data-stu-id="65aee-144">Windows Vista, Windows XP with SP2 \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="65aee-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65aee-145">Minimum supported server</span></span><br/> | <span data-ttu-id="65aee-146">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="65aee-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="65aee-147">IDL</span><span class="sxs-lookup"><span data-stu-id="65aee-147">IDL</span></span><br/>                      | <dl> <span data-ttu-id="65aee-148"><dt>Imapi2fs. idl</dt></span><span class="sxs-lookup"><span data-stu-id="65aee-148"><dt>Imapi2fs.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65aee-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65aee-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65aee-150">**IEnumProgressItems**</span><span class="sxs-lookup"><span data-stu-id="65aee-150">**IEnumProgressItems**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems)
</dt> <dt>

[<span data-ttu-id="65aee-151">IEnumProgressItems:: Next</span><span class="sxs-lookup"><span data-stu-id="65aee-151">IEnumProgressItems::Next</span></span>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumprogressitems-next)
</dt> </dl>

 

 





