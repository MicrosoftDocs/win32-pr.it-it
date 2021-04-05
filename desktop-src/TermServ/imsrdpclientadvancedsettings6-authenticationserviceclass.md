---
title: Proprietà AuthenticationServiceClass di IMsRdpClientAdvancedSettings6
description: Specifica il nome dell'entità servizio (SPN) da utilizzare per l'autenticazione al server.
ms.assetid: 65d10b1f-295a-44b8-a790-306ae4e3e5e2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AuthenticationServiceClass
- Servizi Desktop remoto proprietà AuthenticationServiceClass, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà AuthenticationServiceClass
- Servizi Desktop remoto proprietà AuthenticationServiceClass, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà AuthenticationServiceClass
- Servizi Desktop remoto proprietà AuthenticationServiceClass, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà AuthenticationServiceClass
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings6.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings6.put_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.put_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.put_AuthenticationServiceClass
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 618b55d1489f46e0e1119186bd5003fb68dbfebb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741519"
---
# <a name="imsrdpclientadvancedsettings6authenticationserviceclass-property"></a><span data-ttu-id="94275-110">Proprietà IMsRdpClientAdvancedSettings6:: AuthenticationServiceClass</span><span class="sxs-lookup"><span data-stu-id="94275-110">IMsRdpClientAdvancedSettings6::AuthenticationServiceClass property</span></span>

<span data-ttu-id="94275-111">Specifica il nome dell'entità servizio (SPN) da utilizzare per l'autenticazione al server.</span><span class="sxs-lookup"><span data-stu-id="94275-111">Specifies the service principal name (SPN) to use for authentication to the server.</span></span>

<span data-ttu-id="94275-112">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="94275-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="94275-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94275-113">Syntax</span></span>


```C++
HRESULT put_AuthenticationServiceClass(
  [in]          BSTR bstrAuthServiceClass
);

HRESULT get_AuthenticationServiceClass(
  [out, retval] BSTR *pbstrAuthServiceClass
);
```



## <a name="property-value"></a><span data-ttu-id="94275-114">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="94275-114">Property value</span></span>

<span data-ttu-id="94275-115">Specifica il nome dell'entità servizio da usare.</span><span class="sxs-lookup"><span data-stu-id="94275-115">Specifies the service principal name to use.</span></span>

## <a name="remarks"></a><span data-ttu-id="94275-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="94275-116">Remarks</span></span>

<span data-ttu-id="94275-117">Questa proprietà è supportata solo dai client Connessione Desktop remoto 6,1 e 7,0.</span><span class="sxs-lookup"><span data-stu-id="94275-117">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

<span data-ttu-id="94275-118">I nomi dell'entità servizio (SPN) sono associati all'entità di sicurezza (utente o gruppi) in cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="94275-118">Service principal names (SPNs) are associated with the security principal (user or groups) in whose security context the service executes.</span></span> <span data-ttu-id="94275-119">I nomi SPN vengono utilizzati per supportare l'autenticazione reciproca tra un'applicazione client e un servizio.</span><span class="sxs-lookup"><span data-stu-id="94275-119">SPNs are used to support mutual authentication between a client application and a service.</span></span>

## <a name="requirements"></a><span data-ttu-id="94275-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94275-120">Requirements</span></span>



| <span data-ttu-id="94275-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="94275-121">Requirement</span></span> | <span data-ttu-id="94275-122">Valore</span><span class="sxs-lookup"><span data-stu-id="94275-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94275-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94275-123">Minimum supported client</span></span><br/> | <span data-ttu-id="94275-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94275-124">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="94275-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94275-125">Minimum supported server</span></span><br/> | <span data-ttu-id="94275-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94275-126">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="94275-127">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="94275-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="94275-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94275-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="94275-129">DLL</span><span class="sxs-lookup"><span data-stu-id="94275-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94275-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94275-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="94275-131">IID</span><span class="sxs-lookup"><span data-stu-id="94275-131">IID</span></span><br/>                      | <span data-ttu-id="94275-132">IID \_ IMsRdpClientAdvancedSettings6 è definito come 222c4b5d-45D9-4DF0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="94275-132">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94275-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94275-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94275-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="94275-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="94275-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="94275-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="94275-136">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="94275-136">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





