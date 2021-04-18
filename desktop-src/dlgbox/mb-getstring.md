---
title: Funzione MB_GetString (User. h)
description: Restituisce le stringhe per i pulsanti standard della finestra di messaggio.
ms.assetid: D2AF238D-F5A8-477D-BF47-0F5D4D68B27E
keywords:
- Finestre di dialogo MB_GetString funzione
topic_type:
- apiref
api_name:
- MB_GetString
api_location:
- user32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eafd33f268f2ef1ef87755b79aba6d5d0aa77bb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331573"
---
# <a name="mb_getstring-function"></a><span data-ttu-id="53651-104">MB- \_ funzione GetString</span><span class="sxs-lookup"><span data-stu-id="53651-104">MB\_GetString function</span></span>

<span data-ttu-id="53651-105">Restituisce le stringhe per i pulsanti standard della finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="53651-105">Returns strings for standard message box buttons.</span></span>

## <a name="syntax"></a><span data-ttu-id="53651-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53651-106">Syntax</span></span>


```C++
LPCWSTR WINAPI MB_GetString(
   UINT wBtn
);
```



## <a name="parameters"></a><span data-ttu-id="53651-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="53651-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53651-108">*wBtn*</span><span class="sxs-lookup"><span data-stu-id="53651-108">*wBtn*</span></span> 
</dt> <dd>

<span data-ttu-id="53651-109">ID della stringa da restituire.</span><span class="sxs-lookup"><span data-stu-id="53651-109">The id of the string to return.</span></span> <span data-ttu-id="53651-110">Sono identificati dai valori ID del comando della finestra di dialogo elencati in winuser. h.</span><span class="sxs-lookup"><span data-stu-id="53651-110">These are identified by the Dialog Box Command ID values listed in winuser.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53651-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53651-111">Return value</span></span>

<span data-ttu-id="53651-112">Stringa o NULL se non viene trovato.</span><span class="sxs-lookup"><span data-stu-id="53651-112">The string, or NULL if not found.</span></span>

## <a name="requirements"></a><span data-ttu-id="53651-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53651-113">Requirements</span></span>



| <span data-ttu-id="53651-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="53651-114">Requirement</span></span> | <span data-ttu-id="53651-115">Valore</span><span class="sxs-lookup"><span data-stu-id="53651-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53651-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53651-116">Header</span></span><br/>  | <dl> <span data-ttu-id="53651-117"><dt>Utente. h</dt></span><span class="sxs-lookup"><span data-stu-id="53651-117"><dt>User.h</dt></span></span> </dl>     |
| <span data-ttu-id="53651-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="53651-118">Library</span></span><br/> | <dl> <span data-ttu-id="53651-119"><dt>User32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53651-119"><dt>User32.lib</dt></span></span> </dl> |
| <span data-ttu-id="53651-120">DLL</span><span class="sxs-lookup"><span data-stu-id="53651-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="53651-121"><dt>User32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53651-121"><dt>User32.dll</dt></span></span> </dl> |



 

 





