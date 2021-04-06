---
title: Metodo ISoftKbd SetKeyboardLabelText (Softkbdc. h)
description: Il metodo ISoftKbd SetKeyboardLabelText imposta il testo dell'etichetta dal layout per una tastiera soft.
ms.assetid: 86c45c37-fe50-4596-b4c9-960de760a2e0
keywords:
- Framework servizi di testo Metodo SetKeyboardLabelText
- Framework dei servizi di testo del metodo SetKeyboardLabelText, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo SetKeyboardLabelText
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelText
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 862341182b9c97a751ba4a130566d5cf18437c2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742791"
---
# <a name="isoftkbdsetkeyboardlabeltext-method"></a><span data-ttu-id="ed7ff-106">Metodo ISoftKbd:: SetKeyboardLabelText</span><span class="sxs-lookup"><span data-stu-id="ed7ff-106">ISoftKbd::SetKeyboardLabelText method</span></span>

<span data-ttu-id="ed7ff-107">Il metodo **ISoftKbd:: SetKeyboardLabelText** imposta il testo dell'etichetta dal layout per una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="ed7ff-107">The **ISoftKbd::SetKeyboardLabelText** method sets the label text from the layout for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed7ff-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed7ff-108">Syntax</span></span>


```C++
HRESULT SetKeyboardLabelText(
  [in] HKL hKl
);
```



## <a name="parameters"></a><span data-ttu-id="ed7ff-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed7ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed7ff-110">*hKl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed7ff-110">*hKl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed7ff-111">Handle utilizzato per recuperare il layout installato per la tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="ed7ff-111">Handle that is used to retrieve the installed layout for the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed7ff-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed7ff-112">Return value</span></span>

<span data-ttu-id="ed7ff-113">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="ed7ff-113">This method can return one of these values.</span></span>



| <span data-ttu-id="ed7ff-114">Valore</span><span class="sxs-lookup"><span data-stu-id="ed7ff-114">Value</span></span>                                                                                        | <span data-ttu-id="ed7ff-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed7ff-115">Description</span></span>                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="ed7ff-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ed7ff-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ed7ff-117">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="ed7ff-117">The method was successful.</span></span><br/>      |
| <dl> <span data-ttu-id="ed7ff-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ed7ff-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ed7ff-119">Il parametro *hKl* non è valido.</span><span class="sxs-lookup"><span data-stu-id="ed7ff-119">The *hKl* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ed7ff-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed7ff-120">Requirements</span></span>



| <span data-ttu-id="ed7ff-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed7ff-121">Requirement</span></span> | <span data-ttu-id="ed7ff-122">Valore</span><span class="sxs-lookup"><span data-stu-id="ed7ff-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed7ff-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed7ff-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ed7ff-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ed7ff-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ed7ff-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed7ff-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ed7ff-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ed7ff-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ed7ff-127">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="ed7ff-127">Redistributable</span></span><br/>          | <span data-ttu-id="ed7ff-128">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ed7ff-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="ed7ff-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed7ff-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed7ff-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed7ff-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="ed7ff-131">IDL</span><span class="sxs-lookup"><span data-stu-id="ed7ff-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ed7ff-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ed7ff-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="ed7ff-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ed7ff-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed7ff-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed7ff-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed7ff-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed7ff-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed7ff-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="ed7ff-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="ed7ff-137">**ISoftKbd::SetKeyboardLabelTextCombination**</span><span class="sxs-lookup"><span data-stu-id="ed7ff-137">**ISoftKbd::SetKeyboardLabelTextCombination**</span></span>](isoftkbd-setkeyboardlabeltextcombination.md)
</dt> </dl>

 

 





