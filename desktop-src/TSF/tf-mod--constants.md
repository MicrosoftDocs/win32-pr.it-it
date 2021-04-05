---
title: Costanti TF_MOD_ (msctf. h)
description: Le \_ costanti TF mod \_ \ specificano i modificatori di chiave nella \_ struttura TF PRESERVEDKEY.
ms.assetid: 4642ef17-34bd-4482-a9e9-0fbed7b574b1
topic_type:
- apiref
api_name:
- TF_MOD_ALT
- TF_MOD_CONTROL
- TF_MOD_SHIFT
- TF_MOD_RALT
- TF_MOD_RCONTROL
- TF_MOD_RSHIFT
- TF_MOD_LALT
- TF_MOD_LCONTROL
- TF_MOD_LSHIFT
- TF_MOD_ON_KEYUP
- TF_MOD_IGNORE_ALL_MODIFIER
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e67e081d9a0f8714410861c7c36f9f751bad8d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048325"
---
# <a name="tf_mod_-constants"></a><span data-ttu-id="5954d-103">\_Costanti TF mod \_ \*</span><span class="sxs-lookup"><span data-stu-id="5954d-103">TF\_MOD\_\* Constants</span></span>

<span data-ttu-id="5954d-104">Le \_ costanti TF mod \_ \* specificano i modificatori di chiave nella struttura [tf \_ PRESERVEDKEY](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey) .</span><span class="sxs-lookup"><span data-stu-id="5954d-104">The TF\_MOD\_\* constants specify key modifiers in the [TF\_PRESERVEDKEY](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey) structure.</span></span>



