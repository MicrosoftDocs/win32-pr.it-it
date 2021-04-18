---
description: La funzione LoadOLEAut32 carica la libreria a collegamento dinamico (OleAut32.dll) di automazione.
ms.assetid: af907341-1e2c-4c63-bf4e-d6c49b4f6a6e
title: Funzione LoadOLEAut32 (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadOLEAut32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b23bad7e445eebc78ecf8a849ddde8fc23746131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324784"
---
# <a name="loadoleaut32-function"></a><span data-ttu-id="cb5af-103">LoadOLEAut32 (funzione)</span><span class="sxs-lookup"><span data-stu-id="cb5af-103">LoadOLEAut32 function</span></span>

<span data-ttu-id="cb5af-104">La funzione **LoadOLEAut32** carica la libreria a collegamento dinamico (OleAut32.dll) di automazione.</span><span class="sxs-lookup"><span data-stu-id="cb5af-104">The **LoadOLEAut32** function loads the Automation dynamic-link library (OleAut32.dll).</span></span>

## <a name="syntax"></a><span data-ttu-id="cb5af-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb5af-105">Syntax</span></span>


```C++
HINSTANCE LoadOLEAut32(void);
```



## <a name="parameters"></a><span data-ttu-id="cb5af-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb5af-106">Parameters</span></span>

<span data-ttu-id="cb5af-107">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="cb5af-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cb5af-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb5af-108">Return value</span></span>

<span data-ttu-id="cb5af-109">Restituisce un handle a un'istanza di DLL di automazione.</span><span class="sxs-lookup"><span data-stu-id="cb5af-109">Returns a handle to an Automation DLL instance.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb5af-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb5af-110">Remarks</span></span>

<span data-ttu-id="cb5af-111">Quando il distruttore [**CBaseObject**](cbaseobject.md) Elimina l'oggetto che ha caricato OleAut32.dll, la libreria verrà scaricata se ancora caricata.</span><span class="sxs-lookup"><span data-stu-id="cb5af-111">When the [**CBaseObject**](cbaseobject.md) destructor destroys the object that loaded OleAut32.dll, it will unload the library if it is still loaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb5af-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb5af-112">Requirements</span></span>



| <span data-ttu-id="cb5af-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb5af-113">Requirement</span></span> | <span data-ttu-id="cb5af-114">Valore</span><span class="sxs-lookup"><span data-stu-id="cb5af-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb5af-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb5af-115">Header</span></span><br/>  | <dl> <span data-ttu-id="cb5af-116"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb5af-116"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cb5af-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="cb5af-117">Library</span></span><br/> | <dl> <span data-ttu-id="cb5af-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cb5af-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb5af-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb5af-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb5af-120">**Funzioni helper COM**</span><span class="sxs-lookup"><span data-stu-id="cb5af-120">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> </dl>

 

 




