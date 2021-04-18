---
title: Metodo ISoftKbd SetKeyboardLabelTextCombination (Softkbdc. h)
description: Il metodo ISoftKbd SetKeyboardLabelTextCombination imposta una combinazione di etichetta e testo usati per descrivere una tastiera soft.
ms.assetid: fe054eae-1a44-41ad-9a44-bc0b46df7c7b
keywords:
- Framework servizi di testo Metodo SetKeyboardLabelTextCombination
- Framework dei servizi di testo del metodo SetKeyboardLabelTextCombination, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo SetKeyboardLabelTextCombination
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelTextCombination
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98dad124455625f0da3ada1a717c692437398
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302181"
---
# <a name="isoftkbdsetkeyboardlabeltextcombination-method"></a><span data-ttu-id="3bcf2-106">Metodo ISoftKbd:: SetKeyboardLabelTextCombination</span><span class="sxs-lookup"><span data-stu-id="3bcf2-106">ISoftKbd::SetKeyboardLabelTextCombination method</span></span>

<span data-ttu-id="3bcf2-107">Il metodo **ISoftKbd:: SetKeyboardLabelTextCombination** imposta una combinazione di etichetta e testo usati per descrivere una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="3bcf2-107">The **ISoftKbd::SetKeyboardLabelTextCombination** method sets a combination of label and text used to describe a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bcf2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3bcf2-108">Syntax</span></span>


```C++
HRESULT SetKeyboardLabelTextCombination(
  [in] DWORD nModifierCombination
);
```



## <a name="parameters"></a><span data-ttu-id="3bcf2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3bcf2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bcf2-110">*nModifierCombination* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3bcf2-110">*nModifierCombination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bcf2-111">Combinazione di etichetta e testo usati per descrivere la tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="3bcf2-111">Combination of label and text used to describe the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bcf2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3bcf2-112">Return value</span></span>

<span data-ttu-id="3bcf2-113">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="3bcf2-113">This method can return one of these values.</span></span>



| <span data-ttu-id="3bcf2-114">Valore</span><span class="sxs-lookup"><span data-stu-id="3bcf2-114">Value</span></span>                                                                                        | <span data-ttu-id="3bcf2-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3bcf2-115">Description</span></span>                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="3bcf2-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3bcf2-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="3bcf2-117">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="3bcf2-117">The method was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="3bcf2-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3bcf2-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="3bcf2-119">Il parametro *nModifierCombination* non è valido.</span><span class="sxs-lookup"><span data-stu-id="3bcf2-119">The *nModifierCombination* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3bcf2-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3bcf2-120">Requirements</span></span>



| <span data-ttu-id="3bcf2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bcf2-121">Requirement</span></span> | <span data-ttu-id="3bcf2-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3bcf2-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bcf2-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bcf2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3bcf2-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3bcf2-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3bcf2-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bcf2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3bcf2-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3bcf2-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3bcf2-127">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="3bcf2-127">Redistributable</span></span><br/>          | <span data-ttu-id="3bcf2-128">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3bcf2-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="3bcf2-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3bcf2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bcf2-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bcf2-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="3bcf2-131">IDL</span><span class="sxs-lookup"><span data-stu-id="3bcf2-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3bcf2-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3bcf2-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="3bcf2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3bcf2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bcf2-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bcf2-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bcf2-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3bcf2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bcf2-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="3bcf2-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="3bcf2-137">**ISoftKbd::SetKeyboardLabelText**</span><span class="sxs-lookup"><span data-stu-id="3bcf2-137">**ISoftKbd::SetKeyboardLabelText**</span></span>](isoftkbd-setkeyboardlabeltext.md)
</dt> </dl>

 

 





