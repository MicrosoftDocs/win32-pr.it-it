---
title: Interfaccia IMsRdpClientAdvancedSettings6
description: Espone le proprietà che gestiscono le impostazioni avanzate del controllo ActiveX.
ms.assetid: 45b48cdf-3860-4359-99b2-8d2598146d1d
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e61d3358f1af228dcd1b5a7431ee759b486df7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301893"
---
# <a name="imsrdpclientadvancedsettings6-interface"></a><span data-ttu-id="140e4-105">Interfaccia IMsRdpClientAdvancedSettings6</span><span class="sxs-lookup"><span data-stu-id="140e4-105">IMsRdpClientAdvancedSettings6 interface</span></span>

<span data-ttu-id="140e4-106">Espone le proprietà che gestiscono le impostazioni avanzate del controllo ActiveX.</span><span class="sxs-lookup"><span data-stu-id="140e4-106">Exposes properties that manage advanced ActiveX control settings.</span></span> <span data-ttu-id="140e4-107">L'interfaccia **IMsRdpClientAdvancedSettings6** è derivata dall'interfaccia [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) .</span><span class="sxs-lookup"><span data-stu-id="140e4-107">The **IMsRdpClientAdvancedSettings6** interface is derived from the [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) interface.</span></span>

<span data-ttu-id="140e4-108">Per ottenere un'istanza di questa interfaccia, usare la proprietà [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) per ottenere un puntatore a interfaccia [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="140e4-108">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="140e4-109">Chiamare quindi [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul puntatore **IMsTscAdvancedSettings** e passare **IID \_ IMsRdpClientAdvancedSettings6** a **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="140e4-109">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings6** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="140e4-110">Membri</span><span class="sxs-lookup"><span data-stu-id="140e4-110">Members</span></span>

<span data-ttu-id="140e4-111">L'interfaccia **IMsRdpClientAdvancedSettings6** eredita da [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md).</span><span class="sxs-lookup"><span data-stu-id="140e4-111">The **IMsRdpClientAdvancedSettings6** interface inherits from [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md).</span></span> <span data-ttu-id="140e4-112">**IMsRdpClientAdvancedSettings6** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="140e4-112">**IMsRdpClientAdvancedSettings6** also has these types of members:</span></span>

