---
title: Interfaccia IMsTscSecuredSettings
description: Include metodi per recuperare e impostare le proprietà del controllo ActiveX Desktop remoto che sono limitate a zone di sicurezza URL di Internet Explorer specifiche. | Interfaccia IMsTscSecuredSettings
ms.assetid: 1136dbc5-abe6-40e0-b44f-700a1460fbd2
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsTscSecuredSettings Servizi Desktop remoto
- Interfaccia IMsTscSecuredSettings Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2037393147bd5a2e35d6eb803951890c9b5e7de5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321461"
---
# <a name="imstscsecuredsettings-interface"></a><span data-ttu-id="e1777-106">Interfaccia IMsTscSecuredSettings</span><span class="sxs-lookup"><span data-stu-id="e1777-106">IMsTscSecuredSettings interface</span></span>

<span data-ttu-id="e1777-107">Include metodi per recuperare e impostare le proprietà del controllo ActiveX Desktop remoto che sono limitate a zone di sicurezza URL di Internet Explorer specifiche.</span><span class="sxs-lookup"><span data-stu-id="e1777-107">Includes methods to retrieve and set properties of the Remote Desktop ActiveX control that are restricted to specific Internet Explorer URL security zones.</span></span> <span data-ttu-id="e1777-108">Le proprietà includono quelle che specificano la modalità del controllo client (modalità schermo intero o modalità finestra) e il programma da avviare dopo la connessione al server di host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="e1777-108">Properties include those that specify the mode of the client control (full-screen mode or window mode) and the program to start upon connection to the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="e1777-109">Questi metodi sono disponibili anche tramite l'interfaccia [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="e1777-109">These methods are also available through the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="e1777-110">Membri</span><span class="sxs-lookup"><span data-stu-id="e1777-110">Members</span></span>

<span data-ttu-id="e1777-111">L'interfaccia **IMsTscSecuredSettings** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="e1777-111">The **IMsTscSecuredSettings** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="e1777-112">**IMsTscSecuredSettings** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e1777-112">**IMsTscSecuredSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="e1777-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e1777-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e1777-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e1777-114">Properties</span></span>

<span data-ttu-id="e1777-115">L'interfaccia **IMsTscSecuredSettings** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e1777-115">The **IMsTscSecuredSettings** interface has these properties.</span></span>



| <span data-ttu-id="e1777-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e1777-116">Property</span></span>                                                              | <span data-ttu-id="e1777-117">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="e1777-117">Access type</span></span>           | <span data-ttu-id="e1777-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1777-118">Description</span></span>                                                                |
|:----------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="e1777-119">**FullScreen**</span><span class="sxs-lookup"><span data-stu-id="e1777-119">**FullScreen**</span></span>](imstscsecuredsettings-fullscreen.md)<br/>     | <span data-ttu-id="e1777-120">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="e1777-120">Read/write</span></span><br/> | <span data-ttu-id="e1777-121">Stato a schermo intero del controllo client.</span><span class="sxs-lookup"><span data-stu-id="e1777-121">The full-screen state of the client control.</span></span><br/>                    |
| [<span data-ttu-id="e1777-122">**StartProgram**</span><span class="sxs-lookup"><span data-stu-id="e1777-122">**StartProgram**</span></span>](imstscsecuredsettings-startprogram.md)<br/> | <span data-ttu-id="e1777-123">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="e1777-123">Read/write</span></span><br/> | <span data-ttu-id="e1777-124">Programma da avviare sul server remoto dopo la connessione.</span><span class="sxs-lookup"><span data-stu-id="e1777-124">The program to be started on the remote server upon connection.</span></span><br/> |
| [<span data-ttu-id="e1777-125">**WorkDir**</span><span class="sxs-lookup"><span data-stu-id="e1777-125">**WorkDir**</span></span>](imstscsecuredsettings-workdir.md)<br/>           | <span data-ttu-id="e1777-126">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="e1777-126">Read/write</span></span><br/> | <span data-ttu-id="e1777-127">Directory di lavoro del programma di avvio.</span><span class="sxs-lookup"><span data-stu-id="e1777-127">The working directory of the start program.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="e1777-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1777-128">Remarks</span></span>

<span data-ttu-id="e1777-129">Per ulteriori informazioni sui metodi di questa interfaccia, vedere la pagina [relativa a come fornire la sicurezza del client RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="e1777-129">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information about the methods of this interface.</span></span>

<span data-ttu-id="e1777-130">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e1777-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1777-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1777-131">Requirements</span></span>



| <span data-ttu-id="e1777-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1777-132">Requirement</span></span> | <span data-ttu-id="e1777-133">Valore</span><span class="sxs-lookup"><span data-stu-id="e1777-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1777-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1777-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e1777-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1777-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e1777-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1777-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e1777-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1777-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e1777-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e1777-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="e1777-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1777-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e1777-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e1777-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1777-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1777-141"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1777-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1777-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1777-143">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="e1777-143">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="e1777-144">Riferimento Connessione Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="e1777-144">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

