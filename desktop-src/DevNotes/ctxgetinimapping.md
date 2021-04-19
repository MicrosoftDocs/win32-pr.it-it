---
description: Determina se l'Terminal Server è in modalità di installazione (solo in Windows Terminal Server 4,0).
ms.assetid: f6cb7971-d4f5-49ca-938a-9c280028764a
title: CtxGetIniMapping (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CtxGetIniMapping
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 17093303cf0ea74e7efc6a3070c48660083bc491
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331821"
---
# <a name="ctxgetinimapping-function"></a><span data-ttu-id="6c65d-103">CtxGetIniMapping (funzione)</span><span class="sxs-lookup"><span data-stu-id="6c65d-103">CtxGetIniMapping function</span></span>

<span data-ttu-id="6c65d-104">\[Questa funzione non è supportata e non deve essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="6c65d-104">\[This function is not supported and should not be used.</span></span> <span data-ttu-id="6c65d-105">Potrebbe cambiare o scomparire completamente senza preavviso.</span><span class="sxs-lookup"><span data-stu-id="6c65d-105">It may change or disappear completely without advance notice.</span></span> <span data-ttu-id="6c65d-106">Usare invece **VerifyVersionInfo**.\]</span><span class="sxs-lookup"><span data-stu-id="6c65d-106">Instead, use **VerifyVersionInfo**.\]</span></span>

<span data-ttu-id="6c65d-107">Determina se l'Terminal Server è in modalità di installazione (solo in Windows Terminal Server 4,0).</span><span class="sxs-lookup"><span data-stu-id="6c65d-107">Determines whether the Terminal Server is in INSTALL mode (only on Windows Terminal Server 4.0).</span></span>

## <a name="syntax"></a><span data-ttu-id="6c65d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c65d-108">Syntax</span></span>


```C++
BOOLEAN CtxGetIniMapping(void);
```



## <a name="parameters"></a><span data-ttu-id="6c65d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c65d-109">Parameters</span></span>

<span data-ttu-id="6c65d-110">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="6c65d-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6c65d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c65d-111">Return value</span></span>

<span data-ttu-id="6c65d-112">Questa funzione restituisce **false** se il Terminal Server è in modalità di installazione, **true** se è in modalità di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6c65d-112">This function returns **FALSE** if the Terminal Server is in INSTALL mode, **TRUE** if it is in EXECUTE mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c65d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c65d-113">Requirements</span></span>



| <span data-ttu-id="6c65d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c65d-114">Requirement</span></span> | <span data-ttu-id="6c65d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6c65d-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c65d-116">DLL</span><span class="sxs-lookup"><span data-stu-id="6c65d-116">DLL</span></span><br/> | <dl> <span data-ttu-id="6c65d-117"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c65d-117"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c65d-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c65d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c65d-119">**VerifyVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="6c65d-119">**VerifyVersionInfo**</span></span>](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)
</dt> </dl>

 

 
