---
title: Proprietà GatewayCredSharing di IMsRdpClientTransportSettings2
description: Specifica o recupera l'impostazione per verificare se la funzionalità di condivisione delle credenziali del gateway di Desktop remoto (Gateway Desktop remoto) è abilitata.
ms.assetid: 296dc578-376d-41f6-988a-286fe744959f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayCredSharing
- Servizi Desktop remoto proprietà GatewayCredSharing, interfaccia IMsRdpClientTransportSettings2
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto, proprietà GatewayCredSharing
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayCredSharing
- IMsRdpClientTransportSettings2.get_GatewayCredSharing
- IMsRdpClientTransportSettings2.put_GatewayCredSharing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329e425631b674e050f246c4105115bd4326be3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475628"
---
# <a name="imsrdpclienttransportsettings2gatewaycredsharing-property"></a><span data-ttu-id="b0047-106">Proprietà IMsRdpClientTransportSettings2:: GatewayCredSharing</span><span class="sxs-lookup"><span data-stu-id="b0047-106">IMsRdpClientTransportSettings2::GatewayCredSharing property</span></span>

<span data-ttu-id="b0047-107">Specifica o recupera l'impostazione per verificare se la funzionalità di condivisione delle credenziali del gateway di Desktop remoto (Gateway Desktop remoto) è abilitata.</span><span class="sxs-lookup"><span data-stu-id="b0047-107">Specifies or retrieves the setting for whether the Remote Desktop Gateway (RD Gateway) credential sharing feature is enabled.</span></span> <span data-ttu-id="b0047-108">Quando la funzionalità è abilitata, il controllo ActiveX Desktop remoto tenta di utilizzare le stesse credenziali per l'autenticazione al server di host sessione Desktop remoto (host sessione Desktop remoto) e al server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="b0047-108">When the feature is enabled, the Remote Desktop ActiveX control tries to use the same credentials to authenticate to the Remote Desktop Session Host (RD Session Host) server and to the RD Gateway server.</span></span>

<span data-ttu-id="b0047-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b0047-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0047-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b0047-110">Syntax</span></span>


```C++
HRESULT put_GatewayCredSharing(
  [in]  ULONG ulProxyCredSharing
);

HRESULT get_GatewayCredSharing(
  [out] ULONG *pulProxyCredSharing
);
```



## <a name="property-value"></a><span data-ttu-id="b0047-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b0047-111">Property value</span></span>

<span data-ttu-id="b0047-112">Se impostato su uno, la condivisione delle credenziali è abilitata.</span><span class="sxs-lookup"><span data-stu-id="b0047-112">If set to one, credential sharing is enabled.</span></span> <span data-ttu-id="b0047-113">Se è impostato su zero, la condivisione delle credenziali è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="b0047-113">If set to zero, credential sharing is disabled.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b0047-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="b0047-114">Error codes</span></span>

<span data-ttu-id="b0047-115">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b0047-115">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0047-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0047-116">Remarks</span></span>

<span data-ttu-id="b0047-117">Questa proprietà viene utilizzata dal controllo ActiveX per implementare una singola richiesta di condivisione delle credenziali tra il server Host sessione Desktop remoto e il server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="b0047-117">This property is used by the ActiveX control to implement a single prompt for credential sharing between the RD Session Host server and the RD Gateway server.</span></span> <span data-ttu-id="b0047-118">La condivisione delle credenziali non supporta la condivisione delle password basata sul Web con [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md) o [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md).</span><span class="sxs-lookup"><span data-stu-id="b0047-118">Credential sharing does not support web-based password sharing with [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md) or [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0047-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0047-119">Requirements</span></span>



| <span data-ttu-id="b0047-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0047-120">Requirement</span></span> | <span data-ttu-id="b0047-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b0047-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0047-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0047-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b0047-123">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="b0047-123">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="b0047-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0047-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b0047-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0047-125">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="b0047-126">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="b0047-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="b0047-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0047-127"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="b0047-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b0047-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0047-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0047-129"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="b0047-130">IID</span><span class="sxs-lookup"><span data-stu-id="b0047-130">IID</span></span><br/>                      | <span data-ttu-id="b0047-131">IID \_ IMsRdpClientTransportSettings2 è definito come 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="b0047-131">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b0047-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b0047-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0047-133">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="b0047-133">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="b0047-134">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="b0047-134">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





