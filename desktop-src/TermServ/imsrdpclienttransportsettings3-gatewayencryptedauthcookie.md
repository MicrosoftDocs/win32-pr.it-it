---
title: Proprietà GatewayEncryptedAuthCookie di IMsRdpClientTransportSettings3
description: Cookie di autenticazione crittografato.
ms.assetid: c9ab6667-327c-44f8-a10e-b048ea91980c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayEncryptedAuthCookie
- Servizi Desktop remoto proprietà GatewayEncryptedAuthCookie, interfaccia IMsRdpClientTransportSettings3
- Interfaccia IMsRdpClientTransportSettings3 Servizi Desktop remoto, proprietà GatewayEncryptedAuthCookie
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.get_GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.put_GatewayEncryptedAuthCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3949d36f25f2029d7b134943b4e57d8a13db798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340683"
---
# <a name="imsrdpclienttransportsettings3gatewayencryptedauthcookie-property"></a><span data-ttu-id="aae5f-106">Proprietà IMsRdpClientTransportSettings3:: GatewayEncryptedAuthCookie</span><span class="sxs-lookup"><span data-stu-id="aae5f-106">IMsRdpClientTransportSettings3::GatewayEncryptedAuthCookie property</span></span>

<span data-ttu-id="aae5f-107">Cookie di autenticazione crittografato.</span><span class="sxs-lookup"><span data-stu-id="aae5f-107">The encrypted authentication cookie.</span></span> <span data-ttu-id="aae5f-108">La dimensione della proprietà è specificata dalla proprietà [**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md) .</span><span class="sxs-lookup"><span data-stu-id="aae5f-108">The size of the property is specified by the [**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md) property.</span></span>

<span data-ttu-id="aae5f-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="aae5f-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="aae5f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aae5f-110">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedAuthCookie(
  [in]          BSTR bstrEncryptedAuthCookie
);

HRESULT get_GatewayEncryptedAuthCookie(
  [out, retval] BSTR *pbstrEncryptedAuthCookie
);
```



## <a name="property-value"></a><span data-ttu-id="aae5f-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="aae5f-111">Property value</span></span>

<span data-ttu-id="aae5f-112">Nuovo cookie di autenticazione crittografato.</span><span class="sxs-lookup"><span data-stu-id="aae5f-112">The new encrypted authentication cookie.</span></span>

## <a name="requirements"></a><span data-ttu-id="aae5f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aae5f-113">Requirements</span></span>



| <span data-ttu-id="aae5f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="aae5f-114">Requirement</span></span> | <span data-ttu-id="aae5f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="aae5f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aae5f-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aae5f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aae5f-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="aae5f-117">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="aae5f-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aae5f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aae5f-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aae5f-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="aae5f-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="aae5f-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="aae5f-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aae5f-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="aae5f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="aae5f-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aae5f-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aae5f-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aae5f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aae5f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aae5f-125">**GatewayEncryptedAuthCookieSize**</span><span class="sxs-lookup"><span data-stu-id="aae5f-125">**GatewayEncryptedAuthCookieSize**</span></span>](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)
</dt> <dt>

[<span data-ttu-id="aae5f-126">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="aae5f-126">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





