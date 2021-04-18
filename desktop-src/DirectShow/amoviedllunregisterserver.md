---
description: Obsoleta. In alternativa, usare AMovieDllRegisterServer2.
ms.assetid: 80f52109-6239-4e3d-a395-eb69f5278cd2
title: Funzione AMovieDllUnregisterServer (Dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllUnregisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cab526a69f14cdd4c4f48767ca34722f61002eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331708"
---
# <a name="amoviedllunregisterserver-function"></a><span data-ttu-id="1b668-104">AMovieDllUnregisterServer (funzione)</span><span class="sxs-lookup"><span data-stu-id="1b668-104">AMovieDllUnregisterServer function</span></span>

<span data-ttu-id="1b668-105">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="1b668-105">Obsolete.</span></span> <span data-ttu-id="1b668-106">In alternativa, usare [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) .</span><span class="sxs-lookup"><span data-stu-id="1b668-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b668-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1b668-107">Syntax</span></span>


```C++
HRESULT AMovieDllUnregisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="1b668-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1b668-108">Parameters</span></span>

<span data-ttu-id="1b668-109">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="1b668-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1b668-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1b668-110">Return value</span></span>

<span data-ttu-id="1b668-111">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1b668-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1b668-112">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1b668-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b668-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b668-113">Requirements</span></span>



| <span data-ttu-id="1b668-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b668-114">Requirement</span></span> | <span data-ttu-id="1b668-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1b668-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b668-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1b668-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1b668-117"><dt>Dllsetup. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1b668-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1b668-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="1b668-118">Library</span></span><br/> | <dl> <span data-ttu-id="1b668-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1b668-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b668-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b668-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b668-121">**Funzioni di installazione DLL**</span><span class="sxs-lookup"><span data-stu-id="1b668-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




