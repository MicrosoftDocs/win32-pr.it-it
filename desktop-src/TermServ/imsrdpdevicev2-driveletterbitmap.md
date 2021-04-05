---
title: Proprietà DriveLetterBitmap di IMsRdpDeviceV2
description: Contiene un bit che rappresenta una mappa delle lettere di unità contenute all'interno del dispositivo.
ms.assetid: 13b7c9b9-a97f-4474-b5ad-833abff384f5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DriveLetterBitmap
- Servizi Desktop remoto proprietà DriveLetterBitmap, interfaccia IMsRdpDeviceV2
- Interfaccia IMsRdpDeviceV2 Servizi Desktop remoto, proprietà DriveLetterBitmap
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.DriveLetterBitmap
- IMsRdpDeviceV2.get_DriveLetterBitmap
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d13189415630539ac47d7a0e0a094b7b3212e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739994"
---
# <a name="imsrdpdevicev2driveletterbitmap-property"></a><span data-ttu-id="48597-106">IMsRdpDeviceV2::D Proprietà riveLetterBitmap</span><span class="sxs-lookup"><span data-stu-id="48597-106">IMsRdpDeviceV2::DriveLetterBitmap property</span></span>

<span data-ttu-id="48597-107">Contiene un bit che rappresenta una mappa delle lettere di unità contenute all'interno del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48597-107">Contains a bitfield that represents a map of drive letters contained within the device.</span></span>

<span data-ttu-id="48597-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="48597-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="48597-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48597-109">Syntax</span></span>


```C++
HRESULT get_DriveLetterBitmap(
  [out, retval] ULONG *pDriveLetterBitmap
);
```



## <a name="property-value"></a><span data-ttu-id="48597-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="48597-110">Property value</span></span>

<span data-ttu-id="48597-111">Mappa delle lettere di unità contenute all'interno del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48597-111">A map of drive letters contained within the device.</span></span> <span data-ttu-id="48597-112">Ogni bit nel valore rappresenta una lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="48597-112">Each bit in the value represents a drive letter.</span></span> <span data-ttu-id="48597-113">Il bit meno significativo rappresenta la lettera di unità "A", il bit successivo rappresenta la lettera di unità "B" e così via.</span><span class="sxs-lookup"><span data-stu-id="48597-113">The least significant bit represents drive letter "A", the next bit represents drive letter "B", and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="48597-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48597-114">Requirements</span></span>



| <span data-ttu-id="48597-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="48597-115">Requirement</span></span> | <span data-ttu-id="48597-116">Valore</span><span class="sxs-lookup"><span data-stu-id="48597-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48597-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48597-117">Minimum supported client</span></span><br/> | <span data-ttu-id="48597-118">Windows 7 con SP1</span><span class="sxs-lookup"><span data-stu-id="48597-118">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="48597-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48597-119">Minimum supported server</span></span><br/> | <span data-ttu-id="48597-120">Windows Server 2008 R2 con SP1</span><span class="sxs-lookup"><span data-stu-id="48597-120">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="48597-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="48597-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="48597-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48597-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="48597-123">DLL</span><span class="sxs-lookup"><span data-stu-id="48597-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48597-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48597-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="48597-125">IID</span><span class="sxs-lookup"><span data-stu-id="48597-125">IID</span></span><br/>                      | <span data-ttu-id="48597-126">IID \_ IMsRdpDeviceV2 è definito come 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="48597-126">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="48597-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48597-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48597-128">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="48597-128">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





