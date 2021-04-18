---
description: La funzione PdhVbGetCounterPathFromList copia il percorso del contatore a cui fa riferimento il parametro index da un elenco di percorsi dei contatori creato dall'utente dalla chiamata più recente alla funzione PdhVbCreateCounterPathList.
ms.assetid: e77a022d-42f2-4c48-acb7-36cb013730dd
title: PdhVbGetCounterPathFromList (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathFromList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 4c5ae4632ede898b7cd323723037ea68d53455b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312150"
---
# <a name="pdhvbgetcounterpathfromlist-function"></a><span data-ttu-id="17412-103">PdhVbGetCounterPathFromList (funzione)</span><span class="sxs-lookup"><span data-stu-id="17412-103">PdhVbGetCounterPathFromList function</span></span>

<span data-ttu-id="17412-104">La funzione **PdhVbGetCounterPathFromList** copia il percorso del contatore a cui fa riferimento il parametro *index* da un elenco di percorsi dei contatori creato dall'utente dalla chiamata più recente alla funzione [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) .</span><span class="sxs-lookup"><span data-stu-id="17412-104">The **PdhVbGetCounterPathFromList** function copies the counter path referenced by the *Index* parameter from a counter path list created by the user from the most recent call to the [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17412-105">La funzione descritta in questo argomento può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="17412-105">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="17412-106">Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="17412-106">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="17412-107">Funzione PdhVbGetCounterPathFromList ( \_ ByVal index As Long, \_ ByVal buffer As String, \_ ByVal bufferLength Long \_ ) Long</span><span class="sxs-lookup"><span data-stu-id="17412-107">Function PdhVbGetCounterPathFromList( \_ ByVal Index As Long, \_ ByVal Buffer As String, \_ ByVal BufferLength As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="17412-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="17412-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17412-109">*Index*</span><span class="sxs-lookup"><span data-stu-id="17412-109">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="17412-110">Indice del percorso del contatore da recuperare.</span><span class="sxs-lookup"><span data-stu-id="17412-110">Index of the counter path to retrieve.</span></span> <span data-ttu-id="17412-111">Deve essere un valore maggiore o uguale a 1 e minore o uguale al valore restituito dalla funzione [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) .</span><span class="sxs-lookup"><span data-stu-id="17412-111">This must be a value that is greater than or equal to 1, and less than or equal to the value returned by the [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="17412-112">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="17412-112">*Buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="17412-113">Stringa dimensionata e inizializzata che riceverà il percorso del contatore che corrisponde al valore del parametro index.</span><span class="sxs-lookup"><span data-stu-id="17412-113">Dimensioned and initialized string that will receive the counter path that corresponds to the value of the Index parameter.</span></span>

</dd> <dt>

<span data-ttu-id="17412-114">*BufferLength*</span><span class="sxs-lookup"><span data-stu-id="17412-114">*BufferLength*</span></span> 
</dt> <dd>

<span data-ttu-id="17412-115">Numero massimo di caratteri che si adatteranno alla stringa a cui fa riferimento il buffer.</span><span class="sxs-lookup"><span data-stu-id="17412-115">Maximum number of characters that will fit in the string referenced by Buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17412-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17412-116">Return value</span></span>

<span data-ttu-id="17412-117">La funzione restituisce il numero di caratteri copiati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="17412-117">The function returns the number of characters copied to Buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="17412-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17412-118">Requirements</span></span>



| <span data-ttu-id="17412-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="17412-119">Requirement</span></span> | <span data-ttu-id="17412-120">Valore</span><span class="sxs-lookup"><span data-stu-id="17412-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="17412-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17412-121">Minimum supported client</span></span><br/> | <span data-ttu-id="17412-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="17412-122">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="17412-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17412-123">Minimum supported server</span></span><br/> | <span data-ttu-id="17412-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="17412-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="17412-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="17412-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="17412-126"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17412-126"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="17412-127">DLL</span><span class="sxs-lookup"><span data-stu-id="17412-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17412-128"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17412-128"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17412-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17412-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17412-130">**PdhVbCreateCounterPathList**</span><span class="sxs-lookup"><span data-stu-id="17412-130">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[<span data-ttu-id="17412-131">**PdhVbGetCounterPathElements**</span><span class="sxs-lookup"><span data-stu-id="17412-131">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
</dt> <dt>

[<span data-ttu-id="17412-132">**PdhVbGetOneCounterPath**</span><span class="sxs-lookup"><span data-stu-id="17412-132">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




