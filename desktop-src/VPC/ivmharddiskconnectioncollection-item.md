---
title: Proprietà Item di IVMHardDiskConnectionCollection (VPCCOMInterfaces. h)
description: Recupera l'oggetto connessione al disco rigido che corrisponde all'indice specificato.
ms.assetid: 24e158fb-b026-4619-9d0d-a59cd782894f
keywords:
- Proprietà elemento Virtual PC
- Proprietà elemento Virtual PC, interfaccia IVMHardDiskConnectionCollection
- Interfaccia IVMHardDiskConnectionCollection Virtual PC, proprietà Item
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Item
- IVMHardDiskConnectionCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5558e70cfcf18f67c14e52160737b851fa9ea2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300934"
---
# <a name="ivmharddiskconnectioncollectionitem-property"></a><span data-ttu-id="895f6-106">Proprietà IVMHardDiskConnectionCollection:: Item</span><span class="sxs-lookup"><span data-stu-id="895f6-106">IVMHardDiskConnectionCollection::Item property</span></span>

<span data-ttu-id="895f6-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="895f6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="895f6-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="895f6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="895f6-109">Recupera l'oggetto connessione al disco rigido che corrisponde all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="895f6-109">Retrieves the hard disk connection object that corresponds to the specified index.</span></span>

<span data-ttu-id="895f6-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="895f6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="895f6-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="895f6-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long                  index,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="property-value"></a><span data-ttu-id="895f6-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="895f6-112">Property value</span></span>

<span data-ttu-id="895f6-113">Oggetto [**IVMHardDiskConnection**](ivmharddiskconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="895f6-113">The [**IVMHardDiskConnection**](ivmharddiskconnection.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="895f6-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="895f6-114">Error codes</span></span>



| <span data-ttu-id="895f6-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="895f6-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="895f6-116">Significato</span><span class="sxs-lookup"><span data-stu-id="895f6-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="895f6-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="895f6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="895f6-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="895f6-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="895f6-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="895f6-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="895f6-120">Il parametro *hardDiskConnection* è **null**.</span><span class="sxs-lookup"><span data-stu-id="895f6-120">The *hardDiskConnection* parameter is **NULL**.</span></span> <br/>                                    |
| <dl> <span data-ttu-id="895f6-121"><dt>Disp \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="895f6-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="895f6-122">L'indice dell'elemento richiesto non corrisponde a un elemento in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="895f6-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="895f6-123"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="895f6-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="895f6-124">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="895f6-124">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="895f6-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="895f6-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="895f6-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="895f6-126">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="895f6-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="895f6-127">Requirements</span></span>



| <span data-ttu-id="895f6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="895f6-128">Requirement</span></span> | <span data-ttu-id="895f6-129">Valore</span><span class="sxs-lookup"><span data-stu-id="895f6-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="895f6-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="895f6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="895f6-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="895f6-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="895f6-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="895f6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="895f6-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="895f6-133">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="895f6-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="895f6-134">End of client support</span></span><br/>    | <span data-ttu-id="895f6-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="895f6-135">Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="895f6-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="895f6-136">Product</span></span><br/>                  | <span data-ttu-id="895f6-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="895f6-137">Windows Virtual PC</span></span><br/>                                                                      |
| <span data-ttu-id="895f6-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="895f6-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="895f6-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="895f6-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>      |
| <span data-ttu-id="895f6-140">IID</span><span class="sxs-lookup"><span data-stu-id="895f6-140">IID</span></span><br/>                      | <span data-ttu-id="895f6-141">IID \_ IVMHardDiskconnectionCollection è definito come b9f2caf4-0aeb-4085-B105-ceddb90dbf62</span><span class="sxs-lookup"><span data-stu-id="895f6-141">IID\_IVMHardDiskconnectionCollection is defined as b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="895f6-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="895f6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="895f6-143">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="895f6-143">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> <dt>

[<span data-ttu-id="895f6-144">**IVMHardDiskConnectionCollection**</span><span class="sxs-lookup"><span data-stu-id="895f6-144">**IVMHardDiskConnectionCollection**</span></span>](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

