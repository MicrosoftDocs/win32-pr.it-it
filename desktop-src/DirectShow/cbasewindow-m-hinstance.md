---
description: Handle per l'istanza del modulo.
ms.assetid: ad889ebe-2bd8-4456-9517-9e2909697a02
title: 'Membro CBaseWindow:: m_hInstance (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hInstance
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6482aac80c1298ea403019f43ddc4effdc30b00a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325784"
---
# <a name="cbasewindowm_hinstance-member"></a><span data-ttu-id="ad57e-103">Membro HINSTANCE di CBaseWindow:: m \_</span><span class="sxs-lookup"><span data-stu-id="ad57e-103">CBaseWindow::m\_hInstance member</span></span>

<span data-ttu-id="ad57e-104">Handle per l'istanza del modulo.</span><span class="sxs-lookup"><span data-stu-id="ad57e-104">Handle to the module instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad57e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad57e-105">Syntax</span></span>


```C++
HINSTANCE m_hInstance;
```



## <a name="remarks"></a><span data-ttu-id="ad57e-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="ad57e-106">Remarks</span></span>

<span data-ttu-id="ad57e-107">La funzione del punto di ingresso della DLL imposta una variabile globale con un handle per l'istanza del modulo.</span><span class="sxs-lookup"><span data-stu-id="ad57e-107">The DLL entry point function sets a global variable with a handle to the module instance.</span></span> <span data-ttu-id="ad57e-108">La classe **CBaseWindow** archivia questo handle nel metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="ad57e-108">The **CBaseWindow** class stores this handle in its constructor method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad57e-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad57e-109">Requirements</span></span>



| <span data-ttu-id="ad57e-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad57e-110">Requirement</span></span> | <span data-ttu-id="ad57e-111">Valore</span><span class="sxs-lookup"><span data-stu-id="ad57e-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad57e-112">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad57e-112">Header</span></span><br/>  | <dl> <span data-ttu-id="ad57e-113"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad57e-113"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ad57e-114">Libreria</span><span class="sxs-lookup"><span data-stu-id="ad57e-114">Library</span></span><br/> | <dl> <span data-ttu-id="ad57e-115"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ad57e-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad57e-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad57e-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad57e-117">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="ad57e-117">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




