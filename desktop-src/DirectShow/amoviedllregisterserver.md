---
description: Obsoleta. In alternativa, usare AMovieDllRegisterServer2.
ms.assetid: d3be5fe0-f993-4a15-a3b8-3d761d51f289
title: Funzione AMovieDllRegisterServer (Dllsetup. h)
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
ms.openlocfilehash: d93724c0f1ea6ed8b6cd2fa2b683a5ba9d45f0d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330321"
---
# <a name="amoviedllregisterserver-function"></a><span data-ttu-id="5f204-104">AMovieDllRegisterServer (funzione)</span><span class="sxs-lookup"><span data-stu-id="5f204-104">AMovieDllRegisterServer function</span></span>

<span data-ttu-id="5f204-105">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="5f204-105">Obsolete.</span></span> <span data-ttu-id="5f204-106">In alternativa, usare [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) .</span><span class="sxs-lookup"><span data-stu-id="5f204-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f204-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f204-107">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="5f204-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f204-108">Parameters</span></span>

<span data-ttu-id="5f204-109">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="5f204-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f204-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f204-110">Return value</span></span>

<span data-ttu-id="5f204-111">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5f204-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5f204-112">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5f204-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f204-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f204-113">Requirements</span></span>



| <span data-ttu-id="5f204-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f204-114">Requirement</span></span> | <span data-ttu-id="5f204-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5f204-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f204-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f204-116">Header</span></span><br/>  | <dl> <span data-ttu-id="5f204-117"><dt>Dllsetup. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f204-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5f204-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="5f204-118">Library</span></span><br/> | <dl> <span data-ttu-id="5f204-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5f204-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f204-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f204-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f204-121">**Funzioni di installazione DLL**</span><span class="sxs-lookup"><span data-stu-id="5f204-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




