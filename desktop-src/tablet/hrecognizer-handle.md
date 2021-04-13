---
description: Un handle HRECOGNIZER viene usato per creare un contesto di riconoscimento, recuperare gli attributi e le proprietà del riconoscimento e determinare le proprietà dei pacchetti richieste dal riconoscimento per eseguire il riconoscimento.
ms.assetid: 1fc1901e-8c4d-4ef1-8c38-52d46ce10a48
title: Handle HRECOGNIZER (riepilogo. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e78086ff86453ef8b0157bb3b274f3c47be0dc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343746"
---
# <a name="hrecognizer-handle"></a><span data-ttu-id="05188-103">Handle HRECOGNIZER</span><span class="sxs-lookup"><span data-stu-id="05188-103">HRECOGNIZER Handle</span></span>

<span data-ttu-id="05188-104">Un handle **HRECOGNIZER** viene usato per creare un contesto di riconoscimento, recuperare gli attributi e le proprietà del riconoscimento e determinare le proprietà dei pacchetti richieste dal riconoscimento per eseguire il riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="05188-104">An **HRECOGNIZER** handle is used to create a recognizer context, retrieve the recognizer's attributes and properties, and determine which packet properties the recognizer requires to perform recognition.</span></span>


```C++
typedef HANDLE HRECOGNIZER;
```



## <a name="remarks"></a><span data-ttu-id="05188-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="05188-105">Remarks</span></span>

<span data-ttu-id="05188-106">Le funzioni seguenti usano un **HRECOGNIZER**.</span><span class="sxs-lookup"><span data-stu-id="05188-106">The following functions use an **HRECOGNIZER**.</span></span>



| <span data-ttu-id="05188-107">Funzione</span><span class="sxs-lookup"><span data-stu-id="05188-107">Function</span></span>                                                               | <span data-ttu-id="05188-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05188-108">Description</span></span>                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05188-109">**CreateRecognizer**</span><span class="sxs-lookup"><span data-stu-id="05188-109">**CreateRecognizer**</span></span>](/windows/desktop/api/recapis/nf-recapis-createrecognizer)                           | <span data-ttu-id="05188-110">Crea un riconoscitore.</span><span class="sxs-lookup"><span data-stu-id="05188-110">Creates a recognizer.</span></span><br/>                                                                   |
| [<span data-ttu-id="05188-111">**DestroyRecognizer**</span><span class="sxs-lookup"><span data-stu-id="05188-111">**DestroyRecognizer**</span></span>](/windows/desktop/api/recapis/nf-recapis-destroyrecognizer)                         | <span data-ttu-id="05188-112">Elimina definitivamente un riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="05188-112">Destroys a recognizer.</span></span><br/>                                                                  |
| [<span data-ttu-id="05188-113">**GetRecoAttributes**</span><span class="sxs-lookup"><span data-stu-id="05188-113">**GetRecoAttributes**</span></span>](/windows/desktop/api/recapis/nf-recapis-getrecoattributes)                         | <span data-ttu-id="05188-114">Restituisce gli attributi del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="05188-114">Returns the attributes of the recognizer.</span></span><br/>                                               |
| [<span data-ttu-id="05188-115">**CreateContext**</span><span class="sxs-lookup"><span data-stu-id="05188-115">**CreateContext**</span></span>](/windows/desktop/api/recapis/nf-recapis-createcontext)                                 | <span data-ttu-id="05188-116">Crea un contesto del riconoscitore.</span><span class="sxs-lookup"><span data-stu-id="05188-116">Creates a recognizer context.</span></span><br/>                                                           |
| [<span data-ttu-id="05188-117">**DestroyContext**</span><span class="sxs-lookup"><span data-stu-id="05188-117">**DestroyContext**</span></span>](/windows/desktop/api/recapis/nf-recapis-destroycontext)                               | <span data-ttu-id="05188-118">Elimina un contesto del riconoscitore.</span><span class="sxs-lookup"><span data-stu-id="05188-118">Destroys a recognizer context.</span></span><br/>                                                          |
| [<span data-ttu-id="05188-119">**GetAllRecognizers**</span><span class="sxs-lookup"><span data-stu-id="05188-119">**GetAllRecognizers**</span></span>](/windows/desktop/api/recapis/nf-recapis-getallrecognizers)                         | <span data-ttu-id="05188-120">Ottiene tutti i riconoscitori.</span><span class="sxs-lookup"><span data-stu-id="05188-120">Gets all recognizers.</span></span><br/>                                                                   |
| [<span data-ttu-id="05188-121">**GetResultPropertyList**</span><span class="sxs-lookup"><span data-stu-id="05188-121">**GetResultPropertyList**</span></span>](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)                 | <span data-ttu-id="05188-122">Recupera un elenco di proprietà che il riconoscimento può restituire per un intervallo di risultati.</span><span class="sxs-lookup"><span data-stu-id="05188-122">Retrieves a list of properties the recognizer can return for a result range.</span></span><br/>            |
| [<span data-ttu-id="05188-123">**GetPreferredPacketDescription**</span><span class="sxs-lookup"><span data-stu-id="05188-123">**GetPreferredPacketDescription**</span></span>](/windows/desktop/api/recapis/nf-recapis-getpreferredpacketdescription) | <span data-ttu-id="05188-124">Recupera una descrizione del pacchetto che contiene le proprietà del pacchetto utilizzate dal riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="05188-124">Retrieves a packet description that contains the packet properties the recognizer uses.</span></span><br/> |
| [<span data-ttu-id="05188-125">**GetUnicodeRanges**</span><span class="sxs-lookup"><span data-stu-id="05188-125">**GetUnicodeRanges**</span></span>](/windows/desktop/api/recapis/nf-recapis-getunicoderanges)                           | <span data-ttu-id="05188-126">Recupera gli intervalli di punti Unicode supportati dal riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="05188-126">Retrieves the ranges of Unicode points that the recognizer supports.</span></span><br/>                    |
| [<span data-ttu-id="05188-127">**LoadCachedAttributes**</span><span class="sxs-lookup"><span data-stu-id="05188-127">**LoadCachedAttributes**</span></span>](/windows/desktop/api/recapis/nf-recapis-loadcachedattributes)                   | <span data-ttu-id="05188-128">Carica gli attributi memorizzati nella cache di un riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="05188-128">Loads the cached attributes of a recognizer.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="05188-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05188-129">Requirements</span></span>



| <span data-ttu-id="05188-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="05188-130">Requirement</span></span> | <span data-ttu-id="05188-131">Valore</span><span class="sxs-lookup"><span data-stu-id="05188-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="05188-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05188-132">Minimum supported client</span></span><br/> | <span data-ttu-id="05188-133">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="05188-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="05188-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05188-134">Minimum supported server</span></span><br/> | <span data-ttu-id="05188-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="05188-135">None supported</span></span><br/>                                                            |
| <span data-ttu-id="05188-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="05188-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="05188-137"><dt>Riepilogo. h</dt></span><span class="sxs-lookup"><span data-stu-id="05188-137"><dt>Recapis.h</dt></span></span> </dl> |



 

 