-   [<span data-ttu-id="140e4-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="140e4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="140e4-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="140e4-114">Properties</span></span>

<span data-ttu-id="140e4-115">L'interfaccia **IMsRdpClientAdvancedSettings6** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="140e4-115">The **IMsRdpClientAdvancedSettings6** interface has these properties.</span></span>



| <span data-ttu-id="140e4-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="140e4-116">Property</span></span>                                                                                                  | <span data-ttu-id="140e4-117">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="140e4-117">Access type</span></span>           | <span data-ttu-id="140e4-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="140e4-118">Description</span></span>                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="140e4-119">**AuthenticationServiceClass**</span><span class="sxs-lookup"><span data-stu-id="140e4-119">**AuthenticationServiceClass**</span></span>](imsrdpclientadvancedsettings6-authenticationserviceclass.md)<br/> | <span data-ttu-id="140e4-120">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="140e4-120">Read/write</span></span><br/> | <span data-ttu-id="140e4-121">Specifica il nome dell'entità servizio (SPN) da utilizzare per l'autenticazione al server.</span><span class="sxs-lookup"><span data-stu-id="140e4-121">Specifies the service principal name (SPN) to use for authentication to the server.</span></span><br/>                                     |
| [<span data-ttu-id="140e4-122">**AuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="140e4-122">**AuthenticationType**</span></span>](imsrdpclientadvancedsettings6-authenticationtype.md)<br/>                 | <span data-ttu-id="140e4-123">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="140e4-123">Read-only</span></span><br/>  | <span data-ttu-id="140e4-124">Specifica il tipo di autenticazione utilizzato per la connessione.</span><span class="sxs-lookup"><span data-stu-id="140e4-124">Specifies the type of authentication used for this connection.</span></span><br/>                                                          |
| [<span data-ttu-id="140e4-125">**ConnectToAdministerServer**</span><span class="sxs-lookup"><span data-stu-id="140e4-125">**ConnectToAdministerServer**</span></span>](imsrdpclientadvancedsettings6-connecttoadministerserver.md)<br/>   | <span data-ttu-id="140e4-126">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="140e4-126">Read/write</span></span><br/> | <span data-ttu-id="140e4-127">Recupera o specifica se il controllo ActiveX deve tentare di connettersi al server per scopi amministrativi.</span><span class="sxs-lookup"><span data-stu-id="140e4-127">Retrieves or specifies whether the ActiveX control should attempt to connect to the server for administrative purposes.</span></span><br/> |
| [<span data-ttu-id="140e4-128">**EnableCredSspSupport**</span><span class="sxs-lookup"><span data-stu-id="140e4-128">**EnableCredSspSupport**</span></span>](imsrdpclientadvancedsettings6-enablecredsspsupport.md)<br/>             | <span data-ttu-id="140e4-129">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="140e4-129">Read/write</span></span><br/> | <span data-ttu-id="140e4-130">Specifica se il provider del servizio di sicurezza delle credenziali (CredSSP) è abilitato per la connessione.</span><span class="sxs-lookup"><span data-stu-id="140e4-130">Specifies whether the Credential Security Service Provider (CredSSP) is enabled for this connection.</span></span><br/>                    |
| [<span data-ttu-id="140e4-131">**HotKeyFocusReleaseLeft**</span><span class="sxs-lookup"><span data-stu-id="140e4-131">**HotKeyFocusReleaseLeft**</span></span>](imsrdpclientadvancedsettings6-hotkeyfocusreleaseleft.md)<br/>         | <span data-ttu-id="140e4-132">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="140e4-132">Read/write</span></span><br/> | <span data-ttu-id="140e4-133">Specifica il codice della chiave virtuale da aggiungere a CTRL + ALT per determinare la sostituzione del tasto di scelta rapida per CTRL + ALT + freccia sinistra.</span><span class="sxs-lookup"><span data-stu-id="140e4-133">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for CTRL+ALT+LEFT ARROW.</span></span><br/>          |
| [<span data-ttu-id="140e4-134">**HotKeyFocusReleaseRight**</span><span class="sxs-lookup"><span data-stu-id="140e4-134">**HotKeyFocusReleaseRight**</span></span>](imsrdpclientadvancedsettings6-hotkeyfocusreleaseright.md)<br/>       | <span data-ttu-id="140e4-135">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="140e4-135">Read/write</span></span><br/> | <span data-ttu-id="140e4-136">Specifica il codice della chiave virtuale da aggiungere a CTRL + ALT per determinare la sostituzione del tasto di scelta rapida per CTRL + ALT + freccia destra.</span><span class="sxs-lookup"><span data-stu-id="140e4-136">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for CTRL+ALT+RIGHT ARROW.</span></span><br/>         |
| [<span data-ttu-id="140e4-137">**PCB**</span><span class="sxs-lookup"><span data-stu-id="140e4-137">**PCB**</span></span>](imsrdpclientadvancedsettings6-pcb.md)<br/>                                               | <span data-ttu-id="140e4-138">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="140e4-138">Read/write</span></span><br/> | <span data-ttu-id="140e4-139">Specifica l'impostazione del BLOB di preconnessione (PCB) da usare prima della connessione per la trasmissione al server.</span><span class="sxs-lookup"><span data-stu-id="140e4-139">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span><br/>               |
| [<span data-ttu-id="140e4-140">**RelativeMouseMode**</span><span class="sxs-lookup"><span data-stu-id="140e4-140">**RelativeMouseMode**</span></span>](imsrdpclientadvancedsettings6-relativemousemode.md)<br/>                   | <span data-ttu-id="140e4-141">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="140e4-141">Read/write</span></span><br/> | <span data-ttu-id="140e4-142">Specifica se il mouse deve utilizzare la modalità relativa.</span><span class="sxs-lookup"><span data-stu-id="140e4-142">Specifies whether the mouse should use relative mode.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="140e4-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="140e4-143">Remarks</span></span>

<span data-ttu-id="140e4-144">Questa interfaccia è stata estesa dall'interfaccia [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) , che eredita tutti i metodi e le proprietà delle interfacce precedenti.</span><span class="sxs-lookup"><span data-stu-id="140e4-144">This interface has been extended by the [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) interface, inheriting all the methods and properties of the previous interfaces.</span></span>

## <a name="requirements"></a><span data-ttu-id="140e4-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="140e4-145">Requirements</span></span>



| <span data-ttu-id="140e4-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="140e4-146">Requirement</span></span> | <span data-ttu-id="140e4-147">Valore</span><span class="sxs-lookup"><span data-stu-id="140e4-147">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="140e4-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="140e4-148">Minimum supported client</span></span><br/> | <span data-ttu-id="140e4-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="140e4-149">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="140e4-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="140e4-150">Minimum supported server</span></span><br/> | <span data-ttu-id="140e4-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="140e4-151">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="140e4-152">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="140e4-152">Type library</span></span><br/>             | <dl> <span data-ttu-id="140e4-153"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="140e4-153"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="140e4-154">DLL</span><span class="sxs-lookup"><span data-stu-id="140e4-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="140e4-155"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="140e4-155"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="140e4-156">IID</span><span class="sxs-lookup"><span data-stu-id="140e4-156">IID</span></span><br/>                      | <span data-ttu-id="140e4-157">IID \_ IMsRdpClientAdvancedSettings6 è definito come 222c4b5d-45D9-4DF0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="140e4-157">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="140e4-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="140e4-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="140e4-159">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="140e4-159">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="140e4-160">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="140e4-160">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="140e4-161">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="140e4-161">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="140e4-162">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="140e4-162">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="140e4-163">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="140e4-163">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="140e4-164">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="140e4-164">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

