---
title: Proprietà IMsRdpDevice FriendlyName
description: Recupera il nome visualizzato per il dispositivo.
ms.assetid: ed27eacd-1d39-484c-8217-62ed608db050
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto della proprietà FriendlyName
- Servizi Desktop remoto proprietà FriendlyName, interfaccia IMsRdpDevice
- Interfaccia IMsRdpDevice Servizi Desktop remoto, proprietà FriendlyName
topic_type:
- apiref
api_name:
- IMsRdpDevice.FriendlyName
- IMsRdpDevice.get_FriendlyName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bf7963cf49945b886d72a622b517438e24d148f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740543"
---
# <a name="imsrdpdevicefriendlyname-property"></a><span data-ttu-id="393a2-106">Proprietà IMsRdpDevice:: FriendlyName</span><span class="sxs-lookup"><span data-stu-id="393a2-106">IMsRdpDevice::FriendlyName property</span></span>

<span data-ttu-id="393a2-107">Recupera il nome visualizzato per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="393a2-107">Retrieves the display name for the device.</span></span>

<span data-ttu-id="393a2-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="393a2-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="393a2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="393a2-109">Syntax</span></span>


```C++
HRESULT get_FriendlyName(
  [out] BSTR *pFriendlyName
);
```



## <a name="property-value"></a><span data-ttu-id="393a2-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="393a2-110">Property value</span></span>

<span data-ttu-id="393a2-111">Nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="393a2-111">The display name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="393a2-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="393a2-112">Error codes</span></span>

<span data-ttu-id="393a2-113">Se il metodo ha esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="393a2-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="393a2-114">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="393a2-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="393a2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="393a2-115">Requirements</span></span>



| <span data-ttu-id="393a2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="393a2-116">Requirement</span></span> | <span data-ttu-id="393a2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="393a2-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="393a2-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="393a2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="393a2-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="393a2-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="393a2-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="393a2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="393a2-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="393a2-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="393a2-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="393a2-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="393a2-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="393a2-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="393a2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="393a2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="393a2-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="393a2-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="393a2-126">IID</span><span class="sxs-lookup"><span data-stu-id="393a2-126">IID</span></span><br/>                      | <span data-ttu-id="393a2-127">IID \_ IMsRdpDevice è definito come 60c3b9c8-9E92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="393a2-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="393a2-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="393a2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="393a2-129">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="393a2-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





