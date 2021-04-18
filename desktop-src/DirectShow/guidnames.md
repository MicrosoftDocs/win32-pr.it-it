---
description: GuidNames è una matrice globale nella libreria di classi base DirectShow che contiene le stringhe che rappresentano i GUID definiti in UUIDs. h. Questa matrice è utile per la generazione dell'output di debug.
ms.assetid: 6d72ad1e-588a-4a82-a1c1-e1e7b49df572
title: GuidNames (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GuidNames
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 359294d0cf3ab4e2074db5935cbbd604dcc1b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328167"
---
# <a name="guidnames"></a><span data-ttu-id="162e5-104">GuidNames</span><span class="sxs-lookup"><span data-stu-id="162e5-104">GuidNames</span></span>

<span data-ttu-id="162e5-105">`GuidNames` è una matrice globale nella libreria di classi base DirectShow che contiene stringhe che rappresentano i GUID definiti in UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="162e5-105">`GuidNames` is a global array in the DirectShow base class library that contains strings representing the GUIDs defined in Uuids.h.</span></span> <span data-ttu-id="162e5-106">Questa matrice è utile per la generazione dell'output di debug.</span><span class="sxs-lookup"><span data-stu-id="162e5-106">This array is useful for generating debug output.</span></span>

``` syntax
char* GuidNames[guid]
```

## <a name="parameters"></a><span data-ttu-id="162e5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="162e5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="162e5-108"><span id="guid"></span><span id="GUID"></span>*GUID*</span><span class="sxs-lookup"><span data-stu-id="162e5-108"><span id="guid"></span><span id="GUID"></span>*guid*</span></span>
</dt> <dd>

<span data-ttu-id="162e5-109">Specifica qualsiasi valore GUID definito nel file di intestazione UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="162e5-109">Specifies any GUID value defined in the header file Uuids.h.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="162e5-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="162e5-110">Remarks</span></span>

<span data-ttu-id="162e5-111">Usare questa matrice globale per restituire costanti GUID come stringhe.</span><span class="sxs-lookup"><span data-stu-id="162e5-111">Use this global array to output GUID constants as strings.</span></span> <span data-ttu-id="162e5-112">Il codice seguente, ad esempio, stampa la stringa "MEDIATYPE \_ video" nella console:</span><span class="sxs-lookup"><span data-stu-id="162e5-112">For example, the following code prints the string "MEDIATYPE\_Video" to the console:</span></span>


```C++
puts(GuidNames[MEDIATYPE_Video]);
```



<span data-ttu-id="162e5-113">Se il GUID non corrisponde, viene restituita la stringa "nome GUID sconosciuto".</span><span class="sxs-lookup"><span data-stu-id="162e5-113">If the GUID is not matched, the string "Unknown GUID Name" is returned.</span></span> <span data-ttu-id="162e5-114">Non tutti i GUID DirectShow sono definiti in UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="162e5-114">Not all DirectShow GUIDs are defined in uuids.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="162e5-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="162e5-115">Requirements</span></span>



| <span data-ttu-id="162e5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="162e5-116">Requirement</span></span> | <span data-ttu-id="162e5-117">Valore</span><span class="sxs-lookup"><span data-stu-id="162e5-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="162e5-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="162e5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="162e5-119"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="162e5-119"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="162e5-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="162e5-120">Library</span></span><br/> | <dl> <span data-ttu-id="162e5-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="162e5-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="162e5-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="162e5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="162e5-123">Funzioni di output di debug</span><span class="sxs-lookup"><span data-stu-id="162e5-123">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




