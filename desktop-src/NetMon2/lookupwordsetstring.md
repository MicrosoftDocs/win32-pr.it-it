---
description: La funzione LookupWordSetString restituisce la stringa corrispondente al valore richiesto da un set con etichetta.
ms.assetid: e8d158a1-8544-4c10-b8e8-46888c1097e4
title: Funzione LookupWordSetString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupWordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7487becb195571e1eb88044195293b2c0b226e8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526761"
---
# <a name="lookupwordsetstring-function"></a><span data-ttu-id="166d7-103">LookupWordSetString (funzione)</span><span class="sxs-lookup"><span data-stu-id="166d7-103">LookupWordSetString function</span></span>

<span data-ttu-id="166d7-104">La funzione **LookupWordSetString** restituisce la stringa corrispondente al valore richiesto da un set con etichetta.</span><span class="sxs-lookup"><span data-stu-id="166d7-104">The **LookupWordSetString** function returns the string corresponding to the requested value from a labeled set.</span></span>

## <a name="syntax"></a><span data-ttu-id="166d7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="166d7-105">Syntax</span></span>


```C++
LPBYTE WINAPI LookupWordSetString(
   LPSET lpSet,
   WORD  Value
);
```



## <a name="parameters"></a><span data-ttu-id="166d7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="166d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="166d7-107">*lpSet*</span><span class="sxs-lookup"><span data-stu-id="166d7-107">*lpSet*</span></span> 
</dt> <dd>

<span data-ttu-id="166d7-108">Etichettato set da cui estrarre l'etichetta del valore.</span><span class="sxs-lookup"><span data-stu-id="166d7-108">Labeled set from which you extract the value's label.</span></span>

</dd> <dt>

<span data-ttu-id="166d7-109">*Valore*</span><span class="sxs-lookup"><span data-stu-id="166d7-109">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="166d7-110">Valore di un set con etichetta.</span><span class="sxs-lookup"><span data-stu-id="166d7-110">Value of a labeled set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="166d7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="166d7-111">Return value</span></span>

<span data-ttu-id="166d7-112">Se la funzione ha esito positivo, il valore restituito è una stringa che corrisponde al valore richiesto.</span><span class="sxs-lookup"><span data-stu-id="166d7-112">If the function is successful, the return value is a string that corresponds to the requested value.</span></span>

<span data-ttu-id="166d7-113">Se la funzione ha esito negativo, il valore specificato non è presente nel set, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="166d7-113">If the function is unsuccessful, the specified value is not in the set, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="166d7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="166d7-114">Requirements</span></span>



| <span data-ttu-id="166d7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="166d7-115">Requirement</span></span> | <span data-ttu-id="166d7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="166d7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="166d7-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="166d7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="166d7-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="166d7-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="166d7-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="166d7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="166d7-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="166d7-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="166d7-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="166d7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="166d7-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="166d7-122"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="166d7-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="166d7-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="166d7-124"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="166d7-124"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="166d7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="166d7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="166d7-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="166d7-126"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




