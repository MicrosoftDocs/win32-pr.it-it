---
title: Proprietà ConnectToAdministerServer di IMsRdpClientAdvancedSettings6
description: Recupera o specifica se il controllo ActiveX deve tentare di connettersi al server per scopi amministrativi.
ms.assetid: b98f9b9b-a3e7-4a3c-a7e3-e388ce53c5c9
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ConnectToAdministerServer
- Servizi Desktop remoto proprietà ConnectToAdministerServer, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà ConnectToAdministerServer
- Servizi Desktop remoto proprietà ConnectToAdministerServer, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà ConnectToAdministerServer
- Servizi Desktop remoto proprietà ConnectToAdministerServer, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà ConnectToAdministerServer
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.put_ConnectToAdministerServer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9cad8d50e2e0a4c1ec18fbd33733dc394101a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048370"
---
# <a name="imsrdpclientadvancedsettings6connecttoadministerserver-property"></a><span data-ttu-id="891ac-110">Proprietà IMsRdpClientAdvancedSettings6:: ConnectToAdministerServer</span><span class="sxs-lookup"><span data-stu-id="891ac-110">IMsRdpClientAdvancedSettings6::ConnectToAdministerServer property</span></span>

<span data-ttu-id="891ac-111">Recupera o specifica se il controllo ActiveX deve tentare di connettersi al server per scopi amministrativi.</span><span class="sxs-lookup"><span data-stu-id="891ac-111">Retrieves or specifies whether the ActiveX control should attempt to connect to the server for administrative purposes.</span></span>

<span data-ttu-id="891ac-112">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="891ac-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="891ac-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="891ac-113">Syntax</span></span>


```C++
HRESULT put_ConnectToAdministerServer(
  [in]  VARIANT_BOOL connectToAdministerServer
);

HRESULT get_ConnectToAdministerServer(
  [out] VARIANT_BOOL *pConnectToAdministerServer
);
```



## <a name="property-value"></a><span data-ttu-id="891ac-114">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="891ac-114">Property value</span></span>

<span data-ttu-id="891ac-115">**Variante \_ TRUE** per fare in modo che il controllo ActiveX tenti di connettersi al server per scopi amministrativi. in caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="891ac-115">**VARIANT\_TRUE** to cause the ActiveX control to attempt to connect to the server for administrative purposes; otherwise **VARIANT\_FALSE**.</span></span> <span data-ttu-id="891ac-116">Il valore predefinito è **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="891ac-116">The default value is **VARIANT\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="891ac-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="891ac-117">Remarks</span></span>

<span data-ttu-id="891ac-118">Per utilizzare **ConnectToAdministerServer**, è necessario eseguire Connessione desktop remoto (RDC) client versione 6,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="891ac-118">To use **ConnectToAdministerServer**, you must be running Remote Desktop Connection (RDC) client version 6.1 or later.</span></span>

> [!Note]  
> <span data-ttu-id="891ac-119">La versione RDC 6,1 (6.0.6001) supporta Remote Desktop Protocol 6,1.</span><span class="sxs-lookup"><span data-stu-id="891ac-119">RDC version 6.1 (6.0.6001) supports Remote Desktop Protocol 6.1.</span></span> <span data-ttu-id="891ac-120">RDC 6,1 è incluso in Windows Server 2008 e Windows Vista con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="891ac-120">RDC 6.1 is included with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

 

<span data-ttu-id="891ac-121">**ConnectToAdministerServer** consente di connettersi a una sessione di utilizzata a scopo amministrativo sul server remoto.</span><span class="sxs-lookup"><span data-stu-id="891ac-121">**ConnectToAdministerServer** connects you to a session that is used for administrative purposes on the remote server.</span></span> <span data-ttu-id="891ac-122">Se il servizio ruolo host sessione Desktop remoto (host sessione Desktop remoto) è installato nel server remoto, **ConnectToAdministerServer** esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="891ac-122">If the Remote Desktop Session Host (RD Session Host) role service is installed on the remote server, **ConnectToAdministerServer** does the following:</span></span>

-   <span data-ttu-id="891ac-123">Disabilita Servizi Desktop remoto licenze di accesso client per la sessione.</span><span class="sxs-lookup"><span data-stu-id="891ac-123">Disables Remote Desktop Services client access licensing for the session.</span></span>
-   <span data-ttu-id="891ac-124">Disabilita il reindirizzamento del fuso orario per la sessione.</span><span class="sxs-lookup"><span data-stu-id="891ac-124">Disables time zone redirection for the session.</span></span>
-   <span data-ttu-id="891ac-125">Disabilita il reindirizzamento di Connessione Desktop remoto broker (gestore connessione Desktop remoto) per la sessione.</span><span class="sxs-lookup"><span data-stu-id="891ac-125">Disables Remote Desktop Connection Broker (RD Connection Broker) redirection for the session.</span></span>
-   <span data-ttu-id="891ac-126">Disabilita il reindirizzamento del dispositivo Plug and Play per la sessione.</span><span class="sxs-lookup"><span data-stu-id="891ac-126">Disables Plug and Play device redirection for the session.</span></span>
-   <span data-ttu-id="891ac-127">Consente di modificare il tema della sessione remota in Windows classico per la sessione.</span><span class="sxs-lookup"><span data-stu-id="891ac-127">Changes the remote session theme to Windows Classic for the session.</span></span>

## <a name="requirements"></a><span data-ttu-id="891ac-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="891ac-128">Requirements</span></span>



| <span data-ttu-id="891ac-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="891ac-129">Requirement</span></span> | <span data-ttu-id="891ac-130">Valore</span><span class="sxs-lookup"><span data-stu-id="891ac-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="891ac-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="891ac-131">Minimum supported client</span></span><br/> | <span data-ttu-id="891ac-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="891ac-132">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="891ac-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="891ac-133">Minimum supported server</span></span><br/> | <span data-ttu-id="891ac-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="891ac-134">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="891ac-135">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="891ac-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="891ac-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="891ac-136"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="891ac-137">DLL</span><span class="sxs-lookup"><span data-stu-id="891ac-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="891ac-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="891ac-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="891ac-139">IID</span><span class="sxs-lookup"><span data-stu-id="891ac-139">IID</span></span><br/>                      | <span data-ttu-id="891ac-140">IID \_ IMsRdpClientAdvancedSettings6 è definito come 222c4b5d-45D9-4DF0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="891ac-140">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="891ac-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="891ac-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="891ac-142">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="891ac-142">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="891ac-143">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="891ac-143">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="891ac-144">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="891ac-144">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





