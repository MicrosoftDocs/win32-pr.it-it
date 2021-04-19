---
title: Interfaccia IMsRdpClientTransportSettings2
description: Gestisce le impostazioni di trasporto client per il server Gateway Desktop remoto di Desktop remoto. | Interfaccia IMsRdpClientTransportSettings2
ms.assetid: 4f9f1905-2693-4666-9f6f-6e00b1eb6a0f
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f2f4887c6a4f55f3b9c97c389e9afd702d2ffab
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321324"
---
# <a name="imsrdpclienttransportsettings2-interface"></a><span data-ttu-id="00b27-106">Interfaccia IMsRdpClientTransportSettings2</span><span class="sxs-lookup"><span data-stu-id="00b27-106">IMsRdpClientTransportSettings2 interface</span></span>

<span data-ttu-id="00b27-107">Gestisce le impostazioni di trasporto client per il server Gateway Desktop remoto di Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="00b27-107">Manages client transport settings for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="members"></a><span data-ttu-id="00b27-108">Membri</span><span class="sxs-lookup"><span data-stu-id="00b27-108">Members</span></span>

<span data-ttu-id="00b27-109">L'interfaccia **IMsRdpClientTransportSettings2** eredita da [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md).</span><span class="sxs-lookup"><span data-stu-id="00b27-109">The **IMsRdpClientTransportSettings2** interface inherits from [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md).</span></span> <span data-ttu-id="00b27-110">**IMsRdpClientTransportSettings2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="00b27-110">**IMsRdpClientTransportSettings2** also has these types of members:</span></span>

