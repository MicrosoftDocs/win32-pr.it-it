---
title: Proprietà Item di IVMSerialPortCollection (VPCCOMInterfaces. h)
description: Recupera l'oggetto porta seriale che corrisponde all'indice specificato.
ms.assetid: 24ce1404-d7aa-4125-b1f9-9c54418ea205
keywords:
- Proprietà elemento Virtual PC
- Proprietà elemento Virtual PC, interfaccia IVMSerialPortCollection
- Interfaccia IVMSerialPortCollection Virtual PC, proprietà Item
topic_type:
- apiref
api_name:
- IVMSerialPortCollection.Item
- IVMSerialPortCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be44cc92507954848c369273ae27de49df8d0ad8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301779"
---
# <a name="ivmserialportcollectionitem-property"></a><span data-ttu-id="d98a6-106">Proprietà IVMSerialPortCollection:: Item</span><span class="sxs-lookup"><span data-stu-id="d98a6-106">IVMSerialPortCollection::Item property</span></span>

<span data-ttu-id="d98a6-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d98a6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d98a6-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d98a6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d98a6-109">Recupera l'oggetto porta seriale che corrisponde all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="d98a6-109">Retrieves the serial port object that corresponds to the specified index.</span></span>

<span data-ttu-id="d98a6-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d98a6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d98a6-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d98a6-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long          index,
  [out, retval] IVMSerialPort **serialPort
);
```



## <a name="property-value"></a><span data-ttu-id="d98a6-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d98a6-112">Property value</span></span>

<span data-ttu-id="d98a6-113">Oggetto [**IVMSerialPort**](ivmserialport.md) .</span><span class="sxs-lookup"><span data-stu-id="d98a6-113">The [**IVMSerialPort**](ivmserialport.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d98a6-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="d98a6-114">Error codes</span></span>



| <span data-ttu-id="d98a6-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="d98a6-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d98a6-116">Significato</span><span class="sxs-lookup"><span data-stu-id="d98a6-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d98a6-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d98a6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d98a6-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d98a6-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="d98a6-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d98a6-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d98a6-120">Il parametro *SerialPort* è null.</span><span class="sxs-lookup"><span data-stu-id="d98a6-120">The *serialPort* parameter is NULL.</span></span> <br/>                                                |
| <dl> <span data-ttu-id="d98a6-121"><dt>Disp \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="d98a6-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="d98a6-122">L'indice dell'elemento richiesto non corrisponde a un elemento in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="d98a6-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="d98a6-123"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d98a6-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="d98a6-124">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="d98a6-124">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="d98a6-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d98a6-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d98a6-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="d98a6-126">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="d98a6-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d98a6-127">Requirements</span></span>



| <span data-ttu-id="d98a6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d98a6-128">Requirement</span></span> | <span data-ttu-id="d98a6-129">Valore</span><span class="sxs-lookup"><span data-stu-id="d98a6-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d98a6-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d98a6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d98a6-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d98a6-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d98a6-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d98a6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d98a6-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d98a6-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d98a6-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d98a6-134">End of client support</span></span><br/>    | <span data-ttu-id="d98a6-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d98a6-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d98a6-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="d98a6-136">Product</span></span><br/>                  | <span data-ttu-id="d98a6-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d98a6-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d98a6-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d98a6-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d98a6-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d98a6-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d98a6-140">IID</span><span class="sxs-lookup"><span data-stu-id="d98a6-140">IID</span></span><br/>                      | <span data-ttu-id="d98a6-141">IID \_ IVMSerialPortCollection è definito come dd3c6175-1F04-4341-9f85-104074880289</span><span class="sxs-lookup"><span data-stu-id="d98a6-141">IID\_IVMSerialPortCollection is defined as dd3c6175-1f04-4341-9f85-104074880289</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="d98a6-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d98a6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d98a6-143">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="d98a6-143">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> <dt>

[<span data-ttu-id="d98a6-144">**IVMSerialPortCollection**</span><span class="sxs-lookup"><span data-stu-id="d98a6-144">**IVMSerialPortCollection**</span></span>](ivmserialportcollection.md)
</dt> </dl>

 

