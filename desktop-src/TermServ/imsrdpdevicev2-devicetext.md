---
title: Proprietà DeviceText di IMsRdpDeviceV2
description: Contiene il testo del dispositivo.
ms.assetid: 2a67e8d4-2af3-4738-ade2-a79800aea4a1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DeviceText
- Servizi Desktop remoto proprietà DeviceText, interfaccia IMsRdpDeviceV2
- Interfaccia IMsRdpDeviceV2 Servizi Desktop remoto, proprietà DeviceText
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.DeviceText
- IMsRdpDeviceV2.get_DeviceText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fb35142a166db7e7c05fa5c0f00f7fdf2e1219c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225200"
---
# <a name="imsrdpdevicev2devicetext-property"></a><span data-ttu-id="cd002-106">IMsRdpDeviceV2::D Proprietà eviceText</span><span class="sxs-lookup"><span data-stu-id="cd002-106">IMsRdpDeviceV2::DeviceText property</span></span>

<span data-ttu-id="cd002-107">Contiene il testo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cd002-107">Contains the device text.</span></span> <span data-ttu-id="cd002-108">Si tratta del nome visualizzato da Windows per l'utente.</span><span class="sxs-lookup"><span data-stu-id="cd002-108">This is the name that Windows displays to the user.</span></span>

<span data-ttu-id="cd002-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="cd002-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd002-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd002-110">Syntax</span></span>


```C++
HRESULT get_DeviceText(
  [out, retval] BSTR *pDeviceText
);
```



## <a name="property-value"></a><span data-ttu-id="cd002-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="cd002-111">Property value</span></span>

<span data-ttu-id="cd002-112">Nome visualizzato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cd002-112">The display name for the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd002-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd002-113">Requirements</span></span>



| <span data-ttu-id="cd002-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd002-114">Requirement</span></span> | <span data-ttu-id="cd002-115">Valore</span><span class="sxs-lookup"><span data-stu-id="cd002-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd002-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd002-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cd002-117">Windows 7 con SP1</span><span class="sxs-lookup"><span data-stu-id="cd002-117">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="cd002-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd002-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cd002-119">Windows Server 2008 R2 con SP1</span><span class="sxs-lookup"><span data-stu-id="cd002-119">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="cd002-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="cd002-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="cd002-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd002-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="cd002-122">DLL</span><span class="sxs-lookup"><span data-stu-id="cd002-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd002-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd002-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="cd002-124">IID</span><span class="sxs-lookup"><span data-stu-id="cd002-124">IID</span></span><br/>                      | <span data-ttu-id="cd002-125">IID \_ IMsRdpDeviceV2 è definito come 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="cd002-125">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="cd002-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd002-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd002-127">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="cd002-127">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





