---
description: 'Funzione AMovieDllRegisterServer : obsoleta. In alternativa, usare AMovieDllRegisterServer2.'
ms.assetid: d3be5fe0-f993-4a15-a3b8-3d761d51f289
title: Funzione AMovieDllRegisterServer (Dllsetup.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81b6e73b1988d3eb97abdf9a5d2415ecbd62d8c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099939"
---
# <a name="amoviedllregisterserver-function"></a><span data-ttu-id="53781-104">Funzione AMovieDllRegisterServer</span><span class="sxs-lookup"><span data-stu-id="53781-104">AMovieDllRegisterServer function</span></span>

<span data-ttu-id="53781-105">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="53781-105">Obsolete.</span></span> <span data-ttu-id="53781-106">In [**alternativa, usare AMovieDllRegisterServer2.**](amoviedllregisterserver2.md)</span><span class="sxs-lookup"><span data-stu-id="53781-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="53781-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53781-107">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="53781-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="53781-108">Parameters</span></span>

<span data-ttu-id="53781-109">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="53781-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="53781-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53781-110">Return value</span></span>

<span data-ttu-id="53781-111">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="53781-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="53781-112">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="53781-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="53781-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53781-113">Requirements</span></span>



| <span data-ttu-id="53781-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="53781-114">Requirement</span></span> | <span data-ttu-id="53781-115">Valore</span><span class="sxs-lookup"><span data-stu-id="53781-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53781-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53781-116">Header</span></span><br/>  | <dl> <span data-ttu-id="53781-117"><dt>Dllsetup.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="53781-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="53781-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="53781-118">Library</span></span><br/> | <dl> <span data-ttu-id="53781-119"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="53781-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53781-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53781-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53781-121">**Funzioni di installazione dll**</span><span class="sxs-lookup"><span data-stu-id="53781-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




