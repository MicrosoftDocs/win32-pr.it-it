---
title: Proprietà TransportSettings4 di IMsRdpClient9
description: Recupera un oggetto che supporta l'interfaccia IMsRdpClientTransportSettings4.
ms.assetid: 808259b9-a1a4-4611-8602-b6877013c4f6
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà TransportSettings4
- Servizi Desktop remoto proprietà TransportSettings4, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà TransportSettings4
- Servizi Desktop remoto proprietà TransportSettings4, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà TransportSettings4
topic_type:
- apiref
api_name:
- IMsRdpClient9.TransportSettings4
- IMsRdpClient9.get_TransportSettings4
- IMsRdpClient10.TransportSettings4
- IMsRdpClient10.get_TransportSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765d2ad5a50e0608e4c11731742debbaede51737
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340382"
---
# <a name="imsrdpclient9transportsettings4-property"></a><span data-ttu-id="339b8-108">Proprietà IMsRdpClient9:: TransportSettings4</span><span class="sxs-lookup"><span data-stu-id="339b8-108">IMsRdpClient9::TransportSettings4 property</span></span>

<span data-ttu-id="339b8-109">Recupera un oggetto che supporta l'interfaccia [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="339b8-109">Retrieves an object that supports the [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) interface.</span></span>

<span data-ttu-id="339b8-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="339b8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="339b8-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="339b8-111">Syntax</span></span>


```C++
HRESULT get_TransportSettings4(
  [out, retval] IMsRdpClientTransportSettings4 **ppXportSet4
);
```



## <a name="property-value"></a><span data-ttu-id="339b8-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="339b8-112">Property value</span></span>

<span data-ttu-id="339b8-113">Restituisce un puntatore all'interfaccia [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="339b8-113">Returns an [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="339b8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="339b8-114">Requirements</span></span>



| <span data-ttu-id="339b8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="339b8-115">Requirement</span></span> | <span data-ttu-id="339b8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="339b8-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="339b8-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="339b8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="339b8-118">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="339b8-118">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="339b8-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="339b8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="339b8-120">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="339b8-120">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="339b8-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="339b8-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="339b8-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="339b8-122"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="339b8-123">DLL</span><span class="sxs-lookup"><span data-stu-id="339b8-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="339b8-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="339b8-124"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="339b8-125">IID</span><span class="sxs-lookup"><span data-stu-id="339b8-125">IID</span></span><br/>                      | <span data-ttu-id="339b8-126">CLSID \_ MsRdpClient9 è definito come 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="339b8-126">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="339b8-127">CLSID \_ MsRdpClient9NotSafeForScripting è definito come 8B918B82-7985-4c24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="339b8-127">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="339b8-128">IID \_ IMsRdpClient9 è definito come 28904001-04B6-436c-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="339b8-128">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="339b8-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="339b8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="339b8-130">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="339b8-130">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="339b8-131">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="339b8-131">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





