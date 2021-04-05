---
description: Converte un buffer universale di byte (oggetto IStream) in un SAFEARRAY di unsigned char (byte).
ms.assetid: b8d052e8-2f36-42cf-b88c-ace215a2fc68
title: 'Metodo ISCardTypeConv:: ConvertByteBufferToSafeArray (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteBufferToSafeArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: eb6f646df60ab505c41c45bea34fd2d59aa3bb4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757283"
---
# <a name="iscardtypeconvconvertbytebuffertosafearray-method"></a><span data-ttu-id="285bf-103">Metodo ISCardTypeConv:: ConvertByteBufferToSafeArray</span><span class="sxs-lookup"><span data-stu-id="285bf-103">ISCardTypeConv::ConvertByteBufferToSafeArray method</span></span>

<span data-ttu-id="285bf-104">\[Il metodo **ConvertByteBufferToSafeArray** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="285bf-104">\[The **ConvertByteBufferToSafeArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="285bf-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="285bf-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="285bf-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="285bf-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="285bf-107">Il metodo **ConvertByteBufferToSafeArray** converte un buffer universale di byte (oggetto **IStream** ) in un SAFEARRAY di unsigned char (byte).</span><span class="sxs-lookup"><span data-stu-id="285bf-107">The **ConvertByteBufferToSafeArray** method converts a universal buffer of bytes (**IStream** object) into a SAFEARRAY of unsigned char (byte).</span></span>

## <a name="syntax"></a><span data-ttu-id="285bf-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="285bf-108">Syntax</span></span>


```C++
HRESULT ConvertByteBufferToSafeArray(
  [in]  LPBYTEBUFFER pbyBuffer,
  [out] LPSAFEARRAY  *ppbyArray
);
```



## <a name="parameters"></a><span data-ttu-id="285bf-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="285bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="285bf-110">*pbyBuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="285bf-110">*pbyBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="285bf-111">Puntatore all'oggetto **IStream** da convertire.</span><span class="sxs-lookup"><span data-stu-id="285bf-111">Pointer to the **IStream** object to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="285bf-112">*ppbyArray* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="285bf-112">*ppbyArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="285bf-113">Puntatore all'elemento SAFEARRAY da restituire.</span><span class="sxs-lookup"><span data-stu-id="285bf-113">Pointer to the SAFEARRAY to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="285bf-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="285bf-114">Return value</span></span>

<span data-ttu-id="285bf-115">Il metodo restituisce uno dei valori possibili seguenti:</span><span class="sxs-lookup"><span data-stu-id="285bf-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="285bf-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="285bf-116">Return code</span></span>                                                                                   | <span data-ttu-id="285bf-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="285bf-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="285bf-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="285bf-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="285bf-119">Memoria allocata correttamente.</span><span class="sxs-lookup"><span data-stu-id="285bf-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="285bf-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="285bf-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="285bf-121">Si è verificato un problema con uno o più parametri passati nella funzione.</span><span class="sxs-lookup"><span data-stu-id="285bf-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="285bf-122"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="285bf-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="285bf-123">Un parametro di tipo puntatore non è corretto.</span><span class="sxs-lookup"><span data-stu-id="285bf-123">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="285bf-124"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="285bf-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="285bf-125">Memoria disponibile insufficiente per soddisfare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="285bf-125">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="285bf-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="285bf-126">Requirements</span></span>



| <span data-ttu-id="285bf-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="285bf-127">Requirement</span></span> | <span data-ttu-id="285bf-128">Valore</span><span class="sxs-lookup"><span data-stu-id="285bf-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="285bf-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="285bf-129">Minimum supported client</span></span><br/> | <span data-ttu-id="285bf-130">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="285bf-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="285bf-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="285bf-131">Minimum supported server</span></span><br/> | <span data-ttu-id="285bf-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="285bf-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="285bf-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="285bf-133">End of client support</span></span><br/>    | <span data-ttu-id="285bf-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="285bf-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="285bf-135">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="285bf-135">End of server support</span></span><br/>    | <span data-ttu-id="285bf-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="285bf-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="285bf-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="285bf-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="285bf-138"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="285bf-138"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="285bf-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="285bf-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="285bf-140"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="285bf-140"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="285bf-141">DLL</span><span class="sxs-lookup"><span data-stu-id="285bf-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="285bf-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="285bf-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="285bf-143">IID</span><span class="sxs-lookup"><span data-stu-id="285bf-143">IID</span></span><br/>                      | <span data-ttu-id="285bf-144">IID \_ ISCardTypeConv è definito come 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="285bf-144">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="285bf-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="285bf-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="285bf-146">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="285bf-146">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="285bf-147">Valori restituiti da Smart Card</span><span class="sxs-lookup"><span data-stu-id="285bf-147">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
