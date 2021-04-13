---
description: La funzione FilterAddObject aggiunge un singolo oggetto a un filtro di visualizzazione.
ms.assetid: 796216f4-a407-4a8c-98b3-8c3761d91913
title: Funzione FilterAddObject (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilterAddObject
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7fc6c41a675bfe560c060e271e4f9f48f88cd58c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484332"
---
# <a name="filteraddobject-function"></a><span data-ttu-id="d595c-103">FilterAddObject (funzione)</span><span class="sxs-lookup"><span data-stu-id="d595c-103">FilterAddObject function</span></span>

<span data-ttu-id="d595c-104">La funzione **FilterAddObject** aggiunge un singolo oggetto a un [*filtro di visualizzazione*](d.md).</span><span class="sxs-lookup"><span data-stu-id="d595c-104">The **FilterAddObject** function adds a single object to a [*display filter*](d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d595c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d595c-105">Syntax</span></span>


```C++
DWORD WINAPI FilterAddObject(
  _In_  HFILTER        hFilter,
  _Out_ LPFILTEROBJECT lpFilterObject
);
```



## <a name="parameters"></a><span data-ttu-id="d595c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d595c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d595c-107">*hFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d595c-107">*hFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d595c-108">Handle per il filtro di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d595c-108">Handle to the display filter.</span></span>

</dd> <dt>

<span data-ttu-id="d595c-109">*lpFilterObject* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d595c-109">*lpFilterObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d595c-110">Puntatore a una struttura [FILTEROBJECT](filterobject.md) che definisce l'oggetto da aggiungere al filtro.</span><span class="sxs-lookup"><span data-stu-id="d595c-110">Pointer to a [FILTEROBJECT](filterobject.md) structure that defines the object to be added to the filter.</span></span> <span data-ttu-id="d595c-111">Ogni oggetto può essere un operatore, un valore o una proprietà.</span><span class="sxs-lookup"><span data-stu-id="d595c-111">Each object can be an operator, value, or property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d595c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d595c-112">Return value</span></span>

<span data-ttu-id="d595c-113">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d595c-113">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d595c-114">Se la funzione ha esito negativo, il valore restituito è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="d595c-114">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="d595c-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d595c-115">Return code</span></span>                                                                                              | <span data-ttu-id="d595c-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d595c-116">Description</span></span>                                                                  |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d595c-117"><dt>**\_parametro NMERR non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d595c-117"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="d595c-118">Il parametro *hFilter* contiene un valore non valido.</span><span class="sxs-lookup"><span data-stu-id="d595c-118">The *hFilter* parameter has an invalid value.</span></span><br/>                     |
| <dl> <span data-ttu-id="d595c-119"><dt>**\_ \_ \_ memoria insufficiente NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="d595c-119"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="d595c-120">Network Monitor non dispone di memoria sufficiente per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d595c-120">Network Monitor does not have enough memory to create the object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d595c-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="d595c-121">Remarks</span></span>

<span data-ttu-id="d595c-122">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **FilterAddObject** .</span><span class="sxs-lookup"><span data-stu-id="d595c-122">[*Experts*](e.md) and [*parsers*](p.md) can call the **FilterAddObject** function.</span></span>

<span data-ttu-id="d595c-123">La funzione **FilterAddObject** viene chiamata ogni volta che un oggetto filtro viene aggiunto al filtro di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d595c-123">The **FilterAddObject** function is called each time a filter object is added to the display filter.</span></span> <span data-ttu-id="d595c-124">Il filtro di visualizzazione è uno stack di oggetti suffisso che può essere un operatore, un valore o una proprietà.</span><span class="sxs-lookup"><span data-stu-id="d595c-124">The display filter is a postfix stack of objects that can be an operator, value, or property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d595c-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d595c-125">Requirements</span></span>



| <span data-ttu-id="d595c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d595c-126">Requirement</span></span> | <span data-ttu-id="d595c-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d595c-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d595c-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d595c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d595c-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d595c-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d595c-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d595c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d595c-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d595c-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d595c-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d595c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d595c-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d595c-133"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d595c-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="d595c-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="d595c-135"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d595c-135"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d595c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d595c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d595c-137"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d595c-137"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d595c-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d595c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d595c-139">FILTEROBJECT</span><span class="sxs-lookup"><span data-stu-id="d595c-139">FILTEROBJECT</span></span>](filterobject.md)
</dt> </dl>

 

 




