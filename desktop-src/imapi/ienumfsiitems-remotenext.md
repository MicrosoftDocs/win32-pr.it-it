---
title: Metodo IEnumFsiItems RemoteNext
description: Supporta un client remoto che desidera recuperare un numero specificato di elementi nella sequenza di enumerazione. | Metodo IEnumFsiItems RemoteNext
ms.assetid: a5ae59ed-08d7-4225-9aec-91049789e8fe
keywords:
- Metodo RemoteNext IMAPi
- Metodo RemoteNext IMAPi, interfaccia IEnumFsiItems
- Interfaccia IEnumFsiItems IMAPi, Metodo RemoteNext
topic_type:
- apiref
api_name:
- IEnumFsiItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e29d3f75cd8e2f83fcd21236661d0d1fa0dabef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530714"
---
# <a name="ienumfsiitemsremotenext-method"></a><span data-ttu-id="711ba-107">Metodo IEnumFsiItems:: RemoteNext</span><span class="sxs-lookup"><span data-stu-id="711ba-107">IEnumFsiItems::RemoteNext method</span></span>

<span data-ttu-id="711ba-108">Supporta un client remoto che desidera recuperare un numero specificato di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="711ba-108">Supports a remote client that wants to retrieve a specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="711ba-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="711ba-109">Syntax</span></span>


```C++
HRESULT RemoteNext(
  [in]  ULONG    celt,
  [out] IFsiItem **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="711ba-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="711ba-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="711ba-111">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="711ba-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="711ba-112">Numero di elementi da recuperare.</span><span class="sxs-lookup"><span data-stu-id="711ba-112">Number of items to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="711ba-113">*rgelt* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="711ba-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="711ba-114">Matrice di interfacce [**IFsiItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem) .</span><span class="sxs-lookup"><span data-stu-id="711ba-114">Array of [**IFsiItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem) interfaces.</span></span> <span data-ttu-id="711ba-115">Al termine, è necessario rilasciare ogni interfaccia in rgelt.</span><span class="sxs-lookup"><span data-stu-id="711ba-115">You must release each interface in rgelt when done.</span></span>

</dd> <dt>

<span data-ttu-id="711ba-116">*pceltFetched* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="711ba-116">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="711ba-117">Numero di elementi restituiti in rgelt.</span><span class="sxs-lookup"><span data-stu-id="711ba-117">Number of elements returned in rgelt.</span></span> <span data-ttu-id="711ba-118">Se *celt* è uno, è possibile impostare *pceltFetched* su **null** .</span><span class="sxs-lookup"><span data-stu-id="711ba-118">You can set *pceltFetched* to **NULL** if *celt* is one.</span></span> <span data-ttu-id="711ba-119">In caso contrario, inizializzare il valore di *pceltFetched* su 0 prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="711ba-119">Otherwise, initialize the value of *pceltFetched* to 0 before calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="711ba-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="711ba-120">Return value</span></span>

<span data-ttu-id="711ba-121">\_Viene restituito S OK quando il numero di elementi richiesti (*celt*) viene restituito correttamente o il numero di elementi restituiti (*pceltFetched*) è inferiore al numero di elementi richiesti.</span><span class="sxs-lookup"><span data-stu-id="711ba-121">S\_OK is returned when the number of requested elements (*celt*) are returned successfully or the number of returned items (*pceltFetched*) is less than the number of requested elements.</span></span>

<span data-ttu-id="711ba-122">Altri codici di riuscita possono essere restituiti come risultato dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="711ba-122">Other success codes may be returned as a result of implementation.</span></span> <span data-ttu-id="711ba-123">I codici di errore seguenti vengono in genere restituiti in caso di errore dell'operazione, ma non rappresentano solo i possibili valori di errore:</span><span class="sxs-lookup"><span data-stu-id="711ba-123">The following error codes are commonly returned on operation failure, but do not represent the only possible error values:</span></span>



| <span data-ttu-id="711ba-124">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="711ba-124">Return code</span></span>                                                                                   | <span data-ttu-id="711ba-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="711ba-125">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="711ba-126"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="711ba-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="711ba-127">Puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="711ba-127">Pointer is not valid.</span></span><br/> <span data-ttu-id="711ba-128">Valore: 0x80004003</span><span class="sxs-lookup"><span data-stu-id="711ba-128">Value: 0x80004003</span></span><br/>                   |
| <dl> <span data-ttu-id="711ba-129"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="711ba-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="711ba-130">Impossibile allocare la memoria necessaria.</span><span class="sxs-lookup"><span data-stu-id="711ba-130">Failed to allocate the required memory.</span></span><br/> <span data-ttu-id="711ba-131">Valore: 0x8007000E</span><span class="sxs-lookup"><span data-stu-id="711ba-131">Value: 0x8007000E</span></span><br/> |
| <dl> <span data-ttu-id="711ba-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="711ba-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="711ba-133">Uno o più argomenti non sono validi.</span><span class="sxs-lookup"><span data-stu-id="711ba-133">One or more arguments are not valid.</span></span><br/> <span data-ttu-id="711ba-134">Valore: 0x80070057</span><span class="sxs-lookup"><span data-stu-id="711ba-134">Value: 0x80070057</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="711ba-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="711ba-135">Requirements</span></span>



| <span data-ttu-id="711ba-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="711ba-136">Requirement</span></span> | <span data-ttu-id="711ba-137">Valore</span><span class="sxs-lookup"><span data-stu-id="711ba-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="711ba-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="711ba-138">Minimum supported client</span></span><br/> | <span data-ttu-id="711ba-139">Windows Vista, \[ solo app desktop Windows XP con SP2\]</span><span class="sxs-lookup"><span data-stu-id="711ba-139">Windows Vista, Windows XP with SP2 \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="711ba-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="711ba-140">Minimum supported server</span></span><br/> | <span data-ttu-id="711ba-141">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="711ba-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="711ba-142">IDL</span><span class="sxs-lookup"><span data-stu-id="711ba-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="711ba-143"><dt>Imapi2fs. idl</dt></span><span class="sxs-lookup"><span data-stu-id="711ba-143"><dt>Imapi2fs.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="711ba-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="711ba-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="711ba-145">**IEnumFsiItems**</span><span class="sxs-lookup"><span data-stu-id="711ba-145">**IEnumFsiItems**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems)
</dt> <dt>

[<span data-ttu-id="711ba-146">IEnumFsiItems:: Next</span><span class="sxs-lookup"><span data-stu-id="711ba-146">IEnumFsiItems::Next</span></span>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumfsiitems-next)
</dt> </dl>

 

 





