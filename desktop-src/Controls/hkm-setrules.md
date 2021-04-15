---
title: Messaggio HKM_SETRULES (COMmctrl. h)
description: Definisce le combinazioni non valide e la combinazione di modificatore predefinita per un controllo tasto di scelta.
ms.assetid: de3dd463-a534-4c7c-ae04-da80a3bff2ab
keywords:
- Controlli di Windows Message HKM_SETRULES
topic_type:
- apiref
api_name:
- HKM_SETRULES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33c0918a7bb44fdac9a1f2c60fdde8e06b5e679
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477296"
---
# <a name="hkm_setrules-message"></a><span data-ttu-id="479bf-104">\_Messaggio regole di HKM</span><span class="sxs-lookup"><span data-stu-id="479bf-104">HKM\_SETRULES message</span></span>

<span data-ttu-id="479bf-105">Definisce le combinazioni non valide e la combinazione di modificatore predefinita per un controllo tasto di scelta.</span><span class="sxs-lookup"><span data-stu-id="479bf-105">Defines the invalid combinations and the default modifier combination for a hot key control.</span></span>

## <a name="parameters"></a><span data-ttu-id="479bf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="479bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="479bf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="479bf-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="479bf-108">Matrice di flag che specificano combinazioni di chiavi non valide.</span><span class="sxs-lookup"><span data-stu-id="479bf-108">An array of flags that specify invalid key combinations.</span></span> <span data-ttu-id="479bf-109">Questo parametro può essere una combinazione dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="479bf-109">This parameter can be a combination of the following values:</span></span>



| <span data-ttu-id="479bf-110">Valore</span><span class="sxs-lookup"><span data-stu-id="479bf-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="479bf-111">Significato</span><span class="sxs-lookup"><span data-stu-id="479bf-111">Meaning</span></span>                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="HKCOMB_A"></span><span id="hkcomb_a"></span><dl> <span data-ttu-id="479bf-112"><dt>**HKCOMB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="479bf-112"><dt>**HKCOMB\_A**</dt></span></span> </dl>          | <span data-ttu-id="479bf-113">ALT</span><span class="sxs-lookup"><span data-stu-id="479bf-113">ALT</span></span><br/>             |
| <span id="HKCOMB_C"></span><span id="hkcomb_c"></span><dl> <span data-ttu-id="479bf-114"><dt>**HKCOMB \_ C**</dt></span><span class="sxs-lookup"><span data-stu-id="479bf-114"><dt>**HKCOMB\_C**</dt></span></span> </dl>          | <span data-ttu-id="479bf-115">CTRL</span><span class="sxs-lookup"><span data-stu-id="479bf-115">CTRL</span></span><br/>            |
| <span id="HKCOMB_CA"></span><span id="hkcomb_ca"></span><dl> <span data-ttu-id="479bf-116"><dt>**\_CA HKCOMB**</dt></span><span class="sxs-lookup"><span data-stu-id="479bf-116"><dt>**HKCOMB\_CA**</dt></span></span> </dl>       | <span data-ttu-id="479bf-117">CTRL + ALT</span><span class="sxs-lookup"><span data-stu-id="479bf-117">CTRL+ALT</span></span><br/>        |
| <span id="HKCOMB_NONE"></span><span id="hkcomb_none"></span><dl> <span data-ttu-id="479bf-118"><dt>**HKCOMB \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="479bf-118"><dt>**HKCOMB\_NONE**</dt></span></span> </dl> | <span data-ttu-id="479bf-119">Chiavi non modificate</span><span class="sxs-lookup"><span data-stu-id="479bf-119">Unmodified keys</span></span><br/> |
| <span id="HKCOMB_S"></span><span id="hkcomb_s"></span><dl> <span data-ttu-id="479bf-120"><dt>**HKCOMB \_ S**</dt></span><span class="sxs-lookup"><span data-stu-id="479bf-120"><dt>**HKCOMB\_S**</dt></span></span> </dl>          | <span data-ttu-id="479bf-121">MAIUSC</span><span class="sxs-lookup"><span data-stu-id="479bf-121">SHIFT</span></span><br/>           |
| <span id="HKCOMB_SA"></span><span id="hkcomb_sa"></span><dl> <span data-ttu-id="479bf-122"><dt>**\_sa HKCOMB**</dt></span><span class="sxs-lookup"><span data-stu-id="479bf-122"><dt>**HKCOMB\_SA**</dt></span></span> </dl>       | <span data-ttu-id="479bf-123">MAIUSC+ALT</span><span class="sxs-lookup"><span data-stu-id="479bf-123">SHIFT+ALT</span></span><br/>       |
| <span id="HKCOMB_SC"></span><span id="hkcomb_sc"></span><dl> <span data-ttu-id="479bf-124"><dt>**\_SC HKCOMB**</dt></span><span class="sxs-lookup"><span data-stu-id="479bf-124"><dt>**HKCOMB\_SC**</dt></span></span> </dl>       | <span data-ttu-id="479bf-125">MAIUSC + CTRL</span><span class="sxs-lookup"><span data-stu-id="479bf-125">SHIFT+CTRL</span></span><br/>      |
| <span id="HKCOMB_SCA"></span><span id="hkcomb_sca"></span><dl> <span data-ttu-id="479bf-126"><dt>**HKCOMB \_ SCA**</dt></span><span class="sxs-lookup"><span data-stu-id="479bf-126"><dt>**HKCOMB\_SCA**</dt></span></span> </dl>    | <span data-ttu-id="479bf-127">MAIUSC + CTRL + ALT</span><span class="sxs-lookup"><span data-stu-id="479bf-127">SHIFT+CTRL+ALT</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="479bf-128">*lParam*</span><span class="sxs-lookup"><span data-stu-id="479bf-128">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="479bf-129">Matrice di flag che specificano la combinazione di tasti da utilizzare quando l'utente immette una combinazione non valida.</span><span class="sxs-lookup"><span data-stu-id="479bf-129">An array of flags that specify the key combination to use when the user enters an invalid combination.</span></span> <span data-ttu-id="479bf-130">Per un elenco di valori dei flag di modifica, vedere la descrizione del messaggio [**\_ GetHotKey HKM**](hkm-gethotkey.md) .</span><span class="sxs-lookup"><span data-stu-id="479bf-130">For a list of modifier flag values, see the description of the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="479bf-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="479bf-131">Return value</span></span>