| <span data-ttu-id="5954d-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="5954d-105">Constant/value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="5954d-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5954d-106">Description</span></span>                                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MOD_ALT"></span><span id="tf_mod_alt"></span><dl> <span data-ttu-id="5954d-107"><dt>**Tf \_ MOD \_ ALT**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="5954d-107"><dt>**TF\_MOD\_ALT**</dt> <dt>0x0001</dt></span></span> </dl>                                                   | <span data-ttu-id="5954d-108">Viene premuto uno dei tasti ALT</span><span class="sxs-lookup"><span data-stu-id="5954d-108">Either of the ALT keys is pressed</span></span><br/>                                                                                                                                         |
| <span id="TF_MOD_CONTROL"></span><span id="tf_mod_control"></span><dl> <span data-ttu-id="5954d-109"><dt>**Tf \_ \_Controllo mod**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="5954d-109"><dt>**TF\_MOD\_CONTROL**</dt> <dt>0x0002</dt></span></span> </dl>                                       | <span data-ttu-id="5954d-110">Viene premuto uno dei tasti CTRL</span><span class="sxs-lookup"><span data-stu-id="5954d-110">Either of the CTRL keys is pressed</span></span><br/>                                                                                                                                        |
| <span id="TF_MOD_SHIFT"></span><span id="tf_mod_shift"></span><dl> <span data-ttu-id="5954d-111"><dt>**Tf \_ MOD \_ Shift**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="5954d-111"><dt>**TF\_MOD\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>                                             | <span data-ttu-id="5954d-112">Viene premuto uno dei tasti MAIUSC</span><span class="sxs-lookup"><span data-stu-id="5954d-112">Either of the SHIFT keys is pressed</span></span><br/>                                                                                                                                       |
| <span id="TF_MOD_RALT"></span><span id="tf_mod_ralt"></span><dl> <span data-ttu-id="5954d-113"><dt>**Tf \_ MOD \_ Ralt**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="5954d-113"><dt>**TF\_MOD\_RALT**</dt> <dt>0x0008</dt></span></span> </dl>                                                | <span data-ttu-id="5954d-114">Viene premuto il tasto ALT destro</span><span class="sxs-lookup"><span data-stu-id="5954d-114">The right ALT key is pressed</span></span><br/>                                                                                                                                              |
| <span id="TF_MOD_RCONTROL"></span><span id="tf_mod_rcontrol"></span><dl> <span data-ttu-id="5954d-115"><dt>**Tf \_ MOD \_ RCONTROL**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="5954d-115"><dt>**TF\_MOD\_RCONTROL**</dt> <dt>0x0010</dt></span></span> </dl>                                    | <span data-ttu-id="5954d-116">Viene premuto il tasto CTRL destro</span><span class="sxs-lookup"><span data-stu-id="5954d-116">The right CTRL key is pressed</span></span><br/>                                                                                                                                             |
| <span id="TF_MOD_RSHIFT"></span><span id="tf_mod_rshift"></span><dl> <span data-ttu-id="5954d-117"><dt>**Tf \_ MOD \_ RSHIFT**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="5954d-117"><dt>**TF\_MOD\_RSHIFT**</dt> <dt>0x0020</dt></span></span> </dl>                                          | <span data-ttu-id="5954d-118">Viene premuto il tasto MAIUSC destro</span><span class="sxs-lookup"><span data-stu-id="5954d-118">The right SHIFT key is pressed</span></span><br/>                                                                                                                                            |
| <span id="TF_MOD_LALT"></span><span id="tf_mod_lalt"></span><dl> <span data-ttu-id="5954d-119"><dt>**Tf \_ MOD \_ LALT**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="5954d-119"><dt>**TF\_MOD\_LALT**</dt> <dt>0x0040</dt></span></span> </dl>                                                | <span data-ttu-id="5954d-120">Viene premuto il tasto ALT sinistro</span><span class="sxs-lookup"><span data-stu-id="5954d-120">The left ALT key is pressed</span></span><br/>                                                                                                                                               |
| <span id="TF_MOD_LCONTROL"></span><span id="tf_mod_lcontrol"></span><dl> <span data-ttu-id="5954d-121"><dt>**Tf \_ MOD \_ LCONTROL**</dt> <dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="5954d-121"><dt>**TF\_MOD\_LCONTROL**</dt> <dt>0x0080</dt></span></span> </dl>                                    | <span data-ttu-id="5954d-122">Viene premuto il tasto CTRL sinistro</span><span class="sxs-lookup"><span data-stu-id="5954d-122">The left CTRL key is pressed</span></span><br/>                                                                                                                                              |
| <span id="TF_MOD_LSHIFT"></span><span id="tf_mod_lshift"></span><dl> <span data-ttu-id="5954d-123"><dt>**Tf \_ MOD \_ LSHIFT**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="5954d-123"><dt>**TF\_MOD\_LSHIFT**</dt> <dt>0x0100</dt></span></span> </dl>                                          | <span data-ttu-id="5954d-124">Viene premuto il tasto MAIUSC sinistro</span><span class="sxs-lookup"><span data-stu-id="5954d-124">The left SHIFT key is pressed</span></span><br/>                                                                                                                                             |
| <span id="TF_MOD_ON_KEYUP"></span><span id="tf_mod_on_keyup"></span><dl> <span data-ttu-id="5954d-125"><dt>**Tf \_ MOD \_ su \_ KEYUP**</dt> <dt>0x0200</dt></span><span class="sxs-lookup"><span data-stu-id="5954d-125"><dt>**TF\_MOD\_ON\_KEYUP**</dt> <dt>0x0200</dt></span></span> </dl>                                   | <span data-ttu-id="5954d-126">L'evento verrà generato quando la chiave viene rilasciata.</span><span class="sxs-lookup"><span data-stu-id="5954d-126">The event will be fired when the key is released.</span></span> <span data-ttu-id="5954d-127">Senza questo flag, l'evento viene generato quando viene premuto il tasto.</span><span class="sxs-lookup"><span data-stu-id="5954d-127">Without this flag, the event is fired when the key is pressed.</span></span><br/>                                                          |
| <span id="TF_MOD_IGNORE_ALL_MODIFIER"></span><span id="tf_mod_ignore_all_modifier"></span><dl> <span data-ttu-id="5954d-128"><dt>**Tf \_ MOD \_ Ignora \_ tutti i \_ modificatori**</dt> <dt>0x0400</dt></span><span class="sxs-lookup"><span data-stu-id="5954d-128"><dt>**TF\_MOD\_IGNORE\_ALL\_MODIFIER**</dt> <dt>0x0400</dt></span></span> </dl> | <span data-ttu-id="5954d-129">Lo stato dei tasti ALT, CTRL e MAIUSC viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="5954d-129">The state of the ALT, CTRL, and SHIFT keys is ignored.</span></span> <span data-ttu-id="5954d-130">Ciò significa che l'evento verrà generato quando viene premuto il tasto virtuale, indipendentemente dai tasti di modifica.</span><span class="sxs-lookup"><span data-stu-id="5954d-130">This means the event will be fired when the virtual key is pressed, regardless of which modifier keys are pressed.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5954d-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5954d-131">Requirements</span></span>



| <span data-ttu-id="5954d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5954d-132">Requirement</span></span> | <span data-ttu-id="5954d-133">Valore</span><span class="sxs-lookup"><span data-stu-id="5954d-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5954d-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5954d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5954d-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5954d-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5954d-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5954d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5954d-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5954d-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5954d-138">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="5954d-138">Redistributable</span></span><br/>          | <span data-ttu-id="5954d-139">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5954d-139">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="5954d-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5954d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5954d-141"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="5954d-141"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="5954d-142">IDL</span><span class="sxs-lookup"><span data-stu-id="5954d-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5954d-143"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5954d-143"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5954d-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5954d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5954d-145">\_PRESERVEDKEY TF</span><span class="sxs-lookup"><span data-stu-id="5954d-145">TF\_PRESERVEDKEY</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey)
</dt> </dl>

 

 





