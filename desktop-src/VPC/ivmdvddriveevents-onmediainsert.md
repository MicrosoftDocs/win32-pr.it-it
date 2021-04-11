---
title: Metodo IVMDVDDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
description: Riceve la notifica che i supporti sono stati inseriti nell'unità. | Metodo IVMDVDDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
ms.assetid: a246e2dd-638e-4d2f-9089-74771cd8bb2b
keywords:
- Metodo OnMediaInsert Virtual PC
- Metodo OnMediaInsert Virtual PC, interfaccia IVMDVDDriveEvents
- Interfaccia IVMDVDDriveEvents Virtual PC, metodo OnMediaInsert
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 883f7990de17a9d1dbb21db9651e0f5ad4ec74aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969062"
---
# <a name="ivmdvddriveeventsonmediainsert-method"></a><span data-ttu-id="cc430-107">Metodo IVMDVDDriveEvents:: OnMediaInsert</span><span class="sxs-lookup"><span data-stu-id="cc430-107">IVMDVDDriveEvents::OnMediaInsert method</span></span>

<span data-ttu-id="cc430-108">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cc430-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cc430-109">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cc430-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cc430-110">Riceve la notifica che i supporti sono stati inseriti nell'unità.</span><span class="sxs-lookup"><span data-stu-id="cc430-110">Receives notification that media has been inserted into the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc430-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc430-111">Syntax</span></span>


```C++
HRESULT OnMediaInsert(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a><span data-ttu-id="cc430-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc430-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc430-113">*mediaPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc430-113">*mediaPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc430-114">Lettera o percorso dell'unità host nell'immagine ISO.</span><span class="sxs-lookup"><span data-stu-id="cc430-114">The host drive letter, or path, to the ISO image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc430-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc430-115">Return value</span></span>

<span data-ttu-id="cc430-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cc430-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cc430-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cc430-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc430-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc430-118">Remarks</span></span>

<span data-ttu-id="cc430-119">Questo metodo viene chiamato quando viene inserito un supporto (un'immagine ISO o un disco in un'unità host).</span><span class="sxs-lookup"><span data-stu-id="cc430-119">This method is called when media (an ISO image or a disc in a host drive) is inserted.</span></span> <span data-ttu-id="cc430-120">Il programma client deve implementare questo metodo di interfaccia per ricevere la notifica dell' \_ evento OnInsert di vmDVDDriveEvent originato da [**IVMDVDDrive**](ivmdvddrive.md).</span><span class="sxs-lookup"><span data-stu-id="cc430-120">The client program must implement this interface method to receive notification of the vmDVDDriveEvent\_OnInsert event originating from [**IVMDVDDrive**](ivmdvddrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc430-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc430-121">Requirements</span></span>



| <span data-ttu-id="cc430-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc430-122">Requirement</span></span> | <span data-ttu-id="cc430-123">Valore</span><span class="sxs-lookup"><span data-stu-id="cc430-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc430-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc430-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cc430-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cc430-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cc430-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc430-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cc430-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cc430-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cc430-128">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="cc430-128">End of client support</span></span><br/>    | <span data-ttu-id="cc430-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cc430-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cc430-130">Prodotto</span><span class="sxs-lookup"><span data-stu-id="cc430-130">Product</span></span><br/>                  | <span data-ttu-id="cc430-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cc430-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cc430-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc430-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc430-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc430-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cc430-134">IID</span><span class="sxs-lookup"><span data-stu-id="cc430-134">IID</span></span><br/>                      | <span data-ttu-id="cc430-135">DIID \_ IVMDVDDriveEvents è definito come c2a7d8e9-E76C-4EB8-94f7-71a5122d249b</span><span class="sxs-lookup"><span data-stu-id="cc430-135">DIID\_IVMDVDDriveEvents is defined as c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="cc430-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc430-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc430-137">**IVMDVDDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="cc430-137">**IVMDVDDriveEvents**</span></span>](ivmdvddriveevents.md)
</dt> </dl>

 

