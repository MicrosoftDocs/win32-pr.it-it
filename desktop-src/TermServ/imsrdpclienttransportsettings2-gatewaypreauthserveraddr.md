---
title: Proprietà GatewayPreAuthServerAddr di IMsRdpClientTransportSettings2
description: Specifica o recupera l'indirizzo Web del server di pre-autenticazione, che viene utilizzato per la funzionalità di password monouso (OTP) di Desktop remoto Gateway.
ms.assetid: 14edad82-ab19-46fe-b878-d34298763c56
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayPreAuthServerAddr
- Servizi Desktop remoto proprietà GatewayPreAuthServerAddr, interfaccia IMsRdpClientTransportSettings2
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto, proprietà GatewayPreAuthServerAddr
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.get_GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.put_GatewayPreAuthServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d6fe2f397b0d445a6300d68a89b210debd449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400377"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthserveraddr-property"></a><span data-ttu-id="5701f-106">Proprietà IMsRdpClientTransportSettings2:: GatewayPreAuthServerAddr</span><span class="sxs-lookup"><span data-stu-id="5701f-106">IMsRdpClientTransportSettings2::GatewayPreAuthServerAddr property</span></span>

<span data-ttu-id="5701f-107">Specifica o recupera l'indirizzo Web del server di pre-autenticazione, che viene utilizzato per la funzionalità di password monouso (OTP) di Desktop remoto Gateway.</span><span class="sxs-lookup"><span data-stu-id="5701f-107">Specifies or retrieves the web address of the pre-authentication server, which is used for the Remote Desktop Gateway (RD Gateway) one-time password (OTP) feature.</span></span>

<span data-ttu-id="5701f-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5701f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5701f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5701f-109">Syntax</span></span>


```C++
HRESULT put_GatewayPreAuthServerAddr(
  [in]  BSTR bstrProxyPreAuthServerAddr
);

HRESULT get_GatewayPreAuthServerAddr(
  [out] BSTR *pbstrProxyPreAuthServerAddr
);
```



## <a name="property-value"></a><span data-ttu-id="5701f-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5701f-110">Property value</span></span>

<span data-ttu-id="5701f-111">Indirizzo Web del server di pre-autenticazione; ad esempio, l'indirizzo Web del server Microsoft Internet Security and Acceleration (ISA).</span><span class="sxs-lookup"><span data-stu-id="5701f-111">The web address of the pre-authentication server; for example, the web address of the Microsoft Internet Security and Acceleration (ISA) server.</span></span> <span data-ttu-id="5701f-112">Specificare l'indirizzo Web utilizzando il formato "https://*hostname*. *NomeDominio*. com/*Websitename*"o" https://*nome host*. *NomeDominio*. com/*Websitename*".</span><span class="sxs-lookup"><span data-stu-id="5701f-112">Specify the web address by using the format "https://*HostName*.*DomainName*.com/*WebsiteName*" or "https://*HostName*.*DomainName*.com/*WebsiteName*".</span></span>

## <a name="error-codes"></a><span data-ttu-id="5701f-113">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="5701f-113">Error codes</span></span>

<span data-ttu-id="5701f-114">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5701f-114">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="5701f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5701f-115">Requirements</span></span>



| <span data-ttu-id="5701f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5701f-116">Requirement</span></span> | <span data-ttu-id="5701f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5701f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5701f-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5701f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5701f-119">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="5701f-119">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="5701f-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5701f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5701f-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5701f-121">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="5701f-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="5701f-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="5701f-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5701f-123"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="5701f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5701f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5701f-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5701f-125"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="5701f-126">IID</span><span class="sxs-lookup"><span data-stu-id="5701f-126">IID</span></span><br/>                      | <span data-ttu-id="5701f-127">IID \_ IMsRdpClientTransportSettings2 è definito come 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="5701f-127">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5701f-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5701f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5701f-129">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="5701f-129">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="5701f-130">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="5701f-130">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





