---
description: Converte un buffer universale di byte (oggetto IStream) in una matrice di byte C/C++ tipica.
ms.assetid: f5b14096-d848-4de9-a5c3-bb60af9044a2
title: 'Metodo ISCardTypeConv:: ConvertByteBufferToByteArray (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteBufferToByteArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7eed6758373aebf08863669b5b81909fca1c0840
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232964"
---
# <a name="iscardtypeconvconvertbytebuffertobytearray-method"></a><span data-ttu-id="fb736-103">Metodo ISCardTypeConv:: ConvertByteBufferToByteArray</span><span class="sxs-lookup"><span data-stu-id="fb736-103">ISCardTypeConv::ConvertByteBufferToByteArray method</span></span>

<span data-ttu-id="fb736-104">\[Il metodo **ConvertByteBufferToByteArray** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="fb736-104">\[The **ConvertByteBufferToByteArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fb736-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fb736-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fb736-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="fb736-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="fb736-107">Il metodo **ConvertByteBufferToByteArray** converte un buffer universale di byte (oggetto **IStream** ) in una matrice di byte C/C++ tipica.</span><span class="sxs-lookup"><span data-stu-id="fb736-107">The **ConvertByteBufferToByteArray** method converts a universal buffer of bytes (**IStream** object) into a typical C/C++ byte array.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb736-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb736-108">Syntax</span></span>


```C++
HRESULT ConvertByteBufferToByteArray(
  [in]  LPBYTEBUFFER pbyBuffer,
  [out] LPBYTEARRAY  *ppArray
);
```



## <a name="parameters"></a><span data-ttu-id="fb736-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb736-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb736-110">*pbyBuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb736-110">*pbyBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb736-111">Puntatore all'oggetto **IStream** da convertire.</span><span class="sxs-lookup"><span data-stu-id="fb736-111">Pointer to the **IStream** object to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="fb736-112">*ppArray* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fb736-112">*ppArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb736-113">Puntatore alla matrice di byte da restituire.</span><span class="sxs-lookup"><span data-stu-id="fb736-113">Pointer to the array of bytes to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb736-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb736-114">Return value</span></span>

<span data-ttu-id="fb736-115">Il metodo restituisce uno dei valori possibili seguenti:</span><span class="sxs-lookup"><span data-stu-id="fb736-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="fb736-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fb736-116">Return code</span></span>                                                                                   | <span data-ttu-id="fb736-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb736-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fb736-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fb736-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fb736-119">Memoria allocata correttamente.</span><span class="sxs-lookup"><span data-stu-id="fb736-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="fb736-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fb736-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="fb736-121">Si è verificato un problema con uno o più parametri passati nella funzione.</span><span class="sxs-lookup"><span data-stu-id="fb736-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="fb736-122"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="fb736-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fb736-123">Un parametro di tipo puntatore non è corretto.</span><span class="sxs-lookup"><span data-stu-id="fb736-123">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="fb736-124"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="fb736-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fb736-125">Memoria disponibile insufficiente per soddisfare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="fb736-125">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="fb736-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb736-126">Requirements</span></span>



| <span data-ttu-id="fb736-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb736-127">Requirement</span></span> | <span data-ttu-id="fb736-128">Valore</span><span class="sxs-lookup"><span data-stu-id="fb736-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb736-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb736-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fb736-130">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fb736-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fb736-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb736-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fb736-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fb736-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fb736-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="fb736-133">End of client support</span></span><br/>    | <span data-ttu-id="fb736-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fb736-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="fb736-135">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="fb736-135">End of server support</span></span><br/>    | <span data-ttu-id="fb736-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fb736-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="fb736-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fb736-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb736-138"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb736-138"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb736-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="fb736-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="fb736-140"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fb736-140"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fb736-141">DLL</span><span class="sxs-lookup"><span data-stu-id="fb736-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb736-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb736-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fb736-143">IID</span><span class="sxs-lookup"><span data-stu-id="fb736-143">IID</span></span><br/>                      | <span data-ttu-id="fb736-144">IID \_ ISCardTypeConv è definito come 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="fb736-144">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="fb736-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb736-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb736-146">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="fb736-146">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="fb736-147">Valori restituiti da Smart Card</span><span class="sxs-lookup"><span data-stu-id="fb736-147">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
