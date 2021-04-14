---
title: Metodo ISoftKbd GetSoftKeyboardPosSize (Softkbdc. h)
description: Il metodo ISoftKbd GetSoftKeyboardPosSize recupera la posizione iniziale e le dimensioni di una tastiera soft.
ms.assetid: d4482e34-1723-4fe2-a488-e7c18eb3f68e
keywords:
- Framework servizi di testo Metodo GetSoftKeyboardPosSize
- Framework dei servizi di testo del metodo GetSoftKeyboardPosSize, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo GetSoftKeyboardPosSize
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9af445efd3e1b510280d20667862f2d95404597f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340912"
---
# <a name="isoftkbdgetsoftkeyboardpossize-method"></a><span data-ttu-id="9878f-106">Metodo ISoftKbd:: GetSoftKeyboardPosSize</span><span class="sxs-lookup"><span data-stu-id="9878f-106">ISoftKbd::GetSoftKeyboardPosSize method</span></span>

<span data-ttu-id="9878f-107">Il metodo **ISoftKbd:: GetSoftKeyboardPosSize** recupera la posizione iniziale e la dimensione di una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="9878f-107">The **ISoftKbd::GetSoftKeyboardPosSize** method retrieves the starting position and size of a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="9878f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9878f-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardPosSize(
  [out] POINT *lpStartPoint,
  [out] WORD  *lpwidth,
  [out] WORD  *lpheight
);
```



## <a name="parameters"></a><span data-ttu-id="9878f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9878f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9878f-110">*lpStartPoint* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9878f-110">*lpStartPoint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9878f-111">Puntatore a un buffer in cui questo metodo recupera una struttura di [punti](/previous-versions//dd162805(v=vs.85)) che indica le coordinate della posizione superiore sinistra della tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="9878f-111">Pointer to a buffer in which this method retrieves a [POINT](/previous-versions//dd162805(v=vs.85)) structure indicating the coordinates of the upper left position of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="9878f-112">*lpwidth* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9878f-112">*lpwidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9878f-113">Puntatore a un buffer in cui questo metodo recupera la larghezza della tastiera flessibile.</span><span class="sxs-lookup"><span data-stu-id="9878f-113">Pointer to a buffer in which this method retrieves the width of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="9878f-114">*lpheight* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9878f-114">*lpheight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9878f-115">Puntatore a un buffer in cui questo metodo recupera l'altezza della tastiera flessibile.</span><span class="sxs-lookup"><span data-stu-id="9878f-115">Pointer to a buffer in which this method retrieves the height of the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9878f-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9878f-116">Return value</span></span>

<span data-ttu-id="9878f-117">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="9878f-117">This method can return one of these values.</span></span>



| <span data-ttu-id="9878f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9878f-118">Value</span></span>                                                                                        | <span data-ttu-id="9878f-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9878f-119">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="9878f-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9878f-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="9878f-121">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="9878f-121">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="9878f-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9878f-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="9878f-123">Uno dei parametri non è valido.</span><span class="sxs-lookup"><span data-stu-id="9878f-123">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9878f-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9878f-124">Requirements</span></span>



| <span data-ttu-id="9878f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9878f-125">Requirement</span></span> | <span data-ttu-id="9878f-126">Valore</span><span class="sxs-lookup"><span data-stu-id="9878f-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9878f-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9878f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9878f-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9878f-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9878f-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9878f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9878f-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9878f-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9878f-131">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="9878f-131">Redistributable</span></span><br/>          | <span data-ttu-id="9878f-132">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9878f-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="9878f-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9878f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9878f-134"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="9878f-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="9878f-135">IDL</span><span class="sxs-lookup"><span data-stu-id="9878f-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9878f-136"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9878f-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="9878f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9878f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9878f-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9878f-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9878f-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9878f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9878f-140">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="9878f-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="9878f-141">**ISoftKbd::SetSoftKeyboardPosSize**</span><span class="sxs-lookup"><span data-stu-id="9878f-141">**ISoftKbd::SetSoftKeyboardPosSize**</span></span>](isoftkbd-setsoftkeyboardpossize.md)
</dt> </dl>

 

