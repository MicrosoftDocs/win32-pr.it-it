---
title: Proprietà Name di IMsRdpDrive
description: Recupera il nome dell'unità.
ms.assetid: 5aabb7df-fd46-48aa-ad1d-51da45495782
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà nome
- Nome Servizi Desktop remoto proprietà, interfaccia IMsRdpDrive
- Interfaccia IMsRdpDrive Servizi Desktop remoto, proprietà Name
topic_type:
- apiref
api_name:
- IMsRdpDrive.Name
- IMsRdpDrive.get_Name
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38eeb0f6112983f508bb43ba69d721aeb52c314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477740"
---
# <a name="imsrdpdrivename-property"></a><span data-ttu-id="01ecf-106">Proprietà IMsRdpDrive:: Name</span><span class="sxs-lookup"><span data-stu-id="01ecf-106">IMsRdpDrive::Name property</span></span>

<span data-ttu-id="01ecf-107">Recupera il nome dell'unità.</span><span class="sxs-lookup"><span data-stu-id="01ecf-107">Retrieves the name of the drive.</span></span>

<span data-ttu-id="01ecf-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="01ecf-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="01ecf-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01ecf-109">Syntax</span></span>


```C++
HRESULT get_Name(
  [out] BSTR *pName
);
```



## <a name="property-value"></a><span data-ttu-id="01ecf-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="01ecf-110">Property value</span></span>

<span data-ttu-id="01ecf-111">Nome dell'unità.</span><span class="sxs-lookup"><span data-stu-id="01ecf-111">The drive name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="01ecf-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="01ecf-112">Error codes</span></span>

<span data-ttu-id="01ecf-113">Se il metodo ha esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="01ecf-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="01ecf-114">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="01ecf-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="01ecf-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01ecf-115">Requirements</span></span>



| <span data-ttu-id="01ecf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="01ecf-116">Requirement</span></span> | <span data-ttu-id="01ecf-117">Valore</span><span class="sxs-lookup"><span data-stu-id="01ecf-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01ecf-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01ecf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="01ecf-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01ecf-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="01ecf-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01ecf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="01ecf-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01ecf-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="01ecf-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="01ecf-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="01ecf-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01ecf-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="01ecf-124">DLL</span><span class="sxs-lookup"><span data-stu-id="01ecf-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01ecf-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01ecf-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="01ecf-126">IID</span><span class="sxs-lookup"><span data-stu-id="01ecf-126">IID</span></span><br/>                      | <span data-ttu-id="01ecf-127">IID \_ IMsRdpDrive è definito come d28b5458-f694-47a8-8e61-40356a767e46</span><span class="sxs-lookup"><span data-stu-id="01ecf-127">IID\_IMsRdpDrive is defined as d28b5458-f694-47a8-8e61-40356a767e46</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="01ecf-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01ecf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01ecf-129">**IMsRdpDrive**</span><span class="sxs-lookup"><span data-stu-id="01ecf-129">**IMsRdpDrive**</span></span>](imsrdpdrive.md)
</dt> </dl>

 

 





