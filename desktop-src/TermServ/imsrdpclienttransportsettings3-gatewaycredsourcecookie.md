---
title: Proprietà GatewayCredSourceCookie di IMsRdpClientTransportSettings3
description: Specifica se l'origine delle credenziali è basata su cookie.
ms.assetid: 039459a3-7a83-444c-a0b4-46ef0dc5ddd0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayCredSourceCookie
- Servizi Desktop remoto proprietà GatewayCredSourceCookie, interfaccia IMsRdpClientTransportSettings3
- Interfaccia IMsRdpClientTransportSettings3 Servizi Desktop remoto, proprietà GatewayCredSourceCookie
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.get_GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.put_GatewayCredSourceCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9547df10ce9f528a4b52c526c970a82d0bd098c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302576"
---
# <a name="imsrdpclienttransportsettings3gatewaycredsourcecookie-property"></a><span data-ttu-id="46839-106">Proprietà IMsRdpClientTransportSettings3:: GatewayCredSourceCookie</span><span class="sxs-lookup"><span data-stu-id="46839-106">IMsRdpClientTransportSettings3::GatewayCredSourceCookie property</span></span>

<span data-ttu-id="46839-107">Specifica se l'origine delle credenziali è basata su cookie.</span><span class="sxs-lookup"><span data-stu-id="46839-107">Specifies if the credential source is cookie based.</span></span> <span data-ttu-id="46839-108">Contiene uno se l'origine della credenziale è basata su cookie o zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="46839-108">Contains one if the credential source is cookie-based or zero otherwise.</span></span>

<span data-ttu-id="46839-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="46839-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="46839-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46839-110">Syntax</span></span>


```C++
HRESULT put_GatewayCredSourceCookie(
  [in]          ULONG ulProxyCredSourceCookie
);

HRESULT get_GatewayCredSourceCookie(
  [out, retval] ULONG *pulProxyCredSourceCookie
);
```



## <a name="property-value"></a><span data-ttu-id="46839-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="46839-111">Property value</span></span>

<span data-ttu-id="46839-112">Valore **ULONG** che specifica se l'origine delle credenziali è basata su cookie.</span><span class="sxs-lookup"><span data-stu-id="46839-112">A **ULONG** value that specifies if the credential source is cookie based.</span></span>

## <a name="requirements"></a><span data-ttu-id="46839-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46839-113">Requirements</span></span>



| <span data-ttu-id="46839-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="46839-114">Requirement</span></span> | <span data-ttu-id="46839-115">Valore</span><span class="sxs-lookup"><span data-stu-id="46839-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46839-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46839-116">Minimum supported client</span></span><br/> | <span data-ttu-id="46839-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="46839-117">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="46839-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46839-118">Minimum supported server</span></span><br/> | <span data-ttu-id="46839-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46839-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="46839-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="46839-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="46839-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46839-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="46839-122">DLL</span><span class="sxs-lookup"><span data-stu-id="46839-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46839-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46839-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46839-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46839-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46839-125">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="46839-125">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





