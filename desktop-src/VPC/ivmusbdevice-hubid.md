---
title: Proprietà IVMUSBDevice HubID (VPCCOMInterfaces. h)
description: Recupera l'identificatore dell'hub a cui è connesso il dispositivo.
ms.assetid: 22e1d8fb-33f4-43a3-883f-174ddafa17c2
keywords:
- Proprietà HubID Virtual PC
- Proprietà HubID Virtual PC, interfaccia IVMUSBDevice
- Interfaccia IVMUSBDevice Virtual PC, proprietà HubID
topic_type:
- apiref
api_name:
- IVMUSBDevice.HubID
- IVMUSBDevice.get_HubID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53faa79ee999022f993070767846ee4e4723c3a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048572"
---
# <a name="ivmusbdevicehubid-property"></a><span data-ttu-id="e604b-106">Proprietà IVMUSBDevice:: HubID</span><span class="sxs-lookup"><span data-stu-id="e604b-106">IVMUSBDevice::HubID property</span></span>

<span data-ttu-id="e604b-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e604b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e604b-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e604b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e604b-109">Recupera l'identificatore dell'hub a cui è connesso il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e604b-109">Retrieves the identifier of the hub on which the device is connected.</span></span>

<span data-ttu-id="e604b-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e604b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e604b-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e604b-111">Syntax</span></span>


```C++
HRESULT get_HubID(
  [out, retval] long *hubID
);
```



## <a name="property-value"></a><span data-ttu-id="e604b-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e604b-112">Property value</span></span>

<span data-ttu-id="e604b-113">Identificatore dell'hub.</span><span class="sxs-lookup"><span data-stu-id="e604b-113">The hub identifier.</span></span> <span data-ttu-id="e604b-114">Questo valore viene assegnato dal driver del connettore USB.</span><span class="sxs-lookup"><span data-stu-id="e604b-114">This value is assigned by the USB connector driver.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e604b-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="e604b-115">Error codes</span></span>



| <span data-ttu-id="e604b-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="e604b-116">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="e604b-117">Significato</span><span class="sxs-lookup"><span data-stu-id="e604b-117">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="e604b-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e604b-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="e604b-119">Metodo completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="e604b-119">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="e604b-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e604b-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="e604b-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="e604b-121">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="e604b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e604b-122">Requirements</span></span>



| <span data-ttu-id="e604b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e604b-123">Requirement</span></span> | <span data-ttu-id="e604b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e604b-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e604b-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e604b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e604b-126">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e604b-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e604b-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e604b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e604b-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e604b-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e604b-129">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="e604b-129">End of client support</span></span><br/>    | <span data-ttu-id="e604b-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e604b-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e604b-131">Prodotto</span><span class="sxs-lookup"><span data-stu-id="e604b-131">Product</span></span><br/>                  | <span data-ttu-id="e604b-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e604b-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e604b-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e604b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e604b-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e604b-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e604b-135">IID</span><span class="sxs-lookup"><span data-stu-id="e604b-135">IID</span></span><br/>                      | <span data-ttu-id="e604b-136">IID \_ IVMUSBDevice è definito come 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="e604b-136">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e604b-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e604b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e604b-138">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="e604b-138">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

