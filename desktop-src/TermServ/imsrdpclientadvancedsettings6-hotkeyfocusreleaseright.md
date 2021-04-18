---
title: Proprietà HotKeyFocusReleaseRight di IMsRdpClientAdvancedSettings6
description: Specifica il codice della chiave virtuale da aggiungere a CTRL + ALT per determinare la sostituzione del tasto di scelta rapida per CTRL + ALT + freccia destra.
ms.assetid: 9AEEB712-E4C4-435E-A847-40C2B3A41C15
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà HotKeyFocusReleaseRight
- Servizi Desktop remoto proprietà HotKeyFocusReleaseRight, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà HotKeyFocusReleaseRight
- Servizi Desktop remoto proprietà HotKeyFocusReleaseRight, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà HotKeyFocusReleaseRight
- Servizi Desktop remoto proprietà HotKeyFocusReleaseRight, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà HotKeyFocusReleaseRight
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings6.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings6.put_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.put_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.put_HotKeyFocusReleaseRight
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ce11df170b8b0a0a9a3f58a625955cecb41973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302578"
---
# <a name="imsrdpclientadvancedsettings6hotkeyfocusreleaseright-property"></a><span data-ttu-id="fb720-110">Proprietà IMsRdpClientAdvancedSettings6:: HotKeyFocusReleaseRight</span><span class="sxs-lookup"><span data-stu-id="fb720-110">IMsRdpClientAdvancedSettings6::HotKeyFocusReleaseRight property</span></span>

<span data-ttu-id="fb720-111">Specifica il codice della chiave virtuale da aggiungere a CTRL + ALT per determinare la sostituzione del tasto di scelta rapida per CTRL + ALT + freccia destra.</span><span class="sxs-lookup"><span data-stu-id="fb720-111">Specifies the virtual-key code to add to Ctrl+Alt to determine the hotkey replacement for Ctrl+Alt+Right Arrow.</span></span>

<span data-ttu-id="fb720-112">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="fb720-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb720-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb720-113">Syntax</span></span>


```C++
HRESULT put_HotKeyFocusReleaseRight(
  [in]  LONG hotKeyFocusReleaseRight
);

HRESULT get_HotKeyFocusReleaseRight(
  [out] LONG *hotKeyFocusReleaseRight
);
```



## <a name="property-value"></a><span data-ttu-id="fb720-114">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fb720-114">Property value</span></span>

<span data-ttu-id="fb720-115">Nuovo codice della chiave virtuale.</span><span class="sxs-lookup"><span data-stu-id="fb720-115">The new virtual-key code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb720-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb720-116">Remarks</span></span>

<span data-ttu-id="fb720-117">Questa proprietà è supportata solo dai client Connessione Desktop remoto 6,1 e 7,0.</span><span class="sxs-lookup"><span data-stu-id="fb720-117">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb720-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb720-118">Requirements</span></span>



| <span data-ttu-id="fb720-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb720-119">Requirement</span></span> | <span data-ttu-id="fb720-120">Valore</span><span class="sxs-lookup"><span data-stu-id="fb720-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb720-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb720-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fb720-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb720-122">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="fb720-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb720-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fb720-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb720-124">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="fb720-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="fb720-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="fb720-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb720-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="fb720-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fb720-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb720-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb720-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="fb720-129">IID</span><span class="sxs-lookup"><span data-stu-id="fb720-129">IID</span></span><br/>                      | <span data-ttu-id="fb720-130">IID \_ IMsRdpClientAdvancedSettings6 è definito come 222c4b5d-45D9-4DF0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="fb720-130">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fb720-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb720-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb720-132">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="fb720-132">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="fb720-133">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="fb720-133">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="fb720-134">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="fb720-134">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





