---
title: Enumerazione VMSerialPortType (VPCCOMInterfaces. h)
description: Specifica il tipo di porta seriale.
ms.assetid: 1385292b-ee3c-41f0-805a-df126f33cabb
keywords:
- VMSerialPortType enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMSerialPortType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9b6171053e980f1f5dbdc52ef28deed177edba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518370"
---
# <a name="vmserialporttype-enumeration"></a><span data-ttu-id="6ba19-104">Enumerazione VMSerialPortType</span><span class="sxs-lookup"><span data-stu-id="6ba19-104">VMSerialPortType enumeration</span></span>

<span data-ttu-id="6ba19-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6ba19-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6ba19-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6ba19-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6ba19-107">Specifica il tipo di porta seriale.</span><span class="sxs-lookup"><span data-stu-id="6ba19-107">Specifies the type of serial port.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ba19-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ba19-108">Syntax</span></span>


```C++
typedef enum  { 
  vmSerialPort_HostPort   = 0,
  vmSerialPort_TextFile   = 1,
  vmSerialPort_NamedPipe  = 2,
  vmSerialPort_Null       = 3
} VMSerialPortType;
```



## <a name="constants"></a><span data-ttu-id="6ba19-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="6ba19-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6ba19-110"><span id="vmSerialPort_HostPort"></span><span id="vmserialport_hostport"></span><span id="VMSERIALPORT_HOSTPORT"></span>**\_Portahost vmSerialPort**</span><span class="sxs-lookup"><span data-stu-id="6ba19-110"><span id="vmSerialPort_HostPort"></span><span id="vmserialport_hostport"></span><span id="VMSERIALPORT_HOSTPORT"></span>**vmSerialPort\_HostPort**</span></span>
</dt> <dd>

<span data-ttu-id="6ba19-111">Porta seriale host.</span><span class="sxs-lookup"><span data-stu-id="6ba19-111">A host serial port.</span></span>

</dd> <dt>

<span data-ttu-id="6ba19-112"><span id="vmSerialPort_TextFile"></span><span id="vmserialport_textfile"></span><span id="VMSERIALPORT_TEXTFILE"></span>**\_TextFile vmSerialPort**</span><span class="sxs-lookup"><span data-stu-id="6ba19-112"><span id="vmSerialPort_TextFile"></span><span id="vmserialport_textfile"></span><span id="VMSERIALPORT_TEXTFILE"></span>**vmSerialPort\_TextFile**</span></span>
</dt> <dd>

<span data-ttu-id="6ba19-113">Un file di testo host.</span><span class="sxs-lookup"><span data-stu-id="6ba19-113">A host text file.</span></span>

</dd> <dt>

<span data-ttu-id="6ba19-114"><span id="vmSerialPort_NamedPipe"></span><span id="vmserialport_namedpipe"></span><span id="VMSERIALPORT_NAMEDPIPE"></span>**\_NamedPipe vmSerialPort**</span><span class="sxs-lookup"><span data-stu-id="6ba19-114"><span id="vmSerialPort_NamedPipe"></span><span id="vmserialport_namedpipe"></span><span id="VMSERIALPORT_NAMEDPIPE"></span>**vmSerialPort\_NamedPipe**</span></span>
</dt> <dd>

<span data-ttu-id="6ba19-115">Named pipe.</span><span class="sxs-lookup"><span data-stu-id="6ba19-115">A named pipe.</span></span>

</dd> <dt>

<span data-ttu-id="6ba19-116"><span id="vmSerialPort_Null"></span><span id="vmserialport_null"></span><span id="VMSERIALPORT_NULL"></span>**vmSerialPort \_ null**</span><span class="sxs-lookup"><span data-stu-id="6ba19-116"><span id="vmSerialPort_Null"></span><span id="vmserialport_null"></span><span id="VMSERIALPORT_NULL"></span>**vmSerialPort\_Null**</span></span>
</dt> <dd>

<span data-ttu-id="6ba19-117">Una porta seriale **null** (Elimina tutti i bit inviati).</span><span class="sxs-lookup"><span data-stu-id="6ba19-117">A **NULL** serial port (discards all bits sent to it).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ba19-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ba19-118">Requirements</span></span>



| <span data-ttu-id="6ba19-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ba19-119">Requirement</span></span> | <span data-ttu-id="6ba19-120">Valore</span><span class="sxs-lookup"><span data-stu-id="6ba19-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ba19-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ba19-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6ba19-122">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6ba19-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6ba19-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ba19-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6ba19-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6ba19-124">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6ba19-125">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="6ba19-125">End of client support</span></span><br/>    | <span data-ttu-id="6ba19-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6ba19-126">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6ba19-127">Prodotto</span><span class="sxs-lookup"><span data-stu-id="6ba19-127">Product</span></span><br/>                  | <span data-ttu-id="6ba19-128">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6ba19-128">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6ba19-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6ba19-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ba19-130"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ba19-130"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ba19-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ba19-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ba19-132">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="6ba19-132">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

