---
title: Interfaccia IMsRdpClientAdvancedSettings4
description: Gestisce le impostazioni client avanzate. Deriva dall'interfaccia IMsRdpClientAdvancedSettings3.
ms.assetid: cb1785d6-1f94-4423-bdda-0e3e4e9b8641
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d840206a139e3c3272551eab6a187a7b18416e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400589"
---
# <a name="imsrdpclientadvancedsettings4-interface"></a><span data-ttu-id="0f3f6-106">Interfaccia IMsRdpClientAdvancedSettings4</span><span class="sxs-lookup"><span data-stu-id="0f3f6-106">IMsRdpClientAdvancedSettings4 interface</span></span>

<span data-ttu-id="0f3f6-107">Gestisce le impostazioni client avanzate.</span><span class="sxs-lookup"><span data-stu-id="0f3f6-107">Manages advanced client settings.</span></span> <span data-ttu-id="0f3f6-108">Deriva dall'interfaccia [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) .</span><span class="sxs-lookup"><span data-stu-id="0f3f6-108">Derives from the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.</span></span> <span data-ttu-id="0f3f6-109">Questa interfaccia include metodi per recuperare e impostare proprietà avanzate (facoltative) per il controllo ActiveX Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0f3f6-109">This interface includes methods to retrieve and set advanced (optional) properties for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="0f3f6-110">Per ottenere un'istanza di questa interfaccia, usare la proprietà [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) per ottenere un puntatore a interfaccia [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="0f3f6-110">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="0f3f6-111">Chiamare quindi [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul puntatore **IMsTscAdvancedSettings** e passare **IID \_ IMsRdpClientAdvancedSettings4** a **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="0f3f6-111">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings4** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="0f3f6-112">Membri</span><span class="sxs-lookup"><span data-stu-id="0f3f6-112">Members</span></span>

<span data-ttu-id="0f3f6-113">L'interfaccia **IMsRdpClientAdvancedSettings4** eredita da [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md).</span><span class="sxs-lookup"><span data-stu-id="0f3f6-113">The **IMsRdpClientAdvancedSettings4** interface inherits from [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md).</span></span> <span data-ttu-id="0f3f6-114">**IMsRdpClientAdvancedSettings4** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0f3f6-114">**IMsRdpClientAdvancedSettings4** also has these types of members:</span></span>

-   [<span data-ttu-id="0f3f6-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0f3f6-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0f3f6-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0f3f6-116">Properties</span></span>

<span data-ttu-id="0f3f6-117">L'interfaccia **IMsRdpClientAdvancedSettings4** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0f3f6-117">The **IMsRdpClientAdvancedSettings4** interface has these properties.</span></span>



| <span data-ttu-id="0f3f6-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0f3f6-118">Property</span></span>                                                                                    | <span data-ttu-id="0f3f6-119">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="0f3f6-119">Access type</span></span>           | <span data-ttu-id="0f3f6-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f3f6-120">Description</span></span>                                                              |
|:--------------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="0f3f6-121">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="0f3f6-121">**AuthenticationLevel**</span></span>](imsrdpclientadvancedsettings4-authenticationlevel.md)<br/> | <span data-ttu-id="0f3f6-122">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="0f3f6-122">Read/write</span></span><br/> | <span data-ttu-id="0f3f6-123">Specifica il livello di autenticazione da utilizzare per la connessione.</span><span class="sxs-lookup"><span data-stu-id="0f3f6-123">Specifies the authentication level to use for the connection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0f3f6-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f3f6-124">Remarks</span></span>

<span data-ttu-id="0f3f6-125">Questa interfaccia è stata estesa dalle interfacce seguenti, in cui ogni nuova interfaccia eredita tutti i metodi e le proprietà delle interfacce precedenti:</span><span class="sxs-lookup"><span data-stu-id="0f3f6-125">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="0f3f6-126">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="0f3f6-126">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="0f3f6-127">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="0f3f6-127">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="0f3f6-128">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="0f3f6-128">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)

<span data-ttu-id="0f3f6-129">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0f3f6-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f3f6-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f3f6-130">Requirements</span></span>



| <span data-ttu-id="0f3f6-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f3f6-131">Requirement</span></span> | <span data-ttu-id="0f3f6-132">Valore</span><span class="sxs-lookup"><span data-stu-id="0f3f6-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f3f6-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f3f6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0f3f6-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f3f6-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="0f3f6-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f3f6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0f3f6-136">Windows Server 2008, Windows Server 2008 con SP1</span><span class="sxs-lookup"><span data-stu-id="0f3f6-136">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                                     |
| <span data-ttu-id="0f3f6-137">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0f3f6-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="0f3f6-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f3f6-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="0f3f6-139">DLL</span><span class="sxs-lookup"><span data-stu-id="0f3f6-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f3f6-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f3f6-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="0f3f6-141">IID</span><span class="sxs-lookup"><span data-stu-id="0f3f6-141">IID</span></span><br/>                      | <span data-ttu-id="0f3f6-142">IID \_ IMsRdpClientAdvancedSettings4 è definito come FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span><span class="sxs-lookup"><span data-stu-id="0f3f6-142">IID\_IMsRdpClientAdvancedSettings4 is defined as FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0f3f6-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f3f6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f3f6-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="0f3f6-144">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="0f3f6-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="0f3f6-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="0f3f6-146">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="0f3f6-146">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="0f3f6-147">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="0f3f6-147">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="0f3f6-148">Riferimento Connessione Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="0f3f6-148">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

