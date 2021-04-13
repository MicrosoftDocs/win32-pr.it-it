---
title: Interfaccia IMsRdpClientAdvancedSettings2
description: Gestisce le impostazioni client avanzate. Deriva dall'interfaccia IMsRdpClientAdvancedSettings.
ms.assetid: 78cffdf5-bd99-4140-80b6-aa8632894487
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70d7f9ad9b93c0f3cd1d62fdbbaddf4faa55ad9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340873"
---
# <a name="imsrdpclientadvancedsettings2-interface"></a><span data-ttu-id="7d4ad-106">Interfaccia IMsRdpClientAdvancedSettings2</span><span class="sxs-lookup"><span data-stu-id="7d4ad-106">IMsRdpClientAdvancedSettings2 interface</span></span>

<span data-ttu-id="7d4ad-107">Gestisce le impostazioni client avanzate.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-107">Manages advanced client settings.</span></span> <span data-ttu-id="7d4ad-108">Deriva dall'interfaccia [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="7d4ad-108">Derives from the [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) interface.</span></span> <span data-ttu-id="7d4ad-109">Questa interfaccia include metodi per recuperare e impostare proprietà avanzate (facoltative) per il controllo ActiveX Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-109">This interface includes methods to retrieve and set advanced (optional) properties for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="7d4ad-110">Per ottenere un'istanza di questa interfaccia, usare la proprietà [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) per ottenere un puntatore a interfaccia [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="7d4ad-110">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="7d4ad-111">Chiamare quindi [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul puntatore **IMsTscAdvancedSettings** e passare **IID \_ IMsRdpClientAdvancedSettings2** a **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-111">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings2** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="7d4ad-112">Membri</span><span class="sxs-lookup"><span data-stu-id="7d4ad-112">Members</span></span>

<span data-ttu-id="7d4ad-113">L'interfaccia **IMsRdpClientAdvancedSettings2** eredita da [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md).</span><span class="sxs-lookup"><span data-stu-id="7d4ad-113">The **IMsRdpClientAdvancedSettings2** interface inherits from [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md).</span></span> <span data-ttu-id="7d4ad-114">**IMsRdpClientAdvancedSettings2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7d4ad-114">**IMsRdpClientAdvancedSettings2** also has these types of members:</span></span>

-   [<span data-ttu-id="7d4ad-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7d4ad-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7d4ad-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7d4ad-116">Properties</span></span>

<span data-ttu-id="7d4ad-117">L'interfaccia **IMsRdpClientAdvancedSettings2** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-117">The **IMsRdpClientAdvancedSettings2** interface has these properties.</span></span>



| <span data-ttu-id="7d4ad-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7d4ad-118">Property</span></span>                                                                                      | <span data-ttu-id="7d4ad-119">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="7d4ad-119">Access type</span></span>           | <span data-ttu-id="7d4ad-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d4ad-120">Description</span></span>                                                                                                                                           |
|:----------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d4ad-121">**CanAutoReconnect**</span><span class="sxs-lookup"><span data-stu-id="7d4ad-121">**CanAutoReconnect**</span></span>](imsrdpclientadvancedsettings2-canautoreconnect.md)<br/>         | <span data-ttu-id="7d4ad-122">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7d4ad-122">Read-only</span></span><br/>  | <span data-ttu-id="7d4ad-123">Specifica se il controllo client è in grado di riconnettersi automaticamente alla sessione corrente in caso di disconnessione di rete.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-123">Specifies whether the client control is able to reconnect automatically to the current session in the event of a network disconnection.</span></span><br/>    |
| [<span data-ttu-id="7d4ad-124">**EnableAutoReconnect**</span><span class="sxs-lookup"><span data-stu-id="7d4ad-124">**EnableAutoReconnect**</span></span>](imsrdpclientadvancedsettings2-enableautoreconnect.md)<br/>   | <span data-ttu-id="7d4ad-125">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="7d4ad-125">Read/write</span></span><br/> | <span data-ttu-id="7d4ad-126">Specifica se abilitare il controllo client per la riconnessione automatica a una sessione in caso di disconnessione di rete.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-126">Specifies whether to enable the client control to reconnect automatically to a session in the event of a network disconnection.</span></span><br/>            |
| [<span data-ttu-id="7d4ad-127">**MaxReconnectAttempts**</span><span class="sxs-lookup"><span data-stu-id="7d4ad-127">**MaxReconnectAttempts**</span></span>](imsrdpclientadvancedsettings2-maxreconnectattempts.md)<br/> | <span data-ttu-id="7d4ad-128">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="7d4ad-128">Read/write</span></span><br/> | <span data-ttu-id="7d4ad-129">Specifica il numero di tentativi di riconnessione durante la riconnessione automatica.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-129">Specifies the number of times to try to reconnect during automatic reconnection.</span></span> <span data-ttu-id="7d4ad-130">I valori validi di questa proprietà sono compresi tra 0 e 200.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-130">The valid values of this property are 0 to 200 inclusive.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7d4ad-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d4ad-131">Remarks</span></span>

<span data-ttu-id="7d4ad-132">Questa interfaccia è stata estesa dalle interfacce seguenti, in cui ogni nuova interfaccia eredita tutti i metodi e le proprietà delle interfacce precedenti:</span><span class="sxs-lookup"><span data-stu-id="7d4ad-132">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="7d4ad-133">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="7d4ad-133">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
-   [<span data-ttu-id="7d4ad-134">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="7d4ad-134">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
-   [<span data-ttu-id="7d4ad-135">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="7d4ad-135">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="7d4ad-136">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="7d4ad-136">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="7d4ad-137">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="7d4ad-137">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)

<span data-ttu-id="7d4ad-138">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7d4ad-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d4ad-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d4ad-139">Requirements</span></span>



| <span data-ttu-id="7d4ad-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d4ad-140">Requirement</span></span> | <span data-ttu-id="7d4ad-141">Valore</span><span class="sxs-lookup"><span data-stu-id="7d4ad-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d4ad-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d4ad-142">Minimum supported client</span></span><br/> | <span data-ttu-id="7d4ad-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d4ad-143">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="7d4ad-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d4ad-144">Minimum supported server</span></span><br/> | <span data-ttu-id="7d4ad-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d4ad-145">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="7d4ad-146">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="7d4ad-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="7d4ad-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d4ad-147"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="7d4ad-148">DLL</span><span class="sxs-lookup"><span data-stu-id="7d4ad-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d4ad-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d4ad-149"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="7d4ad-150">IID</span><span class="sxs-lookup"><span data-stu-id="7d4ad-150">IID</span></span><br/>                      | <span data-ttu-id="7d4ad-151">IID \_ IMsRdpClientAdvancedSettings2 è definito come 9ac42117-2b76-4320-aa44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="7d4ad-151">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7d4ad-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d4ad-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d4ad-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="7d4ad-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="7d4ad-154">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="7d4ad-154">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="7d4ad-155">Riferimento Connessione Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="7d4ad-155">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

