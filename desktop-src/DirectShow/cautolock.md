---
description: La classe CAutoLock include una sezione critica per l'ambito di un blocco di codice.
ms.assetid: 8013b3a7-297b-4cf8-8107-4cee1fc12b56
title: Classe CAutoLock (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 866ca7164fdaef5a93679da000779c51fb4ddb24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327974"
---
# <a name="cautolock-class"></a><span data-ttu-id="a30b6-103">Classe CAutoLock</span><span class="sxs-lookup"><span data-stu-id="a30b6-103">CAutoLock class</span></span>

<span data-ttu-id="a30b6-104">La `CAutoLock` classe include una sezione critica per l'ambito di un blocco di codice.</span><span class="sxs-lookup"><span data-stu-id="a30b6-104">The `CAutoLock` class holds a critical section for the scope of a code block.</span></span>

<span data-ttu-id="a30b6-105">Questa classe funziona insieme alla classe [**CCritSec**](ccritsec.md) , che è un wrapper per gli oggetti della sezione critica.</span><span class="sxs-lookup"><span data-stu-id="a30b6-105">This class works in conjunction with the [**CCritSec**](ccritsec.md) class, which is a wrapper for critical section objects.</span></span> <span data-ttu-id="a30b6-106">Il `CAutoLock` Costruttore blocca la sezione critica e il distruttore lo sblocca.</span><span class="sxs-lookup"><span data-stu-id="a30b6-106">The `CAutoLock` constructor locks the critical section, and the destructor unlocks it.</span></span> <span data-ttu-id="a30b6-107">Utilizzando un `CAutoLock` oggetto come variabile locale, è possibile bloccare una sezione critica con la garanzia che tutti i percorsi del codice possano sbloccare la sezione critica.</span><span class="sxs-lookup"><span data-stu-id="a30b6-107">By using a `CAutoLock` object as a local variable, you can lock a critical section with the guarantee that all code paths will unlock the critical section.</span></span>

<span data-ttu-id="a30b6-108">Nell'esempio di codice seguente viene illustrato come utilizzare questa classe:</span><span class="sxs-lookup"><span data-stu-id="a30b6-108">The following code example shows how to use this class:</span></span>


```
CCritSec csMyLock;  // Critical section is not locked yet.
{
    CAutoLock cObjectLock(&csMyLock);  // Lock the critical section.

    // Protected section of code.     

} // Lock goes out of scope here.

```



<span data-ttu-id="a30b6-109">I metodi di questa classe non sono progettati per essere sottoposti a override.</span><span class="sxs-lookup"><span data-stu-id="a30b6-109">The methods in this class are not designed to be overridden.</span></span>



| <span data-ttu-id="a30b6-110">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="a30b6-110">Protected Member Variables</span></span>                 | <span data-ttu-id="a30b6-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a30b6-111">Description</span></span>                                                      |
|--------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="a30b6-112">**\_pLock m**</span><span class="sxs-lookup"><span data-stu-id="a30b6-112">**m\_pLock**</span></span>](cautolock-m-plock.md)      | <span data-ttu-id="a30b6-113">Sezione critica per questo blocco.</span><span class="sxs-lookup"><span data-stu-id="a30b6-113">Critical section for this lock.</span></span>                                  |
| <span data-ttu-id="a30b6-114">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="a30b6-114">Public Methods</span></span>                             | <span data-ttu-id="a30b6-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a30b6-115">Description</span></span>                                                      |
| [<span data-ttu-id="a30b6-116">**CAutoLock**</span><span class="sxs-lookup"><span data-stu-id="a30b6-116">**CAutoLock**</span></span>](cautolock-cautolock.md)   | <span data-ttu-id="a30b6-117">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="a30b6-117">Constructor method.</span></span> <span data-ttu-id="a30b6-118">Blocca l'oggetto sezione critica specificato.</span><span class="sxs-lookup"><span data-stu-id="a30b6-118">Locks the specified critical section object.</span></span> |
| [<span data-ttu-id="a30b6-119">**~ CAutoLock**</span><span class="sxs-lookup"><span data-stu-id="a30b6-119">**~CAutoLock**</span></span>](cautolock--cautolock.md) | <span data-ttu-id="a30b6-120">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="a30b6-120">Destructor method.</span></span> <span data-ttu-id="a30b6-121">Sblocca l'oggetto sezione critica.</span><span class="sxs-lookup"><span data-stu-id="a30b6-121">Unlocks the critical section object.</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="a30b6-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a30b6-122">Requirements</span></span>



| <span data-ttu-id="a30b6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a30b6-123">Requirement</span></span> | <span data-ttu-id="a30b6-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a30b6-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a30b6-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a30b6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a30b6-126"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a30b6-126"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a30b6-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="a30b6-127">Library</span></span><br/> | <dl> <span data-ttu-id="a30b6-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a30b6-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