-   [<span data-ttu-id="00b27-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="00b27-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="00b27-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="00b27-112">Properties</span></span>

<span data-ttu-id="00b27-113">L'interfaccia **IMsRdpClientTransportSettings2** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="00b27-113">The **IMsRdpClientTransportSettings2** interface has these properties.</span></span>



| <span data-ttu-id="00b27-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="00b27-114">Property</span></span>                                                                                                    | <span data-ttu-id="00b27-115">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="00b27-115">Access type</span></span>           | <span data-ttu-id="00b27-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00b27-116">Description</span></span>                                                                                       |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00b27-117">**GatewayCredSharing**</span><span class="sxs-lookup"><span data-stu-id="00b27-117">**GatewayCredSharing**</span></span>](imsrdpclienttransportsettings2-gatewaycredsharing.md)<br/>                  | <span data-ttu-id="00b27-118">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="00b27-118">Read/write</span></span><br/> | <span data-ttu-id="00b27-119">Indica se la funzionalità Single Sign-On per Gateway Desktop remoto è abilitata.</span><span class="sxs-lookup"><span data-stu-id="00b27-119">Indicates whether the single sign-on feature for RD Gateway is enabled.</span></span><br/>                |
| [<span data-ttu-id="00b27-120">**GatewayDomain**</span><span class="sxs-lookup"><span data-stu-id="00b27-120">**GatewayDomain**</span></span>](imsrdpclienttransportsettings2-gatewaydomain.md)<br/>                            | <span data-ttu-id="00b27-121">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="00b27-121">Read/write</span></span><br/> | <span data-ttu-id="00b27-122">Nome di dominio fornito da un utente per la connessione al server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="00b27-122">The domain name that a user provides to connect to the RD Gateway server.</span></span><br/>              |
| [<span data-ttu-id="00b27-123">**GatewayEncryptedOtpCookie**</span><span class="sxs-lookup"><span data-stu-id="00b27-123">**GatewayEncryptedOtpCookie**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>     | <span data-ttu-id="00b27-124">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="00b27-124">Read/write</span></span><br/> | <span data-ttu-id="00b27-125">Cookie OTP crittografato.</span><span class="sxs-lookup"><span data-stu-id="00b27-125">The encrypted OTP cookie.</span></span><br/>                                                              |
| [<span data-ttu-id="00b27-126">**GatewayEncryptedOtpCookieSize**</span><span class="sxs-lookup"><span data-stu-id="00b27-126">**GatewayEncryptedOtpCookieSize**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/> | <span data-ttu-id="00b27-127">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="00b27-127">Read/write</span></span><br/> | <span data-ttu-id="00b27-128">Dimensione, in byte, del cookie OTP crittografato.</span><span class="sxs-lookup"><span data-stu-id="00b27-128">The size, in bytes, of the encrypted OTP cookie.</span></span><br/>                                       |
| [<span data-ttu-id="00b27-129">**GatewayPassword**</span><span class="sxs-lookup"><span data-stu-id="00b27-129">**GatewayPassword**</span></span>](imsrdpclienttransportsettings2-gatewaypassword.md)<br/>                        | <span data-ttu-id="00b27-130">Sola scrittura</span><span class="sxs-lookup"><span data-stu-id="00b27-130">Write-only</span></span><br/> | <span data-ttu-id="00b27-131">Password fornita da un utente per la connessione al server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="00b27-131">The password that a user provides to connect to the RD Gateway server.</span></span><br/>                 |
| [<span data-ttu-id="00b27-132">**GatewayPreAuthRequirement**</span><span class="sxs-lookup"><span data-stu-id="00b27-132">**GatewayPreAuthRequirement**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthrequirement.md)<br/>    | <span data-ttu-id="00b27-133">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="00b27-133">Read/write</span></span><br/> | <span data-ttu-id="00b27-134">Indica se la funzionalità di password monouso di Gateway Desktop remoto (OTP) è abilitata.</span><span class="sxs-lookup"><span data-stu-id="00b27-134">Indicates whether the RD Gateway one-time password (OTP) feature is enabled.</span></span><br/>           |
| [<span data-ttu-id="00b27-135">**GatewayPreAuthServerAddr**</span><span class="sxs-lookup"><span data-stu-id="00b27-135">**GatewayPreAuthServerAddr**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>      | <span data-ttu-id="00b27-136">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="00b27-136">Read/write</span></span><br/> | <span data-ttu-id="00b27-137">Indirizzo Web del server di pre-autenticazione.</span><span class="sxs-lookup"><span data-stu-id="00b27-137">The web address of the pre-authentication server.</span></span><br/>                                      |
| [<span data-ttu-id="00b27-138">**GatewaySupportUrl**</span><span class="sxs-lookup"><span data-stu-id="00b27-138">**GatewaySupportUrl**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>             | <span data-ttu-id="00b27-139">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="00b27-139">Read/write</span></span><br/> | <span data-ttu-id="00b27-140">Indirizzo Web del sito che fornisce supporto tecnico per il server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="00b27-140">The web address of the site that provides technical support for the RD Gateway server.</span></span><br/> |
| [<span data-ttu-id="00b27-141">**GatewayUsername**</span><span class="sxs-lookup"><span data-stu-id="00b27-141">**GatewayUsername**</span></span>](imsrdpclienttransportsettings2-gatewayusername.md)<br/>                        | <span data-ttu-id="00b27-142">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="00b27-142">Read/write</span></span><br/> | <span data-ttu-id="00b27-143">Nome utente fornito da un utente per la connessione al server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="00b27-143">The user name that a user provides to connect to the RD Gateway server.</span></span><br/>                |



 

## <a name="requirements"></a><span data-ttu-id="00b27-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00b27-144">Requirements</span></span>



| <span data-ttu-id="00b27-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="00b27-145">Requirement</span></span> | <span data-ttu-id="00b27-146">Valore</span><span class="sxs-lookup"><span data-stu-id="00b27-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00b27-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00b27-147">Minimum supported client</span></span><br/> | <span data-ttu-id="00b27-148">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="00b27-148">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="00b27-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00b27-149">Minimum supported server</span></span><br/> | <span data-ttu-id="00b27-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00b27-150">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="00b27-151">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="00b27-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="00b27-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00b27-152"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="00b27-153">DLL</span><span class="sxs-lookup"><span data-stu-id="00b27-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00b27-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00b27-154"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="00b27-155">IID</span><span class="sxs-lookup"><span data-stu-id="00b27-155">IID</span></span><br/>                      | <span data-ttu-id="00b27-156">IID \_ IMsRdpClientTransportSettings2 è definito come 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="00b27-156">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="00b27-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00b27-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00b27-158">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="00b27-158">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





