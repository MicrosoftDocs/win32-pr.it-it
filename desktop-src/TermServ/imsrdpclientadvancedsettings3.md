---
title: Interfaccia IMsRdpClientAdvancedSettings3
description: Gestisce le impostazioni client avanzate. Deriva dall'interfaccia IMsRdpClientAdvancedSettings2.
ms.assetid: bfa9cf74-5943-45ca-9259-3ef0cc9ab2ab
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 760ae7d40742a800556b3d62bc5a1609b89c986b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741346"
---
# <a name="imsrdpclientadvancedsettings3-interface"></a><span data-ttu-id="c1791-106">Interfaccia IMsRdpClientAdvancedSettings3</span><span class="sxs-lookup"><span data-stu-id="c1791-106">IMsRdpClientAdvancedSettings3 interface</span></span>

<span data-ttu-id="c1791-107">Gestisce le impostazioni client avanzate.</span><span class="sxs-lookup"><span data-stu-id="c1791-107">Manages advanced client settings.</span></span> <span data-ttu-id="c1791-108">Deriva dall'interfaccia [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="c1791-108">Derives from the [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) interface.</span></span> <span data-ttu-id="c1791-109">Questa interfaccia include metodi per recuperare e impostare proprietà avanzate (facoltative) per il controllo ActiveX Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="c1791-109">This interface includes methods to retrieve and set advanced (optional) properties for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="c1791-110">Per ottenere un'istanza di questa interfaccia, usare la proprietà [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) per ottenere un puntatore a interfaccia [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="c1791-110">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="c1791-111">Chiamare quindi [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul puntatore **IMsTscAdvancedSettings** e passare **IID \_ IMsRdpClientAdvancedSettings3** a **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="c1791-111">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings3** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="c1791-112">Membri</span><span class="sxs-lookup"><span data-stu-id="c1791-112">Members</span></span>

<span data-ttu-id="c1791-113">L'interfaccia **IMsRdpClientAdvancedSettings3** eredita da [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md).</span><span class="sxs-lookup"><span data-stu-id="c1791-113">The **IMsRdpClientAdvancedSettings3** interface inherits from [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md).</span></span> <span data-ttu-id="c1791-114">**IMsRdpClientAdvancedSettings3** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c1791-114">**IMsRdpClientAdvancedSettings3** also has these types of members:</span></span>

-   [<span data-ttu-id="c1791-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c1791-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c1791-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c1791-116">Properties</span></span>

<span data-ttu-id="c1791-117">L'interfaccia **IMsRdpClientAdvancedSettings3** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c1791-117">The **IMsRdpClientAdvancedSettings3** interface has these properties.</span></span>



| <span data-ttu-id="c1791-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c1791-118">Property</span></span>                                                                                                            | <span data-ttu-id="c1791-119">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="c1791-119">Access type</span></span>           | <span data-ttu-id="c1791-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1791-120">Description</span></span>                                                                            |
|:--------------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1791-121">**ConnectionBarShowMinimizeButton**</span><span class="sxs-lookup"><span data-stu-id="c1791-121">**ConnectionBarShowMinimizeButton**</span></span>](imsrdpclientadvancedsettings3-connectionbarshowminimizebutton.md)<br/> | <span data-ttu-id="c1791-122">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="c1791-122">Read/write</span></span><br/> | <span data-ttu-id="c1791-123">Specifica se visualizzare il pulsante **Riduci a icona** sulla barra delle connessioni.</span><span class="sxs-lookup"><span data-stu-id="c1791-123">Specifies whether to display the **Minimize** button on the connection bar.</span></span><br/> |
| [<span data-ttu-id="c1791-124">**ConnectionBarShowRestoreButton**</span><span class="sxs-lookup"><span data-stu-id="c1791-124">**ConnectionBarShowRestoreButton**</span></span>](imsrdpclientadvancedsettings3-connectionbarshowrestorebutton.md)<br/>   | <span data-ttu-id="c1791-125">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="c1791-125">Read/write</span></span><br/> | <span data-ttu-id="c1791-126">Specifica se visualizzare il pulsante **Ripristina** sulla barra delle connessioni.</span><span class="sxs-lookup"><span data-stu-id="c1791-126">Specifies whether to display the **Restore** button on the connection bar.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="c1791-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1791-127">Remarks</span></span>

<span data-ttu-id="c1791-128">Questa interfaccia è stata estesa dalle interfacce seguenti, in cui ogni nuova interfaccia eredita tutti i metodi e le proprietà delle interfacce precedenti:</span><span class="sxs-lookup"><span data-stu-id="c1791-128">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="c1791-129">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="c1791-129">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
-   [<span data-ttu-id="c1791-130">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c1791-130">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="c1791-131">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="c1791-131">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="c1791-132">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="c1791-132">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
-   [<span data-ttu-id="c1791-133">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="c1791-133">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)

<span data-ttu-id="c1791-134">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c1791-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1791-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1791-135">Requirements</span></span>



| <span data-ttu-id="c1791-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1791-136">Requirement</span></span> | <span data-ttu-id="c1791-137">Valore</span><span class="sxs-lookup"><span data-stu-id="c1791-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1791-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1791-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c1791-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1791-139">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="c1791-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1791-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c1791-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1791-141">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="c1791-142">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c1791-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="c1791-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1791-143"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c1791-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c1791-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1791-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1791-145"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c1791-146">IID</span><span class="sxs-lookup"><span data-stu-id="c1791-146">IID</span></span><br/>                      | <span data-ttu-id="c1791-147">IID \_ IMsRdpClientAdvancedSettings3 è definito come 19cd856b-C542-4c53-Acee-f127e3be1a59</span><span class="sxs-lookup"><span data-stu-id="c1791-147">IID\_IMsRdpClientAdvancedSettings3 is defined as 19cd856b-c542-4c53-acee-f127e3be1a59</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1791-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1791-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1791-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="c1791-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="c1791-150">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="c1791-150">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="c1791-151">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="c1791-151">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="c1791-152">Riferimento Connessione Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="c1791-152">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

