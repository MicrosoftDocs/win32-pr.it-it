---
description: Determina la dimensione, in byte, dell'interfaccia COM IStream.
ms.assetid: 8c2f081d-cc41-409e-a868-bcf834e1f128
title: 'Metodo ISCardTypeConv:: SizeOfIStream (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.SizeOfIStream
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 603a01dc6cb4727d59a7fb82c3270c08a495f021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313296"
---
# <a name="iscardtypeconvsizeofistream-method"></a><span data-ttu-id="55006-103">Metodo ISCardTypeConv:: SizeOfIStream</span><span class="sxs-lookup"><span data-stu-id="55006-103">ISCardTypeConv::SizeOfIStream method</span></span>

<span data-ttu-id="55006-104">\[Il metodo **SizeOfIStream** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="55006-104">\[The **SizeOfIStream** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="55006-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="55006-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="55006-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="55006-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="55006-107">Il metodo **SizeOfIStream** determina la dimensione, in byte, dell'interfaccia com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="55006-107">The **SizeOfIStream** method determines the size, in bytes, of the **IStream** COM interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="55006-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55006-108">Syntax</span></span>


```C++
HRESULT SizeOfIStream(
  [in]  LPSTREAM       pStrm,
  [out] ULARGE_INTEGER *puliSize
);
```



## <a name="parameters"></a><span data-ttu-id="55006-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="55006-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55006-110">*pStrm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55006-110">*pStrm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55006-111">Puntatore all'interfaccia com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="55006-111">A pointer to the **IStream** COM interface.</span></span>

</dd> <dt>

<span data-ttu-id="55006-112">*puliSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="55006-112">*puliSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55006-113">Puntatore all'intero senza segno di grandi dimensioni che può ospitare l'intero valore sizeof a 64 bit dell'interfaccia com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="55006-113">A pointer to the unsigned large integer that can hold the entire 64-bit sizeof value of the **IStream** COM interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55006-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55006-114">Return value</span></span>

<span data-ttu-id="55006-115">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="55006-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="55006-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="55006-116">Return code</span></span>                                                                                  | <span data-ttu-id="55006-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55006-117">Description</span></span>                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="55006-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="55006-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="55006-119">La funzione ha avuto esito positivo e *\* puliSize* è la dimensione, in byte, dell'interfaccia COM IStream.</span><span class="sxs-lookup"><span data-stu-id="55006-119">The function succeeded and *\*puliSize* is the size, in bytes, of the IStream COM interface.</span></span><br/> |
| <dl> <span data-ttu-id="55006-120"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="55006-120"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="55006-121">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="55006-121">Unspecified failure occurred.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="55006-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="55006-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="55006-123">Il parametro *puliSize* non è corretto.</span><span class="sxs-lookup"><span data-stu-id="55006-123">The *puliSize* parameter is incorrect.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="55006-124"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="55006-124"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="55006-125">Il parametro *pStrm* non è corretto.</span><span class="sxs-lookup"><span data-stu-id="55006-125">The *pStrm* parameter is incorrect.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="55006-126"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="55006-126"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="55006-127">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="55006-127">Unexpected error occurred.</span></span><br/>                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="55006-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55006-128">Requirements</span></span>



| <span data-ttu-id="55006-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="55006-129">Requirement</span></span> | <span data-ttu-id="55006-130">Valore</span><span class="sxs-lookup"><span data-stu-id="55006-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55006-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55006-131">Minimum supported client</span></span><br/> | <span data-ttu-id="55006-132">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="55006-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="55006-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55006-133">Minimum supported server</span></span><br/> | <span data-ttu-id="55006-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="55006-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="55006-135">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="55006-135">End of client support</span></span><br/>    | <span data-ttu-id="55006-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="55006-136">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="55006-137">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="55006-137">End of server support</span></span><br/>    | <span data-ttu-id="55006-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="55006-138">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="55006-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55006-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="55006-140"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="55006-140"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="55006-141">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="55006-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="55006-142"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="55006-142"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="55006-143">DLL</span><span class="sxs-lookup"><span data-stu-id="55006-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55006-144"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55006-144"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="55006-145">IID</span><span class="sxs-lookup"><span data-stu-id="55006-145">IID</span></span><br/>                      | <span data-ttu-id="55006-146">IID \_ ISCardTypeConv è definito come 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="55006-146">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="55006-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55006-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55006-148">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="55006-148">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="55006-149">Valori restituiti da Smart Card</span><span class="sxs-lookup"><span data-stu-id="55006-149">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
