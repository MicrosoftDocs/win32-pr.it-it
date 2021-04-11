---
title: Proprietà GatewayAuthLoginPage di IMsRdpClientTransportSettings3
description: Indirizzo della pagina Web di accesso da usare per autenticare un utente.
ms.assetid: d7a5e0d8-353e-416d-a9e0-11ef5072f9ff
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayAuthLoginPage
- Servizi Desktop remoto proprietà GatewayAuthLoginPage, interfaccia IMsRdpClientTransportSettings3
- Interfaccia IMsRdpClientTransportSettings3 Servizi Desktop remoto, proprietà GatewayAuthLoginPage
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthLoginPage
- IMsRdpClientTransportSettings3.get_GatewayAuthLoginPage
- IMsRdpClientTransportSettings3.put_GatewayAuthLoginPage
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5be535dea0a89f1cf6e7c238029e53f38f58b0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121378"
---
# <a name="imsrdpclienttransportsettings3gatewayauthloginpage-property"></a><span data-ttu-id="c68b0-106">Proprietà IMsRdpClientTransportSettings3:: GatewayAuthLoginPage</span><span class="sxs-lookup"><span data-stu-id="c68b0-106">IMsRdpClientTransportSettings3::GatewayAuthLoginPage property</span></span>

<span data-ttu-id="c68b0-107">Indirizzo della pagina Web di accesso da usare per autenticare un utente.</span><span class="sxs-lookup"><span data-stu-id="c68b0-107">The address of the login webpage to use to authenticate a user.</span></span>

<span data-ttu-id="c68b0-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c68b0-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c68b0-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c68b0-109">Syntax</span></span>


```C++
HRESULT put_GatewayAuthLoginPage(
  [in]          BSTR bstrProxyAuthLoginPage
);

HRESULT get_GatewayAuthLoginPage(
  [out, retval] BSTR *pbstrProxyAuthLoginPage
);
```



## <a name="property-value"></a><span data-ttu-id="c68b0-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c68b0-110">Property value</span></span>

<span data-ttu-id="c68b0-111">Nuovo indirizzo della pagina Web di accesso.</span><span class="sxs-lookup"><span data-stu-id="c68b0-111">The new login webpage address.</span></span>

## <a name="requirements"></a><span data-ttu-id="c68b0-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c68b0-112">Requirements</span></span>



| <span data-ttu-id="c68b0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c68b0-113">Requirement</span></span> | <span data-ttu-id="c68b0-114">Valore</span><span class="sxs-lookup"><span data-stu-id="c68b0-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c68b0-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c68b0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c68b0-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c68b0-116">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="c68b0-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c68b0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c68b0-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c68b0-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c68b0-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c68b0-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="c68b0-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c68b0-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c68b0-121">DLL</span><span class="sxs-lookup"><span data-stu-id="c68b0-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c68b0-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c68b0-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c68b0-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c68b0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c68b0-124">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="c68b0-124">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





