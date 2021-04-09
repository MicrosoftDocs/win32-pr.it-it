---
title: Proprietà anteprima IVMDisplay (VPCCOMInterfaces. h)
description: Recupera una matrice di pixel che rappresenta un'immagine di anteprima della schermata della macchina virtuale. | Proprietà anteprima IVMDisplay (VPCCOMInterfaces. h)
ms.assetid: e7b57f16-eec1-4461-acfb-742976eff14a
keywords:
- Proprietà anteprima PC virtuale
- Proprietà anteprima Virtual PC, interfaccia IVMDisplay
- Interfaccia IVMDisplay Virtual PC, proprietà Thumbnail
topic_type:
- apiref
api_name:
- IVMDisplay.Thumbnail
- IVMDisplay.get_Thumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0466af2552fbb108f31de94b3f970d6e7d5571b7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969037"
---
# <a name="ivmdisplaythumbnail-property"></a><span data-ttu-id="772c7-107">Proprietà IVMDisplay:: thumbnail</span><span class="sxs-lookup"><span data-stu-id="772c7-107">IVMDisplay::Thumbnail property</span></span>

<span data-ttu-id="772c7-108">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="772c7-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="772c7-109">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="772c7-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="772c7-110">Recupera una matrice di pixel che rappresenta un'immagine di anteprima della schermata della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="772c7-110">Retrieves an array of pixels representing a thumbnail image of the virtual machine's screen.</span></span>

<span data-ttu-id="772c7-111">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="772c7-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="772c7-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="772c7-112">Syntax</span></span>


```C++
HRESULT get_Thumbnail(
  [out, retval] VARIANT *thumbnailImage
);
```



## <a name="property-value"></a><span data-ttu-id="772c7-113">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="772c7-113">Property value</span></span>

<span data-ttu-id="772c7-114">Variante di tipo VT \_ Array VT \| \_ Variant contenente le voci di tipo VT \_ UI4, una per ogni pixel nell'anteprima.</span><span class="sxs-lookup"><span data-stu-id="772c7-114">A variant of type VT\_ARRAY \| VT\_VARIANT containing entries of type VT\_UI4, one for each pixel in the thumbnail.</span></span>

## <a name="error-codes"></a><span data-ttu-id="772c7-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="772c7-115">Error codes</span></span>



| <span data-ttu-id="772c7-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="772c7-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="772c7-117">Significato</span><span class="sxs-lookup"><span data-stu-id="772c7-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="772c7-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="772c7-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="772c7-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="772c7-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="772c7-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="772c7-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="772c7-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="772c7-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="772c7-122"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="772c7-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="772c7-123">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="772c7-123">An unexpected error has occurred.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="772c7-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="772c7-124">Remarks</span></span>

<span data-ttu-id="772c7-125">Questa interfaccia restituisce l'anteprima in modo meno efficiente rispetto al metodo [**\_ GenerateThumbnail**](ivmdisplay--generatethumbnail.md) , ma può essere utilizzata dai client di scripting.</span><span class="sxs-lookup"><span data-stu-id="772c7-125">This interface returns the thumbnail less efficiently than the [**\_GenerateThumbnail**](ivmdisplay--generatethumbnail.md) method, but is usable from scripting clients.</span></span> <span data-ttu-id="772c7-126">L'anteprima è sempre di 64 pixel in larghezza per 48 pixel di altezza.</span><span class="sxs-lookup"><span data-stu-id="772c7-126">The thumbnail is always 64 pixels wide by 48 pixels high.</span></span> <span data-ttu-id="772c7-127">Ogni pixel è 32 bit.</span><span class="sxs-lookup"><span data-stu-id="772c7-127">Each pixel is 32 bits.</span></span> <span data-ttu-id="772c7-128">I primi 64 elementi nella matrice sono la prima riga di pixel nell'anteprima, i successivi 64 elementi sono la seconda riga e così via.</span><span class="sxs-lookup"><span data-stu-id="772c7-128">The first 64 elements in the array is the first row of pixels in the thumbnail, the next 64 elements is the second row, and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="772c7-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="772c7-129">Requirements</span></span>



| <span data-ttu-id="772c7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="772c7-130">Requirement</span></span> | <span data-ttu-id="772c7-131">Valore</span><span class="sxs-lookup"><span data-stu-id="772c7-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="772c7-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="772c7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="772c7-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="772c7-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="772c7-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="772c7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="772c7-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="772c7-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="772c7-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="772c7-136">End of client support</span></span><br/>    | <span data-ttu-id="772c7-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="772c7-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="772c7-138">Prodotto</span><span class="sxs-lookup"><span data-stu-id="772c7-138">Product</span></span><br/>                  | <span data-ttu-id="772c7-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="772c7-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="772c7-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="772c7-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="772c7-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="772c7-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="772c7-142">IID</span><span class="sxs-lookup"><span data-stu-id="772c7-142">IID</span></span><br/>                      | <span data-ttu-id="772c7-143">IID \_ IVMDisplay è definito come 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="772c7-143">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="772c7-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="772c7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="772c7-145">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="772c7-145">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

