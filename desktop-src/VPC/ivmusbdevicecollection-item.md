---
title: Proprietà Item di IVMUSBDeviceCollection (VPCCOMInterfaces. h)
description: Recupera l'oggetto dispositivo USB che corrisponde all'indice specificato.
ms.assetid: 664a038e-7c86-43a9-a376-c913d431dc93
keywords:
- Proprietà elemento Virtual PC
- Proprietà elemento Virtual PC, interfaccia IVMUSBDeviceCollection
- Interfaccia IVMUSBDeviceCollection Virtual PC, proprietà Item
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection.Item
- IVMUSBDeviceCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b50b96de6b19dab15852f58d78480b46da1e9ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477045"
---
# <a name="ivmusbdevicecollectionitem-property"></a><span data-ttu-id="4b683-106">Proprietà IVMUSBDeviceCollection:: Item</span><span class="sxs-lookup"><span data-stu-id="4b683-106">IVMUSBDeviceCollection::Item property</span></span>

<span data-ttu-id="4b683-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4b683-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4b683-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4b683-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4b683-109">Recupera l'oggetto dispositivo USB che corrisponde all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="4b683-109">Retrieves the USB device object that corresponds to the specified index.</span></span>

<span data-ttu-id="4b683-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4b683-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b683-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b683-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long         index,
  [out, retval] IVMUSBDevice **usbDevice
);
```



## <a name="property-value"></a><span data-ttu-id="4b683-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4b683-112">Property value</span></span>

<span data-ttu-id="4b683-113">Oggetto [**IVMUSBDevice**](ivmusbdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="4b683-113">The [**IVMUSBDevice**](ivmusbdevice.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4b683-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="4b683-114">Error codes</span></span>



| <span data-ttu-id="4b683-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="4b683-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="4b683-116">Significato</span><span class="sxs-lookup"><span data-stu-id="4b683-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4b683-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4b683-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4b683-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="4b683-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="4b683-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4b683-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="4b683-120">Il parametro *usbDevice* è **null**.</span><span class="sxs-lookup"><span data-stu-id="4b683-120">The *usbDevice* parameter is **NULL**.</span></span> <br/>                                             |
| <dl> <span data-ttu-id="4b683-121"><dt>Disp \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="4b683-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="4b683-122">L'indice dell'elemento richiesto non corrisponde a un elemento in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="4b683-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="4b683-123"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4b683-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4b683-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="4b683-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="4b683-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b683-125">Requirements</span></span>



| <span data-ttu-id="4b683-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b683-126">Requirement</span></span> | <span data-ttu-id="4b683-127">Valore</span><span class="sxs-lookup"><span data-stu-id="4b683-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b683-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b683-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4b683-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4b683-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4b683-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b683-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4b683-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4b683-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4b683-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4b683-132">End of client support</span></span><br/>    | <span data-ttu-id="4b683-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4b683-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4b683-134">Prodotto</span><span class="sxs-lookup"><span data-stu-id="4b683-134">Product</span></span><br/>                  | <span data-ttu-id="4b683-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4b683-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4b683-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4b683-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b683-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b683-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4b683-138">IID</span><span class="sxs-lookup"><span data-stu-id="4b683-138">IID</span></span><br/>                      | <span data-ttu-id="4b683-139">IID \_ IVMUSBDeviceCollection è definito come 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span><span class="sxs-lookup"><span data-stu-id="4b683-139">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="4b683-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b683-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b683-141">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="4b683-141">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> <dt>

[<span data-ttu-id="4b683-142">**IVMUSBDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="4b683-142">**IVMUSBDeviceCollection**</span></span>](ivmusbdevicecollection.md)
</dt> </dl>

 

