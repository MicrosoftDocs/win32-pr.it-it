---
title: Metodo ISoftKbd SetSoftKeyboardPosSize (Softkbdc. h)
description: Il metodo ISoftKbd SetSoftKeyboardPosSize imposta la posizione iniziale e le dimensioni di una tastiera soft.
ms.assetid: bf827b07-0e8b-4d5a-8178-45d75af83551
keywords:
- Framework servizi di testo Metodo SetSoftKeyboardPosSize
- Framework dei servizi di testo del metodo SetSoftKeyboardPosSize, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo SetSoftKeyboardPosSize
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7131d9c46c90917f2ebdf471916f872aedb2e33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478208"
---
# <a name="isoftkbdsetsoftkeyboardpossize-method"></a><span data-ttu-id="14dfd-106">Metodo ISoftKbd:: SetSoftKeyboardPosSize</span><span class="sxs-lookup"><span data-stu-id="14dfd-106">ISoftKbd::SetSoftKeyboardPosSize method</span></span>

<span data-ttu-id="14dfd-107">Il metodo **ISoftKbd:: SetSoftKeyboardPosSize** imposta la posizione iniziale e la dimensione di una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="14dfd-107">The **ISoftKbd::SetSoftKeyboardPosSize** method sets the starting position and size of a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="14dfd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14dfd-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardPosSize(
  [in] POINT StartPoint,
  [in] WORD  width,
  [in] WORD  height
);
```



## <a name="parameters"></a><span data-ttu-id="14dfd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="14dfd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14dfd-110">Punto *iniziale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14dfd-110">*StartPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14dfd-111">Struttura di [punti](/previous-versions//dd162805(v=vs.85)) che indica le coordinate della posizione superiore sinistra della tastiera morbida.</span><span class="sxs-lookup"><span data-stu-id="14dfd-111">A [POINT](/previous-versions//dd162805(v=vs.85)) structure indicating the coordinates of the upper left position of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="14dfd-112">*larghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14dfd-112">*width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14dfd-113">Larghezza della tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="14dfd-113">Width of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="14dfd-114">*altezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14dfd-114">*height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14dfd-115">Altezza della tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="14dfd-115">Height of the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14dfd-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14dfd-116">Return value</span></span>

<span data-ttu-id="14dfd-117">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="14dfd-117">This method can return one of these values.</span></span>



| <span data-ttu-id="14dfd-118">Valore</span><span class="sxs-lookup"><span data-stu-id="14dfd-118">Value</span></span>                                                                                        | <span data-ttu-id="14dfd-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14dfd-119">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="14dfd-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="14dfd-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="14dfd-121">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="14dfd-121">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="14dfd-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="14dfd-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="14dfd-123">Uno dei parametri non è valido.</span><span class="sxs-lookup"><span data-stu-id="14dfd-123">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="14dfd-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14dfd-124">Requirements</span></span>



| <span data-ttu-id="14dfd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="14dfd-125">Requirement</span></span> | <span data-ttu-id="14dfd-126">Valore</span><span class="sxs-lookup"><span data-stu-id="14dfd-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14dfd-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14dfd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="14dfd-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="14dfd-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="14dfd-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14dfd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="14dfd-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="14dfd-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="14dfd-131">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="14dfd-131">Redistributable</span></span><br/>          | <span data-ttu-id="14dfd-132">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="14dfd-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="14dfd-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14dfd-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="14dfd-134"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="14dfd-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="14dfd-135">IDL</span><span class="sxs-lookup"><span data-stu-id="14dfd-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="14dfd-136"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="14dfd-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="14dfd-137">DLL</span><span class="sxs-lookup"><span data-stu-id="14dfd-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14dfd-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14dfd-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14dfd-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14dfd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14dfd-140">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="14dfd-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

