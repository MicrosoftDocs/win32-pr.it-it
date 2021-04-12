---
title: Proprietà GatewayPreAuthRequirement di IMsRdpClientTransportSettings2
description: Specifica o recupera l'impostazione per verificare se la funzionalità di password monouso (OTP) del Gateway Desktop remoto (Gateway Desktop remoto) è abilitata.
ms.assetid: cc8f7ebb-16ba-45ed-ba66-de4a339946d0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayPreAuthRequirement
- Servizi Desktop remoto proprietà GatewayPreAuthRequirement, interfaccia IMsRdpClientTransportSettings2
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto, proprietà GatewayPreAuthRequirement
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.get_GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.put_GatewayPreAuthRequirement
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 058ca92237a4f9729f526030f5f8a836ce1c739c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518940"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthrequirement-property"></a><span data-ttu-id="6e3fd-106">Proprietà IMsRdpClientTransportSettings2:: GatewayPreAuthRequirement</span><span class="sxs-lookup"><span data-stu-id="6e3fd-106">IMsRdpClientTransportSettings2::GatewayPreAuthRequirement property</span></span>

<span data-ttu-id="6e3fd-107">Specifica o recupera l'impostazione per verificare se la funzionalità di password monouso (OTP) del Gateway Desktop remoto (Gateway Desktop remoto) è abilitata.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-107">Specifies or retrieves the setting for whether the Remote Desktop Gateway (RD Gateway) one-time password (OTP) feature is enabled.</span></span>

<span data-ttu-id="6e3fd-108">Quando OTP è abilitato, **GatewayPreAuthRequirement** tenta di eseguire una query sul cookie OTP dall'archivio dei cookie Internet usando la proprietà [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md) .</span><span class="sxs-lookup"><span data-stu-id="6e3fd-108">When OTP is enabled, **GatewayPreAuthRequirement** tries to query the OTP cookie from the Internet cookie store by using the [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md) property.</span></span> <span data-ttu-id="6e3fd-109">In caso di esito positivo, **GatewayPreAuthRequirement** invia il cookie OTP al server del firewall, ad esempio Microsoft Internet Security and Acceleration \[ ISA \] Server, per la pre-autenticazione.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-109">If successful, **GatewayPreAuthRequirement** sends the OTP cookie to the firewall server (such as Microsoft Internet Security and Acceleration \[ISA\] server) for pre-authentication.</span></span>

<span data-ttu-id="6e3fd-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e3fd-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e3fd-111">Syntax</span></span>


```C++
HRESULT put_GatewayPreAuthRequirement(
  [in]  ULONG ulProxyPreAuthRequirement
);

HRESULT get_GatewayPreAuthRequirement(
  [out] ULONG *pulProxyPreAuthRequirement
);
```



## <a name="property-value"></a><span data-ttu-id="6e3fd-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6e3fd-112">Property value</span></span>

<span data-ttu-id="6e3fd-113">Se impostato su 1, la funzionalità OTP è abilitata.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-113">If set to 1, the OTP feature is enabled.</span></span> <span data-ttu-id="6e3fd-114">Se è impostato su 0, la funzionalità OTP è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-114">If set to 0, the OTP feature is disabled.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6e3fd-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="6e3fd-115">Error codes</span></span>

<span data-ttu-id="6e3fd-116">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-116">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e3fd-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e3fd-117">Requirements</span></span>



| <span data-ttu-id="6e3fd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e3fd-118">Requirement</span></span> | <span data-ttu-id="6e3fd-119">Valore</span><span class="sxs-lookup"><span data-stu-id="6e3fd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e3fd-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e3fd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6e3fd-121">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="6e3fd-121">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="6e3fd-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e3fd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6e3fd-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e3fd-123">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="6e3fd-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="6e3fd-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="6e3fd-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e3fd-125"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="6e3fd-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6e3fd-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e3fd-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e3fd-127"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="6e3fd-128">IID</span><span class="sxs-lookup"><span data-stu-id="6e3fd-128">IID</span></span><br/>                      | <span data-ttu-id="6e3fd-129">IID \_ IMsRdpClientTransportSettings2 è definito come 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="6e3fd-129">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6e3fd-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e3fd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e3fd-131">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="6e3fd-131">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="6e3fd-132">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="6e3fd-132">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





