---
title: Proprietà RedirectClipboard di IMsRdpClientAdvancedSettings5
description: Imposta o recupera la configurazione per il reindirizzamento degli Appunti.
ms.assetid: c653f593-9912-4ade-a0a3-70d9afac2ab1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RedirectClipboard
- Servizi Desktop remoto proprietà RedirectClipboard, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà RedirectClipboard
- Servizi Desktop remoto proprietà RedirectClipboard, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà RedirectClipboard
- Servizi Desktop remoto proprietà RedirectClipboard, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà RedirectClipboard
- Servizi Desktop remoto proprietà RedirectClipboard, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà RedirectClipboard
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectClipboard
- IMsRdpClientAdvancedSettings5.get_RedirectClipboard
- IMsRdpClientAdvancedSettings5.put_RedirectClipboard
- IMsRdpClientAdvancedSettings6.RedirectClipboard
- IMsRdpClientAdvancedSettings6.get_RedirectClipboard
- IMsRdpClientAdvancedSettings6.put_RedirectClipboard
- IMsRdpClientAdvancedSettings7.RedirectClipboard
- IMsRdpClientAdvancedSettings7.get_RedirectClipboard
- IMsRdpClientAdvancedSettings7.put_RedirectClipboard
- IMsRdpClientAdvancedSettings8.RedirectClipboard
- IMsRdpClientAdvancedSettings8.get_RedirectClipboard
- IMsRdpClientAdvancedSettings8.put_RedirectClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aba9950b8d602ca239d66364279a5876a432d04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963971"
---
# <a name="imsrdpclientadvancedsettings5redirectclipboard-property"></a><span data-ttu-id="13fdc-112">Proprietà IMsRdpClientAdvancedSettings5:: RedirectClipboard</span><span class="sxs-lookup"><span data-stu-id="13fdc-112">IMsRdpClientAdvancedSettings5::RedirectClipboard property</span></span>

<span data-ttu-id="13fdc-113">Imposta o recupera la configurazione per il reindirizzamento degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="13fdc-113">Sets or retrieves the configuration for clipboard redirection.</span></span>

<span data-ttu-id="13fdc-114">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="13fdc-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="13fdc-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13fdc-115">Syntax</span></span>


```C++
HRESULT put_RedirectClipboard(
  [in]  VARIANT_BOOL fRedirectClipboard
);

HRESULT get_RedirectClipboard(
  [out] VARIANT_BOOL *pfRedirectClipboard
);
```



## <a name="property-value"></a><span data-ttu-id="13fdc-116">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="13fdc-116">Property value</span></span>

<span data-ttu-id="13fdc-117">Imposta la modalità di reindirizzamento degli appunti su **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="13fdc-117">Sets the clipboard redirection mode to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="13fdc-118">Se impostato su **true**, la modalità di reindirizzamento degli Appunti è abilitata.</span><span class="sxs-lookup"><span data-stu-id="13fdc-118">If set to **TRUE**, clipboard redirection mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="13fdc-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13fdc-119">Requirements</span></span>



| <span data-ttu-id="13fdc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="13fdc-120">Requirement</span></span> | <span data-ttu-id="13fdc-121">Valore</span><span class="sxs-lookup"><span data-stu-id="13fdc-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13fdc-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13fdc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="13fdc-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13fdc-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="13fdc-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13fdc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="13fdc-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13fdc-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="13fdc-126">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="13fdc-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="13fdc-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13fdc-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="13fdc-128">DLL</span><span class="sxs-lookup"><span data-stu-id="13fdc-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13fdc-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13fdc-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="13fdc-130">IID</span><span class="sxs-lookup"><span data-stu-id="13fdc-130">IID</span></span><br/>                      | <span data-ttu-id="13fdc-131">IID \_ IMsRdpClientAdvancedSettings5 è definito come FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="13fdc-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="13fdc-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13fdc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13fdc-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="13fdc-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="13fdc-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="13fdc-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="13fdc-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="13fdc-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="13fdc-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="13fdc-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





