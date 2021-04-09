---
title: Proprietà porta IVMUSBDevice (VPCCOMInterfaces. h)
description: Recupera l'identificatore della porta a cui è connesso il dispositivo.
ms.assetid: 612c0eba-aa80-4539-a883-f05d32d13b41
keywords:
- Proprietà porta PC virtuale
- Proprietà porta Virtual PC, interfaccia IVMUSBDevice
- Interfaccia IVMUSBDevice Virtual PC, proprietà porta
topic_type:
- apiref
api_name:
- IVMUSBDevice.Port
- IVMUSBDevice.get_Port
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb821921d10b23fdb17256372708650d060e253b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743239"
---
# <a name="ivmusbdeviceport-property"></a><span data-ttu-id="add3c-106">IVMUSBDevice::P proprietà Ort</span><span class="sxs-lookup"><span data-stu-id="add3c-106">IVMUSBDevice::Port property</span></span>

<span data-ttu-id="add3c-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="add3c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="add3c-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="add3c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="add3c-109">Recupera l'identificatore della porta a cui è connesso il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="add3c-109">Retrieves the identifier of the port on which the device is connected.</span></span>

<span data-ttu-id="add3c-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="add3c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="add3c-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="add3c-111">Syntax</span></span>


```C++
HRESULT get_Port(
  [out, retval] long *port
);
```



## <a name="property-value"></a><span data-ttu-id="add3c-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="add3c-112">Property value</span></span>

<span data-ttu-id="add3c-113">Identificatore di porta.</span><span class="sxs-lookup"><span data-stu-id="add3c-113">The port identifier.</span></span> <span data-ttu-id="add3c-114">Questo valore viene assegnato dal driver del connettore USB.</span><span class="sxs-lookup"><span data-stu-id="add3c-114">This value is assigned by the USB connector driver.</span></span>

## <a name="error-codes"></a><span data-ttu-id="add3c-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="add3c-115">Error codes</span></span>



| <span data-ttu-id="add3c-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="add3c-116">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="add3c-117">Significato</span><span class="sxs-lookup"><span data-stu-id="add3c-117">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="add3c-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="add3c-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="add3c-119">Metodo completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="add3c-119">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="add3c-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="add3c-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="add3c-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="add3c-121">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="add3c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="add3c-122">Requirements</span></span>



| <span data-ttu-id="add3c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="add3c-123">Requirement</span></span> | <span data-ttu-id="add3c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="add3c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="add3c-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="add3c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="add3c-126">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="add3c-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="add3c-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="add3c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="add3c-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="add3c-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="add3c-129">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="add3c-129">End of client support</span></span><br/>    | <span data-ttu-id="add3c-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="add3c-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="add3c-131">Prodotto</span><span class="sxs-lookup"><span data-stu-id="add3c-131">Product</span></span><br/>                  | <span data-ttu-id="add3c-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="add3c-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="add3c-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="add3c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="add3c-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="add3c-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="add3c-135">IID</span><span class="sxs-lookup"><span data-stu-id="add3c-135">IID</span></span><br/>                      | <span data-ttu-id="add3c-136">IID \_ IVMUSBDevice è definito come 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="add3c-136">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="add3c-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="add3c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="add3c-138">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="add3c-138">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

