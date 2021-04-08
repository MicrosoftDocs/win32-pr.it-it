---
title: Proprietà HotKeyFocusReleaseLeft di IMsRdpClientAdvancedSettings6
description: Specifica il codice della chiave virtuale da aggiungere a CTRL + ALT per determinare la sostituzione del tasto di scelta rapida per CTRL + ALT + freccia sinistra.
ms.assetid: 9F2942BD-9F5C-4E02-A330-42C30C6C8F87
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà HotKeyFocusReleaseLeft
- Servizi Desktop remoto proprietà HotKeyFocusReleaseLeft, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà HotKeyFocusReleaseLeft
- Servizi Desktop remoto proprietà HotKeyFocusReleaseLeft, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà HotKeyFocusReleaseLeft
- Servizi Desktop remoto proprietà HotKeyFocusReleaseLeft, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà HotKeyFocusReleaseLeft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings6.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings6.put_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.put_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.put_HotKeyFocusReleaseLeft
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27e0e6d4e334edeffbf0ef025e59454e0f26c34c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740007"
---
# <a name="imsrdpclientadvancedsettings6hotkeyfocusreleaseleft-property"></a><span data-ttu-id="f8c21-110">Proprietà IMsRdpClientAdvancedSettings6:: HotKeyFocusReleaseLeft</span><span class="sxs-lookup"><span data-stu-id="f8c21-110">IMsRdpClientAdvancedSettings6::HotKeyFocusReleaseLeft property</span></span>

<span data-ttu-id="f8c21-111">Specifica il codice della chiave virtuale da aggiungere a CTRL + ALT per determinare la sostituzione del tasto di scelta rapida per CTRL + ALT + freccia sinistra.</span><span class="sxs-lookup"><span data-stu-id="f8c21-111">Specifies the virtual-key code to add to Ctrl+Alt to determine the hotkey replacement for Ctrl+Alt+Left Arrow.</span></span>

<span data-ttu-id="f8c21-112">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f8c21-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8c21-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8c21-113">Syntax</span></span>


```C++
HRESULT put_HotKeyFocusReleaseLeft(
  [in]  LONG hotKeyFocusReleaseLeft
);

HRESULT get_HotKeyFocusReleaseLeft(
  [out] LONG *hotKeyFocusReleaseLeft
);
```



## <a name="property-value"></a><span data-ttu-id="f8c21-114">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f8c21-114">Property value</span></span>

<span data-ttu-id="f8c21-115">Nuovo codice della chiave virtuale.</span><span class="sxs-lookup"><span data-stu-id="f8c21-115">The new virtual-key code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8c21-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8c21-116">Remarks</span></span>

<span data-ttu-id="f8c21-117">Questa proprietà è supportata solo dai client Connessione Desktop remoto 6,1 e 7,0.</span><span class="sxs-lookup"><span data-stu-id="f8c21-117">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8c21-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8c21-118">Requirements</span></span>



| <span data-ttu-id="f8c21-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8c21-119">Requirement</span></span> | <span data-ttu-id="f8c21-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f8c21-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8c21-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8c21-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f8c21-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8c21-122">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="f8c21-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8c21-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f8c21-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8c21-124">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="f8c21-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f8c21-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="f8c21-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8c21-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="f8c21-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f8c21-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8c21-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8c21-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="f8c21-129">IID</span><span class="sxs-lookup"><span data-stu-id="f8c21-129">IID</span></span><br/>                      | <span data-ttu-id="f8c21-130">IID \_ IMsRdpClientAdvancedSettings6 è definito come 222c4b5d-45D9-4DF0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="f8c21-130">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f8c21-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8c21-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8c21-132">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="f8c21-132">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="f8c21-133">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="f8c21-133">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="f8c21-134">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="f8c21-134">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





