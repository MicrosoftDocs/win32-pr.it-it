---
title: Proprietà PublicMode di IMsRdpClientAdvancedSettings5
description: Imposta o recupera la configurazione per la modalità pubblica. La modalità pubblica impedisce al client di memorizzare nella cache i dati utente nel sistema locale.
ms.assetid: dff6121a-b69c-411f-832b-29f9609f4230
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà PublicMode
- Servizi Desktop remoto proprietà PublicMode, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà PublicMode
- Servizi Desktop remoto proprietà PublicMode, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà PublicMode
- Servizi Desktop remoto proprietà PublicMode, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà PublicMode
- Servizi Desktop remoto proprietà PublicMode, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà PublicMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.PublicMode
- IMsRdpClientAdvancedSettings5.get_PublicMode
- IMsRdpClientAdvancedSettings5.put_PublicMode
- IMsRdpClientAdvancedSettings6.PublicMode
- IMsRdpClientAdvancedSettings6.get_PublicMode
- IMsRdpClientAdvancedSettings6.put_PublicMode
- IMsRdpClientAdvancedSettings7.PublicMode
- IMsRdpClientAdvancedSettings7.get_PublicMode
- IMsRdpClientAdvancedSettings7.put_PublicMode
- IMsRdpClientAdvancedSettings8.PublicMode
- IMsRdpClientAdvancedSettings8.get_PublicMode
- IMsRdpClientAdvancedSettings8.put_PublicMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9173b7685e77984a28d65129c79c9d1a09cf1458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301304"
---
# <a name="imsrdpclientadvancedsettings5publicmode-property"></a><span data-ttu-id="fc6c2-113">IMsRdpClientAdvancedSettings5::P proprietà ublicMode</span><span class="sxs-lookup"><span data-stu-id="fc6c2-113">IMsRdpClientAdvancedSettings5::PublicMode property</span></span>

<span data-ttu-id="fc6c2-114">Imposta o recupera la configurazione per la modalità pubblica.</span><span class="sxs-lookup"><span data-stu-id="fc6c2-114">Sets or retrieves the configuration for public mode.</span></span> <span data-ttu-id="fc6c2-115">La modalità pubblica impedisce al client di memorizzare nella cache i dati utente nel sistema locale.</span><span class="sxs-lookup"><span data-stu-id="fc6c2-115">Public mode prevents the client from caching user data to the local system.</span></span>

<span data-ttu-id="fc6c2-116">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="fc6c2-116">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc6c2-117">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc6c2-117">Syntax</span></span>


```C++
HRESULT put_PublicMode(
  [in]  VARIANT_BOOL fPublicMode
);

HRESULT get_PublicMode(
  [out] VARIANT_BOOL *pfPublicMode
);
```



## <a name="property-value"></a><span data-ttu-id="fc6c2-118">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fc6c2-118">Property value</span></span>

<span data-ttu-id="fc6c2-119">Imposta l'impostazione della modalità pubblica su **Variant \_ true** o **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="fc6c2-119">Sets the public mode setting to **VARIANT\_TRUE** or **VARIANT\_FALSE**.</span></span> <span data-ttu-id="fc6c2-120">Se impostato su **Variant \_ true**, l'impostazione della modalità pubblica è abilitata.</span><span class="sxs-lookup"><span data-stu-id="fc6c2-120">If set to **VARIANT\_TRUE**, the public mode setting is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc6c2-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc6c2-121">Requirements</span></span>



| <span data-ttu-id="fc6c2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc6c2-122">Requirement</span></span> | <span data-ttu-id="fc6c2-123">Valore</span><span class="sxs-lookup"><span data-stu-id="fc6c2-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc6c2-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc6c2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fc6c2-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc6c2-125">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="fc6c2-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc6c2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fc6c2-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc6c2-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="fc6c2-128">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="fc6c2-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="fc6c2-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc6c2-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="fc6c2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="fc6c2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc6c2-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc6c2-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="fc6c2-132">IID</span><span class="sxs-lookup"><span data-stu-id="fc6c2-132">IID</span></span><br/>                      | <span data-ttu-id="fc6c2-133">IID \_ IMsRdpClientAdvancedSettings5 è definito come FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="fc6c2-133">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fc6c2-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc6c2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc6c2-135">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="fc6c2-135">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="fc6c2-136">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="fc6c2-136">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="fc6c2-137">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="fc6c2-137">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="fc6c2-138">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="fc6c2-138">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





