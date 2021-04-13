---
title: Proprietà GatewaySupportUrl di IMsRdpClientTransportSettings2
description: Specifica o recupera l'indirizzo Web del sito che fornisce supporto tecnico per il server Gateway Desktop remoto di Desktop remoto.
ms.assetid: e9c0f5ec-1b2f-4e09-8169-4316fd394443
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewaySupportUrl
- Servizi Desktop remoto proprietà GatewaySupportUrl, interfaccia IMsRdpClientTransportSettings2
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto, proprietà GatewaySupportUrl
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewaySupportUrl
- IMsRdpClientTransportSettings2.get_GatewaySupportUrl
- IMsRdpClientTransportSettings2.put_GatewaySupportUrl
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4212dd03d5fb217753e14c2869973bda87476367
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400376"
---
# <a name="imsrdpclienttransportsettings2gatewaysupporturl-property"></a><span data-ttu-id="3e2b2-106">Proprietà IMsRdpClientTransportSettings2:: GatewaySupportUrl</span><span class="sxs-lookup"><span data-stu-id="3e2b2-106">IMsRdpClientTransportSettings2::GatewaySupportUrl property</span></span>

<span data-ttu-id="3e2b2-107">Specifica o recupera l'indirizzo Web del sito che fornisce supporto tecnico per il server Gateway Desktop remoto di Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="3e2b2-107">Specifies or retrieves the web address of the site that provides technical support for this Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="3e2b2-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3e2b2-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e2b2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e2b2-109">Syntax</span></span>


```C++
HRESULT put_GatewaySupportUrl(
  [in]  BSTR bstrProxySupportUrl
);

HRESULT get_GatewaySupportUrl(
  [out] BSTR *pbstrProxySupportUrl
);
```



## <a name="property-value"></a><span data-ttu-id="3e2b2-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3e2b2-110">Property value</span></span>

<span data-ttu-id="3e2b2-111">Specifica o recupera l'indirizzo Web del sito che fornisce supporto tecnico per il server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="3e2b2-111">Specifies or retrieves the web address of the site that provides technical support for this RD Gateway server.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e2b2-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e2b2-112">Requirements</span></span>



| <span data-ttu-id="3e2b2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e2b2-113">Requirement</span></span> | <span data-ttu-id="3e2b2-114">Valore</span><span class="sxs-lookup"><span data-stu-id="3e2b2-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e2b2-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e2b2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3e2b2-116">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="3e2b2-116">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="3e2b2-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e2b2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3e2b2-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e2b2-118">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="3e2b2-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="3e2b2-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="3e2b2-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e2b2-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="3e2b2-121">DLL</span><span class="sxs-lookup"><span data-stu-id="3e2b2-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e2b2-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e2b2-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="3e2b2-123">IID</span><span class="sxs-lookup"><span data-stu-id="3e2b2-123">IID</span></span><br/>                      | <span data-ttu-id="3e2b2-124">IID \_ IMsRdpClientTransportSettings2 è definito come 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="3e2b2-124">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3e2b2-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e2b2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e2b2-126">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="3e2b2-126">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="3e2b2-127">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="3e2b2-127">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





