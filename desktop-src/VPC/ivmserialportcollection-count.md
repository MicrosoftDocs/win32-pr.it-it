---
title: Proprietà Count IVMSerialPortCollection (VPCCOMInterfaces. h)
description: Recupera il numero di porte seriali nell'insieme.
ms.assetid: 94ff6c9d-17bc-4aa5-a486-d4428c829d02
keywords:
- Conteggio proprietà PC virtuale
- Proprietà Count Virtual PC, interfaccia IVMSerialPortCollection
- Interfaccia IVMSerialPortCollection Virtual PC, proprietà Count
topic_type:
- apiref
api_name:
- IVMSerialPortCollection.Count
- IVMSerialPortCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbf0503f00fd1df7d27a8eeafedd3efe42619b98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874062"
---
# <a name="ivmserialportcollectioncount-property"></a><span data-ttu-id="37b26-106">Proprietà IVMSerialPortCollection:: count</span><span class="sxs-lookup"><span data-stu-id="37b26-106">IVMSerialPortCollection::Count property</span></span>

<span data-ttu-id="37b26-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="37b26-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="37b26-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="37b26-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="37b26-109">Recupera il numero di porte seriali nell'insieme.</span><span class="sxs-lookup"><span data-stu-id="37b26-109">Retrieves the number of serial ports in this collection.</span></span>

<span data-ttu-id="37b26-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="37b26-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="37b26-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37b26-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="37b26-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="37b26-112">Property value</span></span>

<span data-ttu-id="37b26-113">Numero di porte seriali.</span><span class="sxs-lookup"><span data-stu-id="37b26-113">The number of serial ports.</span></span>

## <a name="error-codes"></a><span data-ttu-id="37b26-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="37b26-114">Error codes</span></span>



| <span data-ttu-id="37b26-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="37b26-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="37b26-116">Significato</span><span class="sxs-lookup"><span data-stu-id="37b26-116">Meaning</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="37b26-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="37b26-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="37b26-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="37b26-118">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="37b26-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="37b26-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="37b26-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="37b26-120">The parameter is **NULL**.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="37b26-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37b26-121">Requirements</span></span>



| <span data-ttu-id="37b26-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="37b26-122">Requirement</span></span> | <span data-ttu-id="37b26-123">Valore</span><span class="sxs-lookup"><span data-stu-id="37b26-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="37b26-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37b26-124">Minimum supported client</span></span><br/> | <span data-ttu-id="37b26-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="37b26-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="37b26-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37b26-126">Minimum supported server</span></span><br/> | <span data-ttu-id="37b26-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="37b26-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="37b26-128">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="37b26-128">End of client support</span></span><br/>    | <span data-ttu-id="37b26-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="37b26-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="37b26-130">Prodotto</span><span class="sxs-lookup"><span data-stu-id="37b26-130">Product</span></span><br/>                  | <span data-ttu-id="37b26-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="37b26-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="37b26-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="37b26-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="37b26-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="37b26-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="37b26-134">IID</span><span class="sxs-lookup"><span data-stu-id="37b26-134">IID</span></span><br/>                      | <span data-ttu-id="37b26-135">IID \_ IVMSerialPortCollection è definito come dd3c6175-1F04-4341-9f85-104074880289</span><span class="sxs-lookup"><span data-stu-id="37b26-135">IID\_IVMSerialPortCollection is defined as dd3c6175-1f04-4341-9f85-104074880289</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="37b26-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37b26-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37b26-137">**IVMSerialPortCollection**</span><span class="sxs-lookup"><span data-stu-id="37b26-137">**IVMSerialPortCollection**</span></span>](ivmserialportcollection.md)
</dt> </dl>

 

