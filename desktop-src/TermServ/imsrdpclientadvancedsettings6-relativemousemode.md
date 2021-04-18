---
title: Proprietà RelativeMouseMode di IMsRdpClientAdvancedSettings6
description: Specifica se il mouse deve utilizzare la modalità relativa.
ms.assetid: 29ae9575-ce60-4999-9601-18413ae739e6
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RelativeMouseMode
- Servizi Desktop remoto proprietà RelativeMouseMode, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà RelativeMouseMode
- Servizi Desktop remoto proprietà RelativeMouseMode, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà RelativeMouseMode
- Servizi Desktop remoto proprietà RelativeMouseMode, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà RelativeMouseMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.RelativeMouseMode
- IMsRdpClientAdvancedSettings6.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings6.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.RelativeMouseMode
- IMsRdpClientAdvancedSettings7.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.RelativeMouseMode
- IMsRdpClientAdvancedSettings8.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.put_RelativeMouseMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31c575acefbfef54dc4c858f465f0cdde2ce8bc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301895"
---
# <a name="imsrdpclientadvancedsettings6relativemousemode-property"></a><span data-ttu-id="bd7db-110">Proprietà IMsRdpClientAdvancedSettings6:: RelativeMouseMode</span><span class="sxs-lookup"><span data-stu-id="bd7db-110">IMsRdpClientAdvancedSettings6::RelativeMouseMode property</span></span>

<span data-ttu-id="bd7db-111">Specifica se il mouse deve utilizzare la modalità relativa.</span><span class="sxs-lookup"><span data-stu-id="bd7db-111">Specifies whether the mouse should use relative mode.</span></span> <span data-ttu-id="bd7db-112">Contiene la **variante \_ true** se il mouse è in modalità relativa o **Variant \_ false** se il mouse è in modalità Absolute.</span><span class="sxs-lookup"><span data-stu-id="bd7db-112">Contains **VARIANT\_TRUE** if the mouse is in relative mode or **VARIANT\_FALSE** if the mouse is in absolute mode.</span></span>

<span data-ttu-id="bd7db-113">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="bd7db-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd7db-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd7db-114">Syntax</span></span>


```C++
HRESULT put_RelativeMouseMode(
  [in]          VARIANT_BOOL fRelativeMouseMode
);

HRESULT get_RelativeMouseMode(
  [out, retval] VARIANT_BOOL *pfRelativeMouseMode
);
```



## <a name="property-value"></a><span data-ttu-id="bd7db-115">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bd7db-115">Property value</span></span>

<span data-ttu-id="bd7db-116">Contiene il nuovo valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="bd7db-116">Contains the new property value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd7db-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd7db-117">Remarks</span></span>

<span data-ttu-id="bd7db-118">La modalità mouse indica il modo in cui il controllo ActiveX calcola le coordinate del mouse inviate al server host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="bd7db-118">The mouse mode indicates how the ActiveX control calculates the mouse coordinates that it sends to the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="bd7db-119">Quando il mouse è in modalità relativa, il controllo ActiveX calcola le coordinate del mouse in relazione all'ultima posizione del mouse.</span><span class="sxs-lookup"><span data-stu-id="bd7db-119">When the mouse is in relative mode, the ActiveX control calculates mouse coordinates relative to the mouse's last position.</span></span> <span data-ttu-id="bd7db-120">Quando il mouse è in modalità assoluta, il controllo ActiveX calcola le coordinate del mouse relative al desktop del server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="bd7db-120">When the mouse is in absolute mode, the ActiveX control calculates mouse coordinates relative to the desktop of the RD Session Host server.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd7db-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd7db-121">Requirements</span></span>



| <span data-ttu-id="bd7db-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd7db-122">Requirement</span></span> | <span data-ttu-id="bd7db-123">Valore</span><span class="sxs-lookup"><span data-stu-id="bd7db-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd7db-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd7db-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bd7db-125">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="bd7db-125">Windows Vista with SP1</span></span><br/>                                                                |
| <span data-ttu-id="bd7db-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd7db-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bd7db-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd7db-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="bd7db-128">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="bd7db-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="bd7db-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd7db-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="bd7db-130">DLL</span><span class="sxs-lookup"><span data-stu-id="bd7db-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd7db-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd7db-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="bd7db-132">IID</span><span class="sxs-lookup"><span data-stu-id="bd7db-132">IID</span></span><br/>                      | <span data-ttu-id="bd7db-133">IID \_ IMsRdpClientAdvancedSettings6 è definito come 222c4b5d-45D9-4DF0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="bd7db-133">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bd7db-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd7db-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd7db-135">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="bd7db-135">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="bd7db-136">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="bd7db-136">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="bd7db-137">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="bd7db-137">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





