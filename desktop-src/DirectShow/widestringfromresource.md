---
description: La funzione WideStringFromResource carica una stringa di caratteri wide da un file di risorse con l'identificatore di risorsa specificato.
ms.assetid: c5fac767-20c4-4342-9d4d-e1b916854b95
title: Funzione WideStringFromResource (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WideStringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c7cbdccc76fc57e660109851ae5b8f141704d04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329357"
---
# <a name="widestringfromresource-function"></a><span data-ttu-id="563ac-103">WideStringFromResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="563ac-103">WideStringFromResource function</span></span>

<span data-ttu-id="563ac-104">La `WideStringFromResource` funzione carica una stringa di caratteri wide da un file di risorse con l'identificatore di risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="563ac-104">The `WideStringFromResource` function loads a wide-character string from a resource file with the given resource identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="563ac-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="563ac-105">Syntax</span></span>


```C++
WCHAR* WINAPI WideStringFromResource(
   pBuffer *pBuffer,
   int     iResourceID
);
```



## <a name="parameters"></a><span data-ttu-id="563ac-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="563ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="563ac-107">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="563ac-107">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="563ac-108">Puntatore alla stringa corrispondente a *iResourceID*.</span><span class="sxs-lookup"><span data-stu-id="563ac-108">Pointer to the string corresponding to *iResourceID*.</span></span>

</dd> <dt>

<span data-ttu-id="563ac-109">*iResourceID*</span><span class="sxs-lookup"><span data-stu-id="563ac-109">*iResourceID*</span></span> 
</dt> <dd>

<span data-ttu-id="563ac-110">Identificatore di risorsa della stringa da recuperare.</span><span class="sxs-lookup"><span data-stu-id="563ac-110">Resource identifier of the string to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="563ac-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="563ac-111">Return value</span></span>

<span data-ttu-id="563ac-112">Restituisce la stessa stringa di *pbuffer*.</span><span class="sxs-lookup"><span data-stu-id="563ac-112">Returns the same string as *pBuffer*.</span></span> <span data-ttu-id="563ac-113">Se la funzione ha esito negativo, restituisce una stringa null.</span><span class="sxs-lookup"><span data-stu-id="563ac-113">If the function is not successful, returns a null string.</span></span>

## <a name="remarks"></a><span data-ttu-id="563ac-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="563ac-114">Remarks</span></span>

<span data-ttu-id="563ac-115">Le pagine delle proprietà vengono in genere chiamate tramite le interfacce COM, che usano stringhe a caratteri wide indipendentemente dalla modalità di compilazione del file binario.</span><span class="sxs-lookup"><span data-stu-id="563ac-115">Property pages are typically called through their COM interfaces, which use wide-character strings regardless of how the binary is built.</span></span> <span data-ttu-id="563ac-116">Questa funzione consente di convertire una stringa di risorsa in una stringa di caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="563ac-116">This function allows you to convert a resource string to a wide-character string.</span></span> <span data-ttu-id="563ac-117">La funzione converte la risorsa in una stringa di caratteri wide (se non è già una) dopo il caricamento.</span><span class="sxs-lookup"><span data-stu-id="563ac-117">The function converts the resource to a wide-character string (if it is not already one) after loading it.</span></span>

## <a name="requirements"></a><span data-ttu-id="563ac-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="563ac-118">Requirements</span></span>



| <span data-ttu-id="563ac-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="563ac-119">Requirement</span></span> | <span data-ttu-id="563ac-120">Valore</span><span class="sxs-lookup"><span data-stu-id="563ac-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="563ac-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="563ac-121">Header</span></span><br/>  | <dl> <span data-ttu-id="563ac-122"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="563ac-122"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="563ac-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="563ac-123">Library</span></span><br/> | <dl> <span data-ttu-id="563ac-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="563ac-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="563ac-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="563ac-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="563ac-126">Funzioni di supporto della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="563ac-126">Property Page Helper Functions</span></span>](property-page-helper-functions.md)
</dt> </dl>

 

 




