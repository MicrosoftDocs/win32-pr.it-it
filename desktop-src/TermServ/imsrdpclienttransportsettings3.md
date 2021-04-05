---
title: Interfaccia IMsRdpClientTransportSettings3
description: Definisce proprietà aggiuntive per il server Gateway Desktop remoto di Desktop remoto. | Interfaccia IMsRdpClientTransportSettings3
ms.assetid: c0bdfe23-9a26-4feb-b9b7-e52f04f23aa1
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientTransportSettings3 Servizi Desktop remoto
- Interfaccia IMsRdpClientTransportSettings3 Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7498db4b39a4ad0e89761cbec439895e4e9a152
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886105"
---
# <a name="imsrdpclienttransportsettings3-interface"></a><span data-ttu-id="bd68c-106">Interfaccia IMsRdpClientTransportSettings3</span><span class="sxs-lookup"><span data-stu-id="bd68c-106">IMsRdpClientTransportSettings3 interface</span></span>

<span data-ttu-id="bd68c-107">Definisce proprietà aggiuntive per il server Gateway Desktop remoto di Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="bd68c-107">Defines additional properties for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="members"></a><span data-ttu-id="bd68c-108">Membri</span><span class="sxs-lookup"><span data-stu-id="bd68c-108">Members</span></span>

<span data-ttu-id="bd68c-109">L'interfaccia **IMsRdpClientTransportSettings3** eredita da [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md).</span><span class="sxs-lookup"><span data-stu-id="bd68c-109">The **IMsRdpClientTransportSettings3** interface inherits from [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md).</span></span> <span data-ttu-id="bd68c-110">**IMsRdpClientTransportSettings3** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bd68c-110">**IMsRdpClientTransportSettings3** also has these types of members:</span></span>

-   [<span data-ttu-id="bd68c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bd68c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bd68c-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bd68c-112">Properties</span></span>

<span data-ttu-id="bd68c-113">L'interfaccia **IMsRdpClientTransportSettings3** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bd68c-113">The **IMsRdpClientTransportSettings3** interface has these properties.</span></span>



| <span data-ttu-id="bd68c-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bd68c-114">Property</span></span>                                                                                                           | <span data-ttu-id="bd68c-115">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="bd68c-115">Access type</span></span>           | <span data-ttu-id="bd68c-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd68c-116">Description</span></span>                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd68c-117">**GatewayAuthCookieServerAddr**</span><span class="sxs-lookup"><span data-stu-id="bd68c-117">**GatewayAuthCookieServerAddr**</span></span>](imsrdpclienttransportsettings3-gatewayauthcookieserveraddr.md)<br/>       | <span data-ttu-id="bd68c-118">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="bd68c-118">Read/write</span></span><br/> | <span data-ttu-id="bd68c-119">Indirizzo del server per l'autenticazione basata su cookie.</span><span class="sxs-lookup"><span data-stu-id="bd68c-119">The server address for cookie-based authentication.</span></span><br/>                                                                                       |
| [<span data-ttu-id="bd68c-120">**GatewayAuthLoginPage**</span><span class="sxs-lookup"><span data-stu-id="bd68c-120">**GatewayAuthLoginPage**</span></span>](imsrdpclienttransportsettings3-gatewayauthloginpage.md)<br/>                     | <span data-ttu-id="bd68c-121">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="bd68c-121">Read/write</span></span><br/> | <span data-ttu-id="bd68c-122">Indirizzo della pagina Web di accesso da usare per autenticare un utente.</span><span class="sxs-lookup"><span data-stu-id="bd68c-122">The address of the login webpage to use to authenticate a user.</span></span><br/>                                                                           |
| [<span data-ttu-id="bd68c-123">**GatewayCredSourceCookie**</span><span class="sxs-lookup"><span data-stu-id="bd68c-123">**GatewayCredSourceCookie**</span></span>](imsrdpclienttransportsettings3-gatewaycredsourcecookie.md)<br/>               | <span data-ttu-id="bd68c-124">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="bd68c-124">Read/write</span></span><br/> | <span data-ttu-id="bd68c-125">Specifica se l'origine delle credenziali è basata su cookie.</span><span class="sxs-lookup"><span data-stu-id="bd68c-125">Specifies if the credential source is cookie based.</span></span><br/>                                                                                       |
| [<span data-ttu-id="bd68c-126">**GatewayEncryptedAuthCookie**</span><span class="sxs-lookup"><span data-stu-id="bd68c-126">**GatewayEncryptedAuthCookie**</span></span>](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md)<br/>         | <span data-ttu-id="bd68c-127">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="bd68c-127">Read/write</span></span><br/> | <span data-ttu-id="bd68c-128">Cookie di autenticazione crittografato.</span><span class="sxs-lookup"><span data-stu-id="bd68c-128">The encrypted authentication cookie.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="bd68c-129">**GatewayEncryptedAuthCookieSize**</span><span class="sxs-lookup"><span data-stu-id="bd68c-129">**GatewayEncryptedAuthCookieSize**</span></span>](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)<br/> | <span data-ttu-id="bd68c-130">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="bd68c-130">Read/write</span></span><br/> | <span data-ttu-id="bd68c-131">Dimensione, in caratteri, della proprietà [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) .</span><span class="sxs-lookup"><span data-stu-id="bd68c-131">The size, in characters, of the [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) property.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bd68c-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd68c-132">Requirements</span></span>



| <span data-ttu-id="bd68c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd68c-133">Requirement</span></span> | <span data-ttu-id="bd68c-134">Valore</span><span class="sxs-lookup"><span data-stu-id="bd68c-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd68c-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd68c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bd68c-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bd68c-136">Windows 7</span></span><br/>                                                                              |
| <span data-ttu-id="bd68c-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd68c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bd68c-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd68c-138">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="bd68c-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="bd68c-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="bd68c-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd68c-140"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="bd68c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="bd68c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd68c-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd68c-142"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="bd68c-143">IID</span><span class="sxs-lookup"><span data-stu-id="bd68c-143">IID</span></span><br/>                      | <span data-ttu-id="bd68c-144">IID \_ IMsRdpClientTransportSettings3 è definito come 3D5B21AC-748D-41DE-8F30-E15169586BD4</span><span class="sxs-lookup"><span data-stu-id="bd68c-144">IID\_IMsRdpClientTransportSettings3 is defined as 3D5B21AC-748D-41DE-8F30-E15169586BD4</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bd68c-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd68c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd68c-146">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="bd68c-146">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