<span data-ttu-id="479bf-132">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="479bf-132">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="479bf-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="479bf-133">Remarks</span></span>

<span data-ttu-id="479bf-134">Quando un utente immette una combinazione di chiavi non valida, come definito dai flag specificati in *wParam*, il sistema usa l'operatore OR bit per bit per combinare le chiavi immesse dall'utente con i flag specificati in *lParam*.</span><span class="sxs-lookup"><span data-stu-id="479bf-134">When a user enters an invalid key combination, as defined by flags specified in *wParam*, the system uses the bitwise-OR operator to combine the keys entered by the user with the flags specified in *lParam*.</span></span> <span data-ttu-id="479bf-135">La combinazione di tasti risultante viene convertita in una stringa e quindi visualizzata nel controllo tasto di scelta.</span><span class="sxs-lookup"><span data-stu-id="479bf-135">The resulting key combination is converted into a string and then displayed in the hot key control.</span></span>

## <a name="requirements"></a><span data-ttu-id="479bf-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="479bf-136">Requirements</span></span>



| <span data-ttu-id="479bf-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="479bf-137">Requirement</span></span> | <span data-ttu-id="479bf-138">Valore</span><span class="sxs-lookup"><span data-stu-id="479bf-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="479bf-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="479bf-139">Minimum supported client</span></span><br/> | <span data-ttu-id="479bf-140">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="479bf-140">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="479bf-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="479bf-141">Minimum supported server</span></span><br/> | <span data-ttu-id="479bf-142">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="479bf-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="479bf-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="479bf-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="479bf-144"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="479bf-144"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





