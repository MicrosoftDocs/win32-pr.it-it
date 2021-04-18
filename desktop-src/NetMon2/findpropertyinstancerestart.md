---
description: Trova l'istanza successiva della proprietà specificata dal parametro hProperty.
ms.assetid: f77cb92b-5936-4349-bf66-643c16e9e0df
title: Funzione FindPropertyInstanceRestart (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstanceRestart
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: d1e731bb00b28bb62862dd18fbd6031fa973fe38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305930"
---
# <a name="findpropertyinstancerestart-function"></a><span data-ttu-id="93f1d-103">FindPropertyInstanceRestart (funzione)</span><span class="sxs-lookup"><span data-stu-id="93f1d-103">FindPropertyInstanceRestart function</span></span>

<span data-ttu-id="93f1d-104">La funzione **FindPropertyInstanceRestart** trova l'istanza successiva della proprietà specificata dal parametro *hProperty* .</span><span class="sxs-lookup"><span data-stu-id="93f1d-104">The **FindPropertyInstanceRestart** function finds the next instance of the property specified by the *hProperty* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="93f1d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93f1d-105">Syntax</span></span>


```C++
LPPROPERTYINST WINAPI FindPropertyInstanceRestart(
  _In_ HFRAME         hFrame,
  _In_ HPROPERTY      hProperty,
  _In_ LPPROPERTYINST *lpRestartKey,
  _In_ BOOL           DirForward
);
```



## <a name="parameters"></a><span data-ttu-id="93f1d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="93f1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93f1d-107">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93f1d-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93f1d-108">Handle per il frame.</span><span class="sxs-lookup"><span data-stu-id="93f1d-108">A handle to the frame.</span></span> <span data-ttu-id="93f1d-109">L'handle del frame può essere recuperato da una chiamata alla funzione [GetFrame](getframe.md) .</span><span class="sxs-lookup"><span data-stu-id="93f1d-109">The frame handle can be retrieved by a call to the [GetFrame](getframe.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="93f1d-110">*hProperty* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93f1d-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93f1d-111">Handle per la proprietà da trovare.</span><span class="sxs-lookup"><span data-stu-id="93f1d-111">A handle to the property to find.</span></span> <span data-ttu-id="93f1d-112">L'handle di proprietà può essere recuperato da una chiamata alla funzione [GetProperty](getproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="93f1d-112">The property handle can be retrieved by a call to the [GetProperty](getproperty.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="93f1d-113">*lpRestartKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93f1d-113">*lpRestartKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93f1d-114">Puntatore all'istanza della proprietà utilizzata come punto iniziale della ricerca.</span><span class="sxs-lookup"><span data-stu-id="93f1d-114">A pointer to the property instance used as the starting point of the search.</span></span> <span data-ttu-id="93f1d-115">Se il parametro *lpRestartKey* è impostato su **null**, la ricerca inizia all'inizio del frame o alla fine del frame, a seconda del valore del parametro *DirForward* .</span><span class="sxs-lookup"><span data-stu-id="93f1d-115">If the *lpRestartKey* parameter is set to **NULL**, the search begins at beginning of the frame, or the end of the frame, depending on the value of the *DirForward* parameter.</span></span>

<span data-ttu-id="93f1d-116">Se *lpRestartKey* punta a **null**, la ricerca inizia all'inizio del frame se *DirForward* è **true** o alla fine del frame se il parametro è **false**.</span><span class="sxs-lookup"><span data-stu-id="93f1d-116">If *lpRestartKey* points to **NULL**, the search begins at the beginning of the frame if *DirForward* is **TRUE** or the at end of the frame if the parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="93f1d-117">*DirForward* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93f1d-117">*DirForward* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93f1d-118">Indicatore della direzione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="93f1d-118">An indicator of the search direction.</span></span> <span data-ttu-id="93f1d-119">Se il valore è **true**, la ricerca viene spostata dalla posizione corrente alla fine del frame.</span><span class="sxs-lookup"><span data-stu-id="93f1d-119">If the value is **TRUE**, the search moves from the current location to the end of the frame.</span></span> <span data-ttu-id="93f1d-120">Se il valore è **false**, la ricerca viene spostata dalla posizione corrente all'inizio del frame.</span><span class="sxs-lookup"><span data-stu-id="93f1d-120">If the value is **FALSE**, the search moves from the current location to the beginning of the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93f1d-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93f1d-121">Return value</span></span>

<span data-ttu-id="93f1d-122">Se la funzione ha esito positivo, il valore restituito è il successivo **LPPROPERTYINST** valido.</span><span class="sxs-lookup"><span data-stu-id="93f1d-122">If the function is successful, the return value is the next valid **LPPROPERTYINST**.</span></span>

<span data-ttu-id="93f1d-123">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="93f1d-123">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="93f1d-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="93f1d-124">Remarks</span></span>

<span data-ttu-id="93f1d-125">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **FindPropertyInstanceRestart** .</span><span class="sxs-lookup"><span data-stu-id="93f1d-125">[*Experts*](e.md) and [*parsers*](p.md) can call the **FindPropertyInstanceRestart** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="93f1d-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93f1d-126">Requirements</span></span>



| <span data-ttu-id="93f1d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="93f1d-127">Requirement</span></span> | <span data-ttu-id="93f1d-128">Valore</span><span class="sxs-lookup"><span data-stu-id="93f1d-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="93f1d-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93f1d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="93f1d-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="93f1d-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="93f1d-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93f1d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="93f1d-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="93f1d-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="93f1d-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93f1d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="93f1d-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="93f1d-134"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="93f1d-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="93f1d-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="93f1d-136"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93f1d-136"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="93f1d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="93f1d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93f1d-138"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93f1d-138"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93f1d-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93f1d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93f1d-140">GetFrame</span><span class="sxs-lookup"><span data-stu-id="93f1d-140">GetFrame</span></span>](getframe.md)
</dt> <dt>

[<span data-ttu-id="93f1d-141">GetProperty</span><span class="sxs-lookup"><span data-stu-id="93f1d-141">GetProperty</span></span>](getproperty.md)
</dt> </dl>

 

 




