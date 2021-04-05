---
description: La funzione LookupDwordSetString restituisce la stringa corrispondente al valore specificato di un set con etichetta.
ms.assetid: ee2b1b7a-6b64-4c8c-a71d-de970b66d46e
title: Funzione LookupDwordSetString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupDwordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 57688edab7421f939e03322b8b244219b00d31fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752186"
---
# <a name="lookupdwordsetstring-function"></a><span data-ttu-id="cf2f8-103">LookupDwordSetString (funzione)</span><span class="sxs-lookup"><span data-stu-id="cf2f8-103">LookupDwordSetString function</span></span>

<span data-ttu-id="cf2f8-104">La funzione **LookupDwordSetString** restituisce la stringa corrispondente al valore specificato di un set con etichetta.</span><span class="sxs-lookup"><span data-stu-id="cf2f8-104">The **LookupDwordSetString** function returns the string corresponding to the specified value of a labeled set.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf2f8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf2f8-105">Syntax</span></span>


```C++
LPBYTE WINAPI LookupDwordSetString(
   LPSET lpSet,
   DWORD Value
);
```



## <a name="parameters"></a><span data-ttu-id="cf2f8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cf2f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf2f8-107">*lpSet*</span><span class="sxs-lookup"><span data-stu-id="cf2f8-107">*lpSet*</span></span> 
</dt> <dd>

<span data-ttu-id="cf2f8-108">Con etichetta impostata, da cui è possibile estrarre l'etichetta del valore.</span><span class="sxs-lookup"><span data-stu-id="cf2f8-108">Labeled set, from which you can extract the value's label.</span></span>

</dd> <dt>

<span data-ttu-id="cf2f8-109">*Valore*</span><span class="sxs-lookup"><span data-stu-id="cf2f8-109">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="cf2f8-110">Valore di un set con etichetta.</span><span class="sxs-lookup"><span data-stu-id="cf2f8-110">Value of a labeled set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf2f8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cf2f8-111">Return value</span></span>

<span data-ttu-id="cf2f8-112">Se la funzione ha esito positivo, il valore restituito è la stringa che corrisponde al valore specificato.</span><span class="sxs-lookup"><span data-stu-id="cf2f8-112">If the function is successful, the return value is the string that corresponds to the specified value.</span></span>

<span data-ttu-id="cf2f8-113">Se la funzione ha esito negativo, il valore specificato non è presente nel set, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="cf2f8-113">If the function is unsuccessful, the specified value is not in the set, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf2f8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf2f8-114">Requirements</span></span>



| <span data-ttu-id="cf2f8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf2f8-115">Requirement</span></span> | <span data-ttu-id="cf2f8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cf2f8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf2f8-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf2f8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cf2f8-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cf2f8-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="cf2f8-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf2f8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cf2f8-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cf2f8-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf2f8-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cf2f8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf2f8-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf2f8-122"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf2f8-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="cf2f8-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="cf2f8-124"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf2f8-124"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="cf2f8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cf2f8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf2f8-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf2f8-126"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




