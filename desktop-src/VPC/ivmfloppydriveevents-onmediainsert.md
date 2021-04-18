---
title: Metodo IVMFloppyDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
description: Riceve la notifica che i supporti sono stati inseriti nell'unità. | Metodo IVMFloppyDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
ms.assetid: 922fca14-8ef6-4d3d-b1b6-72d2ea83e8ef
keywords:
- Metodo OnMediaInsert Virtual PC
- Metodo OnMediaInsert Virtual PC, interfaccia IVMFloppyDriveEvents
- Interfaccia IVMFloppyDriveEvents Virtual PC, metodo OnMediaInsert
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d607a2f63836ca1cb151e602b2d3b2021f4e3913
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321984"
---
# <a name="ivmfloppydriveeventsonmediainsert-method"></a><span data-ttu-id="53e28-107">Metodo IVMFloppyDriveEvents:: OnMediaInsert</span><span class="sxs-lookup"><span data-stu-id="53e28-107">IVMFloppyDriveEvents::OnMediaInsert method</span></span>

<span data-ttu-id="53e28-108">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="53e28-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="53e28-109">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="53e28-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="53e28-110">Riceve la notifica che i supporti sono stati inseriti nell'unità.</span><span class="sxs-lookup"><span data-stu-id="53e28-110">Receives notification that media has been inserted into the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="53e28-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53e28-111">Syntax</span></span>


```C++
HRESULT OnMediaInsert(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a><span data-ttu-id="53e28-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="53e28-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53e28-113">*mediaPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53e28-113">*mediaPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53e28-114">Lettera o percorso dell'unità host nell'immagine floppy.</span><span class="sxs-lookup"><span data-stu-id="53e28-114">The host drive letter, or path, to floppy image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53e28-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53e28-115">Return value</span></span>

<span data-ttu-id="53e28-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="53e28-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="53e28-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="53e28-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="53e28-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="53e28-118">Remarks</span></span>

<span data-ttu-id="53e28-119">Questo metodo viene chiamato quando viene inserito un supporto (un'immagine del disco floppy o un disco floppy in un'unità host).</span><span class="sxs-lookup"><span data-stu-id="53e28-119">This method is called when media (a floppy disk image or a floppy disk in a host drive) is inserted.</span></span> <span data-ttu-id="53e28-120">Il programma client deve implementare questo metodo di interfaccia per ricevere una notifica dell' \_ evento vmFloppyDriveEvent OnMediaInsert originato da [**IVMFloppyDrive**](ivmfloppydrive.md).</span><span class="sxs-lookup"><span data-stu-id="53e28-120">The client program must implement this interface method to receive notification of the vmFloppyDriveEvent\_OnMediaInsert event originating from [**IVMFloppyDrive**](ivmfloppydrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="53e28-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53e28-121">Requirements</span></span>



| <span data-ttu-id="53e28-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="53e28-122">Requirement</span></span> | <span data-ttu-id="53e28-123">Valore</span><span class="sxs-lookup"><span data-stu-id="53e28-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="53e28-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53e28-124">Minimum supported client</span></span><br/> | <span data-ttu-id="53e28-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="53e28-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="53e28-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53e28-126">Minimum supported server</span></span><br/> | <span data-ttu-id="53e28-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="53e28-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="53e28-128">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="53e28-128">End of client support</span></span><br/>    | <span data-ttu-id="53e28-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="53e28-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="53e28-130">Prodotto</span><span class="sxs-lookup"><span data-stu-id="53e28-130">Product</span></span><br/>                  | <span data-ttu-id="53e28-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="53e28-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="53e28-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53e28-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="53e28-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="53e28-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="53e28-134">IID</span><span class="sxs-lookup"><span data-stu-id="53e28-134">IID</span></span><br/>                      | <span data-ttu-id="53e28-135">DIID \_ IVMFloppyDriveEvents è definito come a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span><span class="sxs-lookup"><span data-stu-id="53e28-135">DIID\_IVMFloppyDriveEvents is defined as a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="53e28-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53e28-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53e28-137">**IVMFloppyDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="53e28-137">**IVMFloppyDriveEvents**</span></span>](ivmfloppydriveevents.md)
</dt> </dl>

 

