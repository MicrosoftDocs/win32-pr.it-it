---
title: Proprietà ConnectionBarShowPinButton di IMsRdpClientAdvancedSettings5
description: Imposta o recupera la configurazione per il pulsante Aggiungi nella barra delle connessioni.
ms.assetid: fbb2c19b-88a7-435b-86ef-4856e194b383
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ConnectionBarShowPinButton
- Servizi Desktop remoto proprietà ConnectionBarShowPinButton, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà ConnectionBarShowPinButton
- Servizi Desktop remoto proprietà ConnectionBarShowPinButton, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà ConnectionBarShowPinButton
- Servizi Desktop remoto proprietà ConnectionBarShowPinButton, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà ConnectionBarShowPinButton
- Servizi Desktop remoto proprietà ConnectionBarShowPinButton, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà ConnectionBarShowPinButton
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowPinButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a766bc01bc5bf773fa03e788c3089441e6c3f6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301307"
---
# <a name="imsrdpclientadvancedsettings5connectionbarshowpinbutton-property"></a><span data-ttu-id="442e5-112">Proprietà IMsRdpClientAdvancedSettings5:: ConnectionBarShowPinButton</span><span class="sxs-lookup"><span data-stu-id="442e5-112">IMsRdpClientAdvancedSettings5::ConnectionBarShowPinButton property</span></span>

<span data-ttu-id="442e5-113">Imposta o recupera la configurazione per il pulsante Aggiungi nella barra delle connessioni.</span><span class="sxs-lookup"><span data-stu-id="442e5-113">Sets or retrieves the configuration for the pin button in the connection bar.</span></span>

<span data-ttu-id="442e5-114">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="442e5-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="442e5-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="442e5-115">Syntax</span></span>


```C++
HRESULT put_ConnectionBarShowPinButton(
  [in]  VARIANT_BOOL fShowPin
);

HRESULT get_ConnectionBarShowPinButton(
  [out] VARIANT_BOOL *pfShowPin
);
```



## <a name="property-value"></a><span data-ttu-id="442e5-116">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="442e5-116">Property value</span></span>

<span data-ttu-id="442e5-117">Valore booleano **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="442e5-117">A Boolean value of **TRUE** or **FALSE**.</span></span> <span data-ttu-id="442e5-118">Il valore **true** indica il pulsante Aggiungi nella barra delle connessioni.</span><span class="sxs-lookup"><span data-stu-id="442e5-118">A value of **TRUE** shows the pin button in the connection bar.</span></span> <span data-ttu-id="442e5-119">Il valore **false** nasconde il pulsante Aggiungi nella barra delle connessioni.</span><span class="sxs-lookup"><span data-stu-id="442e5-119">A value of **FALSE** hides the pin button in the connection bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="442e5-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="442e5-120">Requirements</span></span>



| <span data-ttu-id="442e5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="442e5-121">Requirement</span></span> | <span data-ttu-id="442e5-122">Valore</span><span class="sxs-lookup"><span data-stu-id="442e5-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="442e5-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="442e5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="442e5-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="442e5-124">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="442e5-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="442e5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="442e5-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="442e5-126">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="442e5-127">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="442e5-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="442e5-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="442e5-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="442e5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="442e5-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="442e5-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="442e5-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="442e5-131">IID</span><span class="sxs-lookup"><span data-stu-id="442e5-131">IID</span></span><br/>                      | <span data-ttu-id="442e5-132">IID \_ IMsRdpClientAdvancedSettings5 è definito come FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="442e5-132">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="442e5-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="442e5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="442e5-134">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="442e5-134">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="442e5-135">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="442e5-135">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="442e5-136">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="442e5-136">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="442e5-137">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="442e5-137">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





