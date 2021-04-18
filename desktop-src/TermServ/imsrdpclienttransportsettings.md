---
title: Interfaccia IMsRdpClientTransportSettings
description: Gestisce le impostazioni di trasporto client per il server Gateway Desktop remoto di Desktop remoto. | Interfaccia IMsRdpClientTransportSettings
ms.assetid: d2573727-1dcc-4d4d-af5c-038e9467ba84
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientTransportSettings Servizi Desktop remoto
- Interfaccia IMsRdpClientTransportSettings Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec240d008ef2f9469fb67f4041cfb33c08383079
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321239"
---
# <a name="imsrdpclienttransportsettings-interface"></a><span data-ttu-id="c4c36-106">Interfaccia IMsRdpClientTransportSettings</span><span class="sxs-lookup"><span data-stu-id="c4c36-106">IMsRdpClientTransportSettings interface</span></span>

<span data-ttu-id="c4c36-107">Gestisce le impostazioni di trasporto client per il server Gateway Desktop remoto di Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="c4c36-107">Manages client transport settings for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="members"></a><span data-ttu-id="c4c36-108">Membri</span><span class="sxs-lookup"><span data-stu-id="c4c36-108">Members</span></span>

<span data-ttu-id="c4c36-109">L'interfaccia **IMsRdpClientTransportSettings** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="c4c36-109">The **IMsRdpClientTransportSettings** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="c4c36-110">**IMsRdpClientTransportSettings** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c4c36-110">**IMsRdpClientTransportSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="c4c36-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c4c36-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c4c36-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c4c36-112">Properties</span></span>

<span data-ttu-id="c4c36-113">L'interfaccia **IMsRdpClientTransportSettings** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c4c36-113">The **IMsRdpClientTransportSettings** interface has these properties.</span></span>



| <span data-ttu-id="c4c36-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c4c36-114">Property</span></span>                                                                                                          | <span data-ttu-id="c4c36-115">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="c4c36-115">Access type</span></span>           | <span data-ttu-id="c4c36-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4c36-116">Description</span></span>                                                 |
|:------------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------|
| [<span data-ttu-id="c4c36-117">**GatewayCredsSource**</span><span class="sxs-lookup"><span data-stu-id="c4c36-117">**GatewayCredsSource**</span></span>](imsrdpclienttransportsettings-gatewaycredssource.md)<br/>                         | <span data-ttu-id="c4c36-118">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="c4c36-118">Read/write</span></span><br/> | <span data-ttu-id="c4c36-119">Metodo di autenticazione del server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="c4c36-119">The RD Gateway server authentication method.</span></span><br/>     |
| [<span data-ttu-id="c4c36-120">**GatewayDefaultUsageMethod**</span><span class="sxs-lookup"><span data-stu-id="c4c36-120">**GatewayDefaultUsageMethod**</span></span>](imsrdpclienttransportsettings-gatewaydefaultusagemethod.md)<br/>           | <span data-ttu-id="c4c36-121">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4c36-121">Read-only</span></span><br/>  | <span data-ttu-id="c4c36-122">Metodo di utilizzo predefinito del Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="c4c36-122">The default RD Gateway usage method.</span></span><br/>             |
| [<span data-ttu-id="c4c36-123">**GatewayHostname**</span><span class="sxs-lookup"><span data-stu-id="c4c36-123">**GatewayHostname**</span></span>](imsrdpclienttransportsettings-gatewayhostname.md)<br/>                               | <span data-ttu-id="c4c36-124">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="c4c36-124">Read/write</span></span><br/> | <span data-ttu-id="c4c36-125">Nome host del server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="c4c36-125">Host name of the RD Gateway server.</span></span><br/>              |
| [<span data-ttu-id="c4c36-126">**GatewayIsSupported**</span><span class="sxs-lookup"><span data-stu-id="c4c36-126">**GatewayIsSupported**</span></span>](imsrdpclienttransportsettings-gatewayissupported.md)<br/>                         | <span data-ttu-id="c4c36-127">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4c36-127">Read-only</span></span><br/>  | <span data-ttu-id="c4c36-128">Indica se Gateway Desktop remoto è supportato.</span><span class="sxs-lookup"><span data-stu-id="c4c36-128">Indicates whether RD Gateway is supported.</span></span><br/>       |
| [<span data-ttu-id="c4c36-129">**GatewayProfileUsageMethod**</span><span class="sxs-lookup"><span data-stu-id="c4c36-129">**GatewayProfileUsageMethod**</span></span>](imsrdpclienttransportsettings-gatewayprofileusagemethod.md)<br/>           | <span data-ttu-id="c4c36-130">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="c4c36-130">Read/write</span></span><br/> | <span data-ttu-id="c4c36-131">Metodo di utilizzo del profilo Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="c4c36-131">The RD Gateway profile usage method.</span></span><br/>             |
| [<span data-ttu-id="c4c36-132">**GatewayUsageMethod**</span><span class="sxs-lookup"><span data-stu-id="c4c36-132">**GatewayUsageMethod**</span></span>](imsrdpclienttransportsettings-gatewayusagemethod.md)<br/>                         | <span data-ttu-id="c4c36-133">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="c4c36-133">Read/write</span></span><br/> | <span data-ttu-id="c4c36-134">Metodo di utilizzo del server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="c4c36-134">The RD Gateway server usage method.</span></span><br/>              |
| [<span data-ttu-id="c4c36-135">**GatewayUserSelectedCredsSource**</span><span class="sxs-lookup"><span data-stu-id="c4c36-135">**GatewayUserSelectedCredsSource**</span></span>](imsrdpclienttransportsettings-gatewayuserselectedcredssource.md)<br/> | <span data-ttu-id="c4c36-136">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="c4c36-136">Read/write</span></span><br/> | <span data-ttu-id="c4c36-137">Origine della credenziale Gateway Desktop remoto specificata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="c4c36-137">The user-specified RD Gateway credential source.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c4c36-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4c36-138">Requirements</span></span>



| <span data-ttu-id="c4c36-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4c36-139">Requirement</span></span> | <span data-ttu-id="c4c36-140">Valore</span><span class="sxs-lookup"><span data-stu-id="c4c36-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c36-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4c36-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c4c36-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4c36-142">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="c4c36-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4c36-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c4c36-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4c36-144">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="c4c36-145">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c4c36-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="c4c36-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4c36-146"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c4c36-147">DLL</span><span class="sxs-lookup"><span data-stu-id="c4c36-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4c36-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4c36-148"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c4c36-149">IID</span><span class="sxs-lookup"><span data-stu-id="c4c36-149">IID</span></span><br/>                      | <span data-ttu-id="c4c36-150">IID \_ IMsRdpClientTransportSettings è definito come 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="c4c36-150">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c4c36-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4c36-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4c36-152">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="c4c36-152">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="c4c36-153">Riferimento Connessione Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="c4c36-153">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="c4c36-154">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="c4c36-154">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

