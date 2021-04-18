---
description: La funzione FindPropertyInstance trova la prima istanza della proprietà specificata dal parametro hProperty.
ms.assetid: e994503d-2f32-4fa2-bba9-ff66c9d558dc
title: Funzione FindPropertyInstance (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 21f94a3e4a1eb9619b39cff534a778235980a278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305931"
---
# <a name="findpropertyinstance-function"></a><span data-ttu-id="4cb9f-103">FindPropertyInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="4cb9f-103">FindPropertyInstance function</span></span>

<span data-ttu-id="4cb9f-104">La funzione **FindPropertyInstance** trova la prima istanza della proprietà specificata dal parametro *hProperty* .</span><span class="sxs-lookup"><span data-stu-id="4cb9f-104">The **FindPropertyInstance** function finds the first instance of the property specified by the *hProperty* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cb9f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4cb9f-105">Syntax</span></span>


```C++
LPPROPERTYINST WINAPI FindPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a><span data-ttu-id="4cb9f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4cb9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cb9f-107">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cb9f-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb9f-108">Handle per il frame.</span><span class="sxs-lookup"><span data-stu-id="4cb9f-108">Handle to the frame.</span></span> <span data-ttu-id="4cb9f-109">L'handle del frame può essere recuperato da una chiamata alla funzione [GetFrame](getframe.md) .</span><span class="sxs-lookup"><span data-stu-id="4cb9f-109">The frame handle can be retrieved by a call to the [GetFrame](getframe.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="4cb9f-110">*hProperty* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cb9f-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb9f-111">Handle per la proprietà che si desidera trovare.</span><span class="sxs-lookup"><span data-stu-id="4cb9f-111">Handle to the property you want to find.</span></span> <span data-ttu-id="4cb9f-112">L'handle di proprietà può essere recuperato da una chiamata alla funzione [GetProperty](getproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="4cb9f-112">The property handle can be retrieved by a call to the [GetProperty](getproperty.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cb9f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4cb9f-113">Return value</span></span>

<span data-ttu-id="4cb9f-114">Se la funzione ha esito positivo, ovvero se la proprietà viene trovata, il valore restituito è un puntatore alla prima istanza della proprietà.</span><span class="sxs-lookup"><span data-stu-id="4cb9f-114">If the function is successful (that is, if the property is found), the return value is a pointer to the first instance of the property.</span></span>

<span data-ttu-id="4cb9f-115">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="4cb9f-115">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cb9f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="4cb9f-116">Remarks</span></span>

<span data-ttu-id="4cb9f-117">Per recuperare l'istanza successiva della proprietà, chiamare [FindPropertyInstanceRestart](findpropertyinstancerestart.md).</span><span class="sxs-lookup"><span data-stu-id="4cb9f-117">To retrieve the next instance of the property, call [FindPropertyInstanceRestart](findpropertyinstancerestart.md).</span></span>

<span data-ttu-id="4cb9f-118">Gli [*esperti*](e.md) e i [*parser*](p.md)possono chiamare la funzione **FindPropertyInstance** .</span><span class="sxs-lookup"><span data-stu-id="4cb9f-118">[*Experts*](e.md) and [*parsers*](p.md)can call the **FindPropertyInstance** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cb9f-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4cb9f-119">Requirements</span></span>



| <span data-ttu-id="4cb9f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cb9f-120">Requirement</span></span> | <span data-ttu-id="4cb9f-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4cb9f-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4cb9f-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4cb9f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4cb9f-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4cb9f-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4cb9f-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4cb9f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4cb9f-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4cb9f-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4cb9f-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4cb9f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cb9f-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cb9f-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="4cb9f-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="4cb9f-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="4cb9f-129"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cb9f-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="4cb9f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="4cb9f-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cb9f-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cb9f-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cb9f-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4cb9f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cb9f-133">FindPropertyInstanceRestart</span><span class="sxs-lookup"><span data-stu-id="4cb9f-133">FindPropertyInstanceRestart</span></span>](findpropertyinstancerestart.md)
</dt> </dl>

 

 




