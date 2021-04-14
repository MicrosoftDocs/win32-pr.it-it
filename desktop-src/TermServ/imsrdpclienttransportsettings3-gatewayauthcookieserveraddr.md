---
title: Proprietà GatewayAuthCookieServerAddr di IMsRdpClientTransportSettings3
description: Indirizzo del server per l'autenticazione basata su cookie.
ms.assetid: e00480cd-2133-42ff-8447-6c4234b56bf9
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayAuthCookieServerAddr
- Servizi Desktop remoto proprietà GatewayAuthCookieServerAddr, interfaccia IMsRdpClientTransportSettings3
- Interfaccia IMsRdpClientTransportSettings3 Servizi Desktop remoto, proprietà GatewayAuthCookieServerAddr
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.get_GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.put_GatewayAuthCookieServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc238129d0bb9f698e90fc5e1de85e7257a4d16e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479042"
---
# <a name="imsrdpclienttransportsettings3gatewayauthcookieserveraddr-property"></a><span data-ttu-id="4c262-106">Proprietà IMsRdpClientTransportSettings3:: GatewayAuthCookieServerAddr</span><span class="sxs-lookup"><span data-stu-id="4c262-106">IMsRdpClientTransportSettings3::GatewayAuthCookieServerAddr property</span></span>

<span data-ttu-id="4c262-107">Indirizzo del server per l'autenticazione basata su cookie.</span><span class="sxs-lookup"><span data-stu-id="4c262-107">The server address for cookie-based authentication.</span></span>

<span data-ttu-id="4c262-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4c262-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c262-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c262-109">Syntax</span></span>


```C++
HRESULT put_GatewayAuthCookieServerAddr(
  [in]          BSTR bstrProxyAuthCookieServerAddr
);

HRESULT get_GatewayAuthCookieServerAddr(
  [out, retval] BSTR *pbstrProxyAuthCookieServerAddr
);
```



## <a name="property-value"></a><span data-ttu-id="4c262-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4c262-110">Property value</span></span>

<span data-ttu-id="4c262-111">Nuovo indirizzo del server per l'autenticazione basata su cookie.</span><span class="sxs-lookup"><span data-stu-id="4c262-111">The new server address for cookie-based authentication.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c262-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c262-112">Requirements</span></span>



| <span data-ttu-id="4c262-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c262-113">Requirement</span></span> | <span data-ttu-id="4c262-114">Valore</span><span class="sxs-lookup"><span data-stu-id="4c262-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c262-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c262-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4c262-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4c262-116">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="4c262-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c262-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4c262-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c262-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4c262-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="4c262-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="4c262-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c262-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4c262-121">DLL</span><span class="sxs-lookup"><span data-stu-id="4c262-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c262-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c262-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c262-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c262-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c262-124">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="4c262-124">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





