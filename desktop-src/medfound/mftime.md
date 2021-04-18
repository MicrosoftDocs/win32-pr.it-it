---
description: Definisce unità di 100 nanosecondi.
ms.assetid: 9273ff1f-382e-4c58-b571-4852545915b3
title: MFTIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e82c99c3c4a42b652c04595d086951c3c1a71a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329582"
---
# <a name="mftime"></a><span data-ttu-id="44bdc-103">MFTIME</span><span class="sxs-lookup"><span data-stu-id="44bdc-103">MFTIME</span></span>

<span data-ttu-id="44bdc-104">Definisce unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="44bdc-104">Defines units of 100 nanoseconds.</span></span>


```C++
typedef LONGLONG MFTIME;
```



## <a name="examples"></a><span data-ttu-id="44bdc-105">Esempio</span><span class="sxs-lookup"><span data-stu-id="44bdc-105">Examples</span></span>


```C++
const MFTIME ONE_SECOND = 10000000; // One second.
const LONG   ONE_MSEC = 1000;       // One millisecond

// Convert 100-nanosecond units to milliseconds.

inline LONG MFTimeToMsec(const LONGLONG& time)
{
    return (LONG)(time / (ONE_SECOND / ONE_MSEC));
}
```



## <a name="requirements"></a><span data-ttu-id="44bdc-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44bdc-106">Requirements</span></span>



| <span data-ttu-id="44bdc-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="44bdc-107">Requirement</span></span> | <span data-ttu-id="44bdc-108">Valore</span><span class="sxs-lookup"><span data-stu-id="44bdc-108">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="44bdc-109">Intestazione</span><span class="sxs-lookup"><span data-stu-id="44bdc-109">Header</span></span><br/> | <dl> <span data-ttu-id="44bdc-110"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="44bdc-110"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44bdc-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44bdc-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44bdc-112">Tipi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="44bdc-112">Media Foundation Datatypes</span></span>](media-foundation-datatypes.md)
</dt> </dl>

 

 




