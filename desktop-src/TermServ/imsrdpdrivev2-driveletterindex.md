---
title: Proprietà DriveLetterIndex di IMsRdpDriveV2
description: Contiene l'indice della lettera per l'unità.
ms.assetid: 9091d1c4-b97e-4e4c-9563-5a0b881ec250
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DriveLetterIndex
- Servizi Desktop remoto proprietà DriveLetterIndex, interfaccia IMsRdpDriveV2
- Interfaccia IMsRdpDriveV2 Servizi Desktop remoto, proprietà DriveLetterIndex
topic_type:
- apiref
api_name:
- IMsRdpDriveV2.DriveLetterIndex
- IMsRdpDriveV2.get_DriveLetterIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39284a94950935e2d273483db871a9b08f7daf36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964974"
---
# <a name="imsrdpdrivev2driveletterindex-property"></a><span data-ttu-id="13041-106">IMsRdpDriveV2::D Proprietà riveLetterIndex</span><span class="sxs-lookup"><span data-stu-id="13041-106">IMsRdpDriveV2::DriveLetterIndex property</span></span>

<span data-ttu-id="13041-107">Contiene l'indice della lettera per l'unità.</span><span class="sxs-lookup"><span data-stu-id="13041-107">Contains the index of the letter for the drive.</span></span>

<span data-ttu-id="13041-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="13041-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="13041-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13041-109">Syntax</span></span>


```C++
HRESULT get_DriveLetterIndex(
  [out, retval] ULONG *pDriveLetterIndex
);
```



## <a name="property-value"></a><span data-ttu-id="13041-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="13041-110">Property value</span></span>

<span data-ttu-id="13041-111">Indice della lettera per l'unità.</span><span class="sxs-lookup"><span data-stu-id="13041-111">The index of the letter for the drive.</span></span> <span data-ttu-id="13041-112">0 = "A", 1 = "B" e così via.</span><span class="sxs-lookup"><span data-stu-id="13041-112">0 = "A", 1 = "B", and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="13041-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13041-113">Requirements</span></span>



| <span data-ttu-id="13041-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="13041-114">Requirement</span></span> | <span data-ttu-id="13041-115">Valore</span><span class="sxs-lookup"><span data-stu-id="13041-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13041-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13041-116">Minimum supported client</span></span><br/> | <span data-ttu-id="13041-117">Windows 7 con SP1</span><span class="sxs-lookup"><span data-stu-id="13041-117">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="13041-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13041-118">Minimum supported server</span></span><br/> | <span data-ttu-id="13041-119">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="13041-119">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="13041-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="13041-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="13041-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13041-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="13041-122">DLL</span><span class="sxs-lookup"><span data-stu-id="13041-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13041-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13041-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13041-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13041-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13041-125">**IMsRdpDriveV2**</span><span class="sxs-lookup"><span data-stu-id="13041-125">**IMsRdpDriveV2**</span></span>](imsrdpdrivev2.md)
</dt> </dl>

 

 





