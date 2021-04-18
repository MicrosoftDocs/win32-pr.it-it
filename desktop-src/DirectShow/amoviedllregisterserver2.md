---
description: La funzione AMovieDllRegisterServer2 registra e Annulla la registrazione dei filtri.
ms.assetid: 2122949d-0117-4c68-bfcd-c717b14dc970
title: Funzione AMovieDllRegisterServer2 (Dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec36290b7cad66b2b5f27633d30ae76c3331eba9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331711"
---
# <a name="amoviedllregisterserver2-function"></a><span data-ttu-id="bb88d-103">AMovieDllRegisterServer2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="bb88d-103">AMovieDllRegisterServer2 function</span></span>

<span data-ttu-id="bb88d-104">La funzione **AMovieDllRegisterServer2** registra e Annulla la registrazione dei filtri.</span><span class="sxs-lookup"><span data-stu-id="bb88d-104">The **AMovieDllRegisterServer2** function registers and unregisters filters.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb88d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb88d-105">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer2(
   BOOL bRegister
);
```



## <a name="parameters"></a><span data-ttu-id="bb88d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb88d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb88d-107">*bRegister*</span><span class="sxs-lookup"><span data-stu-id="bb88d-107">*bRegister*</span></span> 
</dt> <dd>

<span data-ttu-id="bb88d-108">**True** indica che registra il filtro, **false** indica che è stata annullata la registrazione.</span><span class="sxs-lookup"><span data-stu-id="bb88d-108">**TRUE** indicates register the filter, **FALSE** indicates unregister it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb88d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb88d-109">Return value</span></span>

<span data-ttu-id="bb88d-110">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bb88d-110">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bb88d-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bb88d-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb88d-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb88d-112">Remarks</span></span>

<span data-ttu-id="bb88d-113">Usare questa funzione per impostare i filtri.</span><span class="sxs-lookup"><span data-stu-id="bb88d-113">Use this function to set up your filters.</span></span> <span data-ttu-id="bb88d-114">Per altre informazioni, vedere [How to register DirectShow Filters](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="bb88d-114">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb88d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb88d-115">Requirements</span></span>



| <span data-ttu-id="bb88d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb88d-116">Requirement</span></span> | <span data-ttu-id="bb88d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="bb88d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb88d-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb88d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="bb88d-119"><dt>Dllsetup. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb88d-119"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bb88d-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="bb88d-120">Library</span></span><br/> | <dl> <span data-ttu-id="bb88d-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bb88d-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb88d-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb88d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb88d-123">**Funzioni di installazione DLL**</span><span class="sxs-lookup"><span data-stu-id="bb88d-123">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




