---
title: Interfaccia IMsRdpClientSecuredSettings
description: Include metodi per recuperare e impostare le proprietà del controllo ActiveX Desktop remoto che sono limitate a zone di sicurezza URL di Internet Explorer specifiche. | Interfaccia IMsRdpClientSecuredSettings
ms.assetid: 56d3193d-a0fb-468a-9fb3-c080db5500b7
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientSecuredSettings Servizi Desktop remoto
- Interfaccia IMsRdpClientSecuredSettings Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396e6b58b2be0122076b5529b910423377417fa6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321561"
---
# <a name="imsrdpclientsecuredsettings-interface"></a><span data-ttu-id="ee919-106">Interfaccia IMsRdpClientSecuredSettings</span><span class="sxs-lookup"><span data-stu-id="ee919-106">IMsRdpClientSecuredSettings interface</span></span>

<span data-ttu-id="ee919-107">Include metodi per recuperare e impostare le proprietà del controllo ActiveX Desktop remoto che sono limitate a zone di sicurezza URL di Internet Explorer specifiche.</span><span class="sxs-lookup"><span data-stu-id="ee919-107">Includes methods to retrieve and set properties of the Remote Desktop ActiveX control that are restricted to specific Internet Explorer URL security zones.</span></span>

## <a name="members"></a><span data-ttu-id="ee919-108">Membri</span><span class="sxs-lookup"><span data-stu-id="ee919-108">Members</span></span>

<span data-ttu-id="ee919-109">L'interfaccia **IMsRdpClientSecuredSettings** eredita da [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span><span class="sxs-lookup"><span data-stu-id="ee919-109">The **IMsRdpClientSecuredSettings** interface inherits from [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span></span> <span data-ttu-id="ee919-110">**IMsRdpClientSecuredSettings** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ee919-110">**IMsRdpClientSecuredSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="ee919-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ee919-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ee919-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ee919-112">Properties</span></span>

<span data-ttu-id="ee919-113">L'interfaccia **IMsRdpClientSecuredSettings** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ee919-113">The **IMsRdpClientSecuredSettings** interface has these properties.</span></span>



| <span data-ttu-id="ee919-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ee919-114">Property</span></span>                                                                                   | <span data-ttu-id="ee919-115">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="ee919-115">Access type</span></span>           | <span data-ttu-id="ee919-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee919-116">Description</span></span>                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [<span data-ttu-id="ee919-117">**AudioRedirectionMode**</span><span class="sxs-lookup"><span data-stu-id="ee919-117">**AudioRedirectionMode**</span></span>](imsrdpclientsecuredsettings-autoredirectionmode.md)<br/> | <span data-ttu-id="ee919-118">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="ee919-118">Read/write</span></span><br/> | <span data-ttu-id="ee919-119">Impostazioni del reindirizzamento audio.</span><span class="sxs-lookup"><span data-stu-id="ee919-119">The audio redirection settings.</span></span><br/>    |
| [<span data-ttu-id="ee919-120">**KeyboardHookMode**</span><span class="sxs-lookup"><span data-stu-id="ee919-120">**KeyboardHookMode**</span></span>](imsrdpclientsecuredsettings-keyboardhookmode.md)<br/>        | <span data-ttu-id="ee919-121">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="ee919-121">Read/write</span></span><br/> | <span data-ttu-id="ee919-122">Impostazioni di Reindirizzamento da tastiera.</span><span class="sxs-lookup"><span data-stu-id="ee919-122">The keyboard redirection settings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ee919-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee919-123">Remarks</span></span>

<span data-ttu-id="ee919-124">Non è possibile impostare queste proprietà quando il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="ee919-124">These properties cannot be set when the control is connected.</span></span>

<span data-ttu-id="ee919-125">Per ulteriori informazioni sui metodi di questa interfaccia, vedere la pagina [relativa a come fornire la sicurezza del client RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="ee919-125">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information about the methods of this interface.</span></span>

<span data-ttu-id="ee919-126">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ee919-126">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee919-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee919-127">Requirements</span></span>



| <span data-ttu-id="ee919-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee919-128">Requirement</span></span> | <span data-ttu-id="ee919-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ee919-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee919-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee919-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ee919-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee919-131">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="ee919-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee919-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ee919-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee919-133">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="ee919-134">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ee919-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="ee919-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee919-135"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="ee919-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ee919-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee919-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee919-137"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="ee919-138">IID</span><span class="sxs-lookup"><span data-stu-id="ee919-138">IID</span></span><br/>                      | <span data-ttu-id="ee919-139">IID \_ IMsRdpClientSecuredSettings è definito come 605befcf-39c1-45cc-A811-068fb7be346d</span><span class="sxs-lookup"><span data-stu-id="ee919-139">IID\_IMsRdpClientSecuredSettings is defined as 605befcf-39c1-45cc-a811-068fb7be346d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee919-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee919-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee919-141">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="ee919-141">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="ee919-142">Riferimento Connessione Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="ee919-142">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





