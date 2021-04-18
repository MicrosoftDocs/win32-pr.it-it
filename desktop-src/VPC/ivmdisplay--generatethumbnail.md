---
title: Metodo _GenerateThumbnail IVMDisplay (VPCCOMInterfaces. h)
description: Recupera una matrice di pixel che rappresenta un'immagine di anteprima della schermata della macchina virtuale. | Metodo _GenerateThumbnail IVMDisplay (VPCCOMInterfaces. h)
ms.assetid: c97bb0ff-55cd-491f-a706-0ba15c9a6b54
keywords:
- Metodo di _GenerateThumbnail Virtual PC
- Metodo _GenerateThumbnail Virtual PC, interfaccia IVMDisplay
- Interfaccia IVMDisplay Virtual PC, metodo _GenerateThumbnail
topic_type:
- apiref
api_name:
- IVMDisplay._GenerateThumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4084549de96330761bca4f4ec6da65ca150c96e5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321661"
---
# <a name="ivmdisplay_generatethumbnail-method"></a><span data-ttu-id="3d92c-107">Metodo IVMDisplay:: \_ GenerateThumbnail</span><span class="sxs-lookup"><span data-stu-id="3d92c-107">IVMDisplay::\_GenerateThumbnail method</span></span>

<span data-ttu-id="3d92c-108">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3d92c-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3d92c-109">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3d92c-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3d92c-110">Recupera una matrice di pixel che rappresenta un'immagine di anteprima della schermata della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3d92c-110">Retrieves an array of pixels representing a thumbnail image of the virtual machine's screen.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d92c-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d92c-111">Syntax</span></span>


```C++
HRESULT _GenerateThumbnail(
  [out] unsigned long thumbnailImage[3072]
);
```



## <a name="parameters"></a><span data-ttu-id="3d92c-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d92c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d92c-113">*thumbnailImage* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3d92c-113">*thumbnailImage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d92c-114">Matrice di pixel che rappresenta un'immagine di anteprima della schermata della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3d92c-114">The array of pixels representing a thumbnail image of the virtual machine's screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d92c-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d92c-115">Return value</span></span>

<span data-ttu-id="3d92c-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="3d92c-116">This method can return one of these values.</span></span>



| <span data-ttu-id="3d92c-117">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d92c-117">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="3d92c-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d92c-118">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3d92c-119"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3d92c-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="3d92c-120">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="3d92c-120">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="3d92c-121"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3d92c-121"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="3d92c-122">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="3d92c-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="3d92c-123"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3d92c-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="3d92c-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="3d92c-124">An unexpected error has occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3d92c-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d92c-125">Remarks</span></span>

<span data-ttu-id="3d92c-126">Questa interfaccia restituisce l'anteprima in modo più efficiente rispetto alla proprietà di [**Anteprima**](ivmdisplay-thumbnail.md) , ma non può essere utilizzata dai client di scripting.</span><span class="sxs-lookup"><span data-stu-id="3d92c-126">This interface returns the thumbnail more efficiently than the [**Thumbnail**](ivmdisplay-thumbnail.md) property, but is not usable from scripting clients.</span></span> <span data-ttu-id="3d92c-127">L'anteprima è sempre di 64 pixel in larghezza per 48 pixel di altezza.</span><span class="sxs-lookup"><span data-stu-id="3d92c-127">The thumbnail is always 64 pixels wide by 48 pixels high.</span></span> <span data-ttu-id="3d92c-128">Ogni pixel è 32 bit, dove gli 8 bit superiori rappresentano il valore blu del pixel, i successivi 8 bit rappresentano il valore verde del pixel e gli 8 bit successivi rappresentano il valore rosso del pixel.</span><span class="sxs-lookup"><span data-stu-id="3d92c-128">Each pixel is 32 bits, where the upper 8 bits represent the blue value of the pixel, the next 8 bits represent the green value of the pixel, and the next 8 bits represent the red value of the pixel.</span></span> <span data-ttu-id="3d92c-129">I primi 64 elementi nella matrice sono la prima riga dell'anteprima, i successivi 64 elementi sono la seconda riga e così via.</span><span class="sxs-lookup"><span data-stu-id="3d92c-129">The first 64 elements in the array is the first row of the thumbnail, the next 64 elements is the second row, and so on.</span></span> <span data-ttu-id="3d92c-130">Questo metodo restituisce una matrice statica di pixel, che è più efficiente rispetto alla restituzione di un **SAFEARRAY** di valori **Variant** , ma non è compatibile con i client di scripting.</span><span class="sxs-lookup"><span data-stu-id="3d92c-130">This method returns a static array of pixels, which is more efficient than returning a **SAFEARRAY** of **VARIANT** values, but is not compatible with scripting clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d92c-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d92c-131">Requirements</span></span>



| <span data-ttu-id="3d92c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d92c-132">Requirement</span></span> | <span data-ttu-id="3d92c-133">Valore</span><span class="sxs-lookup"><span data-stu-id="3d92c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d92c-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d92c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3d92c-135">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3d92c-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3d92c-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d92c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3d92c-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3d92c-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3d92c-138">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="3d92c-138">End of client support</span></span><br/>    | <span data-ttu-id="3d92c-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d92c-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3d92c-140">Prodotto</span><span class="sxs-lookup"><span data-stu-id="3d92c-140">Product</span></span><br/>                  | <span data-ttu-id="3d92c-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3d92c-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3d92c-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d92c-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d92c-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d92c-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3d92c-144">IID</span><span class="sxs-lookup"><span data-stu-id="3d92c-144">IID</span></span><br/>                      | <span data-ttu-id="3d92c-145">IID \_ IVMDisplay è definito come 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="3d92c-145">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="3d92c-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d92c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d92c-147">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="3d92c-147">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

