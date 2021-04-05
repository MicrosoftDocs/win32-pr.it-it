---
title: Metodo IVMDVDDriveEvents OnMediaEject (VPCCOMInterfaces. h)
description: Riceve una notifica che segnala che il supporto è stato espulso dall'unità. | Metodo IVMDVDDriveEvents OnMediaEject (VPCCOMInterfaces. h)
ms.assetid: ec90fbce-7123-4bfa-abab-300e916fa089
keywords:
- Metodo OnMediaEject Virtual PC
- Metodo OnMediaEject Virtual PC, interfaccia IVMDVDDriveEvents
- Interfaccia IVMDVDDriveEvents Virtual PC, metodo OnMediaEject
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaEject
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b66091dcc6cc5ee28ab6e0cb3d58e3e647e41cb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886095"
---
# <a name="ivmdvddriveeventsonmediaeject-method"></a><span data-ttu-id="12723-107">Metodo IVMDVDDriveEvents:: OnMediaEject</span><span class="sxs-lookup"><span data-stu-id="12723-107">IVMDVDDriveEvents::OnMediaEject method</span></span>

<span data-ttu-id="12723-108">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="12723-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="12723-109">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="12723-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="12723-110">Riceve una notifica che segnala che il supporto è stato espulso dall'unità.</span><span class="sxs-lookup"><span data-stu-id="12723-110">Receives notification that media has been ejected from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="12723-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12723-111">Syntax</span></span>


```C++
HRESULT OnMediaEject(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a><span data-ttu-id="12723-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="12723-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12723-113">*mediaPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12723-113">*mediaPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12723-114">Lettera o percorso dell'unità host nell'immagine ISO.</span><span class="sxs-lookup"><span data-stu-id="12723-114">The host drive letter, or path, to the ISO image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12723-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12723-115">Return value</span></span>

<span data-ttu-id="12723-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="12723-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="12723-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="12723-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="12723-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="12723-118">Remarks</span></span>

<span data-ttu-id="12723-119">Questo metodo viene chiamato quando viene espulso il supporto (un'immagine ISO o un disco in un'unità host).</span><span class="sxs-lookup"><span data-stu-id="12723-119">This method is called when media (an ISO image or a disc in a host drive) is ejected.</span></span> <span data-ttu-id="12723-120">Il programma client deve implementare questo metodo di interfaccia per ricevere una notifica dell' \_ evento vmDVDDriveEvent oneject originato da [**IVMDVDDrive**](ivmdvddrive.md).</span><span class="sxs-lookup"><span data-stu-id="12723-120">The client program must implement this interface method to receive notification of the vmDVDDriveEvent\_OnEject event originating from [**IVMDVDDrive**](ivmdvddrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="12723-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12723-121">Requirements</span></span>



| <span data-ttu-id="12723-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="12723-122">Requirement</span></span> | <span data-ttu-id="12723-123">Valore</span><span class="sxs-lookup"><span data-stu-id="12723-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="12723-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12723-124">Minimum supported client</span></span><br/> | <span data-ttu-id="12723-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="12723-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="12723-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12723-126">Minimum supported server</span></span><br/> | <span data-ttu-id="12723-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="12723-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="12723-128">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="12723-128">End of client support</span></span><br/>    | <span data-ttu-id="12723-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="12723-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="12723-130">Prodotto</span><span class="sxs-lookup"><span data-stu-id="12723-130">Product</span></span><br/>                  | <span data-ttu-id="12723-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="12723-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="12723-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12723-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="12723-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="12723-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="12723-134">IID</span><span class="sxs-lookup"><span data-stu-id="12723-134">IID</span></span><br/>                      | <span data-ttu-id="12723-135">DIID \_ IVMDVDDriveEvents è definito come c2a7d8e9-E76C-4EB8-94f7-71a5122d249b</span><span class="sxs-lookup"><span data-stu-id="12723-135">DIID\_IVMDVDDriveEvents is defined as c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="12723-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12723-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12723-137">**IVMDVDDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="12723-137">**IVMDVDDriveEvents**</span></span>](ivmdvddriveevents.md)
</dt> </dl>

 

