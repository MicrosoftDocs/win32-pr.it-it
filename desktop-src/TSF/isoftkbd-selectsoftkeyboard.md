---
title: Metodo ISoftKbd SelectSoftKeyboard (Softkbdc. h)
description: Il metodo ISoftKbd SelectSoftKeyboard seleziona la tastiera soft specificata.
ms.assetid: 7e85d346-3741-457d-aadd-11d3a6710e85
keywords:
- Framework servizi di testo Metodo SelectSoftKeyboard
- Framework dei servizi di testo del metodo SelectSoftKeyboard, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo SelectSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.SelectSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda9399297e9776e7fbd7cecb364fd7f6cd4604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518514"
---
# <a name="isoftkbdselectsoftkeyboard-method"></a><span data-ttu-id="ead76-106">Metodo ISoftKbd:: SelectSoftKeyboard</span><span class="sxs-lookup"><span data-stu-id="ead76-106">ISoftKbd::SelectSoftKeyboard method</span></span>

<span data-ttu-id="ead76-107">Il metodo **ISoftKbd:: SelectSoftKeyboard** seleziona la tastiera soft specificata.</span><span class="sxs-lookup"><span data-stu-id="ead76-107">The **ISoftKbd::SelectSoftKeyboard** method selects the specified soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="ead76-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ead76-108">Syntax</span></span>


```C++
HRESULT SelectSoftKeyboard(
  [in] DWORD dwKeyboardId
);
```



## <a name="parameters"></a><span data-ttu-id="ead76-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ead76-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ead76-110">*dwKeyboardId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ead76-110">*dwKeyboardId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ead76-111">Identificatore della tastiera soft da selezionare.</span><span class="sxs-lookup"><span data-stu-id="ead76-111">Identifier of the soft keyboard to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ead76-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ead76-112">Return value</span></span>

<span data-ttu-id="ead76-113">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="ead76-113">This method can return one of these values.</span></span>



| <span data-ttu-id="ead76-114">Valore</span><span class="sxs-lookup"><span data-stu-id="ead76-114">Value</span></span>                                                                                        | <span data-ttu-id="ead76-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ead76-115">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="ead76-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ead76-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ead76-117">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="ead76-117">The method was successful.</span></span><br/>               |
| <dl> <span data-ttu-id="ead76-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ead76-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ead76-119">Il parametro *dwKeyboardId* non è valido.</span><span class="sxs-lookup"><span data-stu-id="ead76-119">The *dwKeyboardId* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ead76-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ead76-120">Requirements</span></span>



| <span data-ttu-id="ead76-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ead76-121">Requirement</span></span> | <span data-ttu-id="ead76-122">Valore</span><span class="sxs-lookup"><span data-stu-id="ead76-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ead76-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ead76-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ead76-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ead76-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ead76-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ead76-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ead76-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ead76-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ead76-127">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="ead76-127">Redistributable</span></span><br/>          | <span data-ttu-id="ead76-128">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ead76-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="ead76-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ead76-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ead76-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="ead76-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="ead76-131">IDL</span><span class="sxs-lookup"><span data-stu-id="ead76-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ead76-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ead76-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="ead76-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ead76-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ead76-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ead76-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ead76-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ead76-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ead76-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="ead76-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





