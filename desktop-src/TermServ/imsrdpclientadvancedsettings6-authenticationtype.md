---
title: Proprietà AuthenticationType IMsRdpClientAdvancedSettings6
description: Specifica il tipo di autenticazione utilizzato per la connessione.
ms.assetid: A6DAAE0A-5045-4C2C-B065-AB5BFB39F955
ms.tgt_platform: multiple
keywords:
- Proprietà AuthenticationType Servizi Desktop remoto
- Proprietà AuthenticationType Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà AuthenticationType
- Proprietà AuthenticationType Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà AuthenticationType
- Proprietà AuthenticationType Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà AuthenticationType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.AuthenticationType
- IMsRdpClientAdvancedSettings6.get_AuthenticationType
- IMsRdpClientAdvancedSettings7.AuthenticationType
- IMsRdpClientAdvancedSettings7.get_AuthenticationType
- IMsRdpClientAdvancedSettings8.AuthenticationType
- IMsRdpClientAdvancedSettings8.get_AuthenticationType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c59239570538b690866e499ee942b6635055c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119778"
---
# <a name="imsrdpclientadvancedsettings6authenticationtype-property"></a><span data-ttu-id="19e82-110">Proprietà IMsRdpClientAdvancedSettings6:: AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="19e82-110">IMsRdpClientAdvancedSettings6::AuthenticationType property</span></span>

<span data-ttu-id="19e82-111">Specifica il tipo di autenticazione utilizzato per la connessione.</span><span class="sxs-lookup"><span data-stu-id="19e82-111">Specifies the type of authentication used for this connection.</span></span>

<span data-ttu-id="19e82-112">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="19e82-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="19e82-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19e82-113">Syntax</span></span>


```C++
HRESULT get_AuthenticationType(
  [out] UINT *puiAuthType
);
```



## <a name="property-value"></a><span data-ttu-id="19e82-114">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="19e82-114">Property value</span></span>

<span data-ttu-id="19e82-115">Riceve un valore che specifica il tipo di autenticazione utilizzato per la connessione.</span><span class="sxs-lookup"><span data-stu-id="19e82-115">Receives a value that specifies the type of authentication used for this connection.</span></span> <span data-ttu-id="19e82-116">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="19e82-116">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="19e82-117">0</span><span class="sxs-lookup"><span data-stu-id="19e82-117">0</span></span>
</dt> <dd>

<span data-ttu-id="19e82-118">Non viene utilizzata alcuna autenticazione.</span><span class="sxs-lookup"><span data-stu-id="19e82-118">No authentication is used.</span></span>

</dd> <dt>

<span data-ttu-id="19e82-119">1</span><span class="sxs-lookup"><span data-stu-id="19e82-119">1</span></span>
</dt> <dd>

<span data-ttu-id="19e82-120">Viene utilizzata l'autenticazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="19e82-120">Certificate authentication is used.</span></span>

</dd> <dt>

<span data-ttu-id="19e82-121">2</span><span class="sxs-lookup"><span data-stu-id="19e82-121">2</span></span>
</dt> <dd>

<span data-ttu-id="19e82-122">Viene utilizzata l'autenticazione Kerberos.</span><span class="sxs-lookup"><span data-stu-id="19e82-122">Kerberos authentication is used.</span></span>

</dd> <dt>

<span data-ttu-id="19e82-123">3</span><span class="sxs-lookup"><span data-stu-id="19e82-123">3</span></span>
</dt> <dd>

<span data-ttu-id="19e82-124">Vengono utilizzati sia il certificato che l'autenticazione Kerberos.</span><span class="sxs-lookup"><span data-stu-id="19e82-124">Both certificate and Kerberos authentication are used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19e82-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19e82-125">Requirements</span></span>



| <span data-ttu-id="19e82-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="19e82-126">Requirement</span></span> | <span data-ttu-id="19e82-127">Valore</span><span class="sxs-lookup"><span data-stu-id="19e82-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19e82-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19e82-128">Minimum supported client</span></span><br/> | <span data-ttu-id="19e82-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19e82-129">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="19e82-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19e82-130">Minimum supported server</span></span><br/> | <span data-ttu-id="19e82-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19e82-131">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="19e82-132">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="19e82-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="19e82-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19e82-133"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="19e82-134">DLL</span><span class="sxs-lookup"><span data-stu-id="19e82-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19e82-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19e82-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="19e82-136">IID</span><span class="sxs-lookup"><span data-stu-id="19e82-136">IID</span></span><br/>                      | <span data-ttu-id="19e82-137">IID \_ IMsRdpClientAdvancedSettings6 è definito come 222c4b5d-45D9-4DF0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="19e82-137">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="19e82-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19e82-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19e82-139">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="19e82-139">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="19e82-140">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="19e82-140">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="19e82-141">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="19e82-141">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





