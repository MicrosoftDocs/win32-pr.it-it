---
description: La funzione LookupByteSetString restituisce la stringa corrispondente al valore specificato di un set con etichetta.
ms.assetid: 295891f9-dc8d-4dbe-aac9-7d0a96993cfa
title: Funzione LookupByteSetString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupByteSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7a2b5bffbfcb30ed8ec00da42fbc9ad6008fd5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307716"
---
# <a name="lookupbytesetstring-function"></a><span data-ttu-id="842fa-103">LookupByteSetString (funzione)</span><span class="sxs-lookup"><span data-stu-id="842fa-103">LookupByteSetString function</span></span>

<span data-ttu-id="842fa-104">La funzione **LookupByteSetString** restituisce la stringa corrispondente al valore specificato di un set con etichetta.</span><span class="sxs-lookup"><span data-stu-id="842fa-104">The **LookupByteSetString** function returns the string corresponding to the specified value of a labeled set.</span></span>

## <a name="syntax"></a><span data-ttu-id="842fa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="842fa-105">Syntax</span></span>


```C++
LPBYTE WINAPI LookupByteSetString(
   LPSET lpSet,
   BYTE  Value
);
```



## <a name="parameters"></a><span data-ttu-id="842fa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="842fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="842fa-107">*lpSet*</span><span class="sxs-lookup"><span data-stu-id="842fa-107">*lpSet*</span></span> 
</dt> <dd>

<span data-ttu-id="842fa-108">Puntatore a un set con etichetta, da cui è possibile estrarre l'etichetta del valore.</span><span class="sxs-lookup"><span data-stu-id="842fa-108">Pointer to a labeled set, from which you can extract the value's label.</span></span>

</dd> <dt>

<span data-ttu-id="842fa-109">*Valore*</span><span class="sxs-lookup"><span data-stu-id="842fa-109">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="842fa-110">Valore di un set con etichetta.</span><span class="sxs-lookup"><span data-stu-id="842fa-110">Value of a labeled set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="842fa-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="842fa-111">Return value</span></span>

<span data-ttu-id="842fa-112">Se la funzione ha esito positivo, il valore restituito è una stringa che corrisponde al valore specificato.</span><span class="sxs-lookup"><span data-stu-id="842fa-112">If the function is successful, the return value is a string corresponding to the value provided.</span></span>

<span data-ttu-id="842fa-113">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="842fa-113">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="842fa-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="842fa-114">Requirements</span></span>



| <span data-ttu-id="842fa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="842fa-115">Requirement</span></span> | <span data-ttu-id="842fa-116">Valore</span><span class="sxs-lookup"><span data-stu-id="842fa-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="842fa-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="842fa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="842fa-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="842fa-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="842fa-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="842fa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="842fa-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="842fa-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="842fa-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="842fa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="842fa-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="842fa-122"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="842fa-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="842fa-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="842fa-124"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="842fa-124"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="842fa-125">DLL</span><span class="sxs-lookup"><span data-stu-id="842fa-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="842fa-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="842fa-126"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




