---
description: La funzione LoadStringAddr trasforma una stringa (ad esempio &\# 0034; 157.54.32.45&\# 0034;) e crea un indirizzo DWORD.
ms.assetid: 305e0072-b597-4cd5-975e-94103a1680aa
title: Funzione LoadStringAddr (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadStringAddr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3317c8e842c23daa08f260063a8310404c92aed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307723"
---
# <a name="loadstringaddr-function"></a><span data-ttu-id="07d33-103">LoadStringAddr (funzione)</span><span class="sxs-lookup"><span data-stu-id="07d33-103">LoadStringAddr function</span></span>

<span data-ttu-id="07d33-104">La funzione **LoadStringAddr** trasforma una stringa (ad esempio "157.54.32.45") e crea un indirizzo **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="07d33-104">The **LoadStringAddr** function transforms a string (such as "157.54.32.45") and creates a **DWORD** address.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d33-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07d33-105">Syntax</span></span>


```C++
BOOL LoadStringAddr(
         DWORD *pAddress,
   const char  *str
);
```



## <a name="parameters"></a><span data-ttu-id="07d33-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="07d33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07d33-107">*pAddress*</span><span class="sxs-lookup"><span data-stu-id="07d33-107">*pAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="07d33-108">Puntatore a un **valore DWORD**.</span><span class="sxs-lookup"><span data-stu-id="07d33-108">Pointer to a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="07d33-109">*str*</span><span class="sxs-lookup"><span data-stu-id="07d33-109">*str*</span></span> 
</dt> <dd>

<span data-ttu-id="07d33-110">Puntatore a una stringa di caratteri con rappresentazione x. x.x. x di un indirizzo IP (ad esempio, 127.0.0.1).</span><span class="sxs-lookup"><span data-stu-id="07d33-110">Pointer to a character string with x.x.x.x representation of an IP address (for example,127.0.0.1).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07d33-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07d33-111">Return value</span></span>

<span data-ttu-id="07d33-112">Se la funzione ha esito positivo (il nome dell'indirizzo è stato trovato); il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="07d33-112">If the function is successful (the address name was found); the return value is **TRUE**.</span></span>

<span data-ttu-id="07d33-113">Se la funzione ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="07d33-113">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="07d33-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07d33-114">Requirements</span></span>



| <span data-ttu-id="07d33-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="07d33-115">Requirement</span></span> | <span data-ttu-id="07d33-116">Valore</span><span class="sxs-lookup"><span data-stu-id="07d33-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="07d33-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07d33-117">Minimum supported client</span></span><br/> | <span data-ttu-id="07d33-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="07d33-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="07d33-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07d33-119">Minimum supported server</span></span><br/> | <span data-ttu-id="07d33-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="07d33-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="07d33-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07d33-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="07d33-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="07d33-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="07d33-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="07d33-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="07d33-124"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07d33-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="07d33-125">DLL</span><span class="sxs-lookup"><span data-stu-id="07d33-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07d33-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07d33-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




