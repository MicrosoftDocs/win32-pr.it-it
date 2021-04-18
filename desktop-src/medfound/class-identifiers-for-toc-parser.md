---
description: Le classi seguenti sono dichiarate e associate a identificatori di classe (CLSID) in wmcodecdsp. h.
ms.assetid: f82d92dc-fbce-4274-a10f-72fa8dd776cc
title: Identificatori di classe per il parser della tabella dei contenuti (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5108855c687085e77ce36aa14b3424732e25572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305508"
---
# <a name="class-identifiers-for-table-of-contents-parser"></a><span data-ttu-id="a9b36-103">Identificatori di classe per il parser della tabella dei contenuti</span><span class="sxs-lookup"><span data-stu-id="a9b36-103">Class Identifiers for Table of Contents Parser</span></span>

<span data-ttu-id="a9b36-104">Le classi seguenti sono dichiarate e associate a identificatori di classe (CLSID) in wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="a9b36-104">The following classes are declared and associated with class identifiers (CLSIDs) in wmcodecdsp.h.</span></span>



| <span data-ttu-id="a9b36-105">Nome di classe</span><span class="sxs-lookup"><span data-stu-id="a9b36-105">Class name</span></span>       | <span data-ttu-id="a9b36-106">Nome descrittivo dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="a9b36-106">Friendly object name</span></span> |
|------------------|----------------------|
| <span data-ttu-id="a9b36-107">CTocEntry</span><span class="sxs-lookup"><span data-stu-id="a9b36-107">CTocEntry</span></span>        | <span data-ttu-id="a9b36-108">Voce Sommario</span><span class="sxs-lookup"><span data-stu-id="a9b36-108">TOC Entry</span></span>            |
| <span data-ttu-id="a9b36-109">CTocEntryList</span><span class="sxs-lookup"><span data-stu-id="a9b36-109">CTocEntryList</span></span>    | <span data-ttu-id="a9b36-110">Elenco voci Sommario</span><span class="sxs-lookup"><span data-stu-id="a9b36-110">TOC Entry List</span></span>       |
| <span data-ttu-id="a9b36-111">CToc</span><span class="sxs-lookup"><span data-stu-id="a9b36-111">CToc</span></span>             | <span data-ttu-id="a9b36-112">Sommario</span><span class="sxs-lookup"><span data-stu-id="a9b36-112">TOC</span></span>                  |
| <span data-ttu-id="a9b36-113">CTocCollection</span><span class="sxs-lookup"><span data-stu-id="a9b36-113">CTocCollection</span></span>   | <span data-ttu-id="a9b36-114">Raccolta TOC</span><span class="sxs-lookup"><span data-stu-id="a9b36-114">TOC Collection</span></span>       |
| <span data-ttu-id="a9b36-115">CTocParser</span><span class="sxs-lookup"><span data-stu-id="a9b36-115">CTocParser</span></span>       | <span data-ttu-id="a9b36-116">Parser Sommario</span><span class="sxs-lookup"><span data-stu-id="a9b36-116">TOC Parser</span></span>           |
| <span data-ttu-id="a9b36-117">CTocGeneratorDmo</span><span class="sxs-lookup"><span data-stu-id="a9b36-117">CTocGeneratorDmo</span></span> | <span data-ttu-id="a9b36-118">Generatore Sommario</span><span class="sxs-lookup"><span data-stu-id="a9b36-118">TOC Generator</span></span>        |



 

<span data-ttu-id="a9b36-119">La tabella precedente fornisce un nome descrittivo dell'oggetto per ogni classe.</span><span class="sxs-lookup"><span data-stu-id="a9b36-119">The preceding table gives a friendly object name for each class.</span></span> <span data-ttu-id="a9b36-120">In questa documentazione vengono utilizzati i nomi descrittivi per fare riferimento alle istanze delle classi.</span><span class="sxs-lookup"><span data-stu-id="a9b36-120">This documentation uses those friendly names to refer to instances of the classes.</span></span> <span data-ttu-id="a9b36-121">La documentazione, ad esempio, fa riferimento a un'istanza della classe CTocEntry come oggetto voce del sommario.</span><span class="sxs-lookup"><span data-stu-id="a9b36-121">For example, the documentation refers to an instance of the CTocEntry class as a TOC Entry object.</span></span>

<span data-ttu-id="a9b36-122">Nel codice è possibile usare **\_ \_ uuidof** per fare riferimento ai CLSID.</span><span class="sxs-lookup"><span data-stu-id="a9b36-122">In code, you can use **\_\_uuidof** to refer to the CLSIDs.</span></span> <span data-ttu-id="a9b36-123">Ad esempio, è possibile usare il codice seguente per fare riferimento al CLSID per CTocGeneratorDmo.</span><span class="sxs-lookup"><span data-stu-id="a9b36-123">For example, you can use the following code to refer to the CLSID for CTocGeneratorDmo.</span></span>


```C++
__uuidof(CTocGeneratorDmo)
```



### <a name="clsid-constants-defined-in-wmcodecdsph"></a><span data-ttu-id="a9b36-124">Costanti CLSID definite in Wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="a9b36-124">CLSID Constants Defined in Wmcodecdsp.h</span></span>

<span data-ttu-id="a9b36-125">In alternativa all'utilizzo di **\_ \_ uuidof**, è possibile utilizzare le costanti per fare riferimento ai CLSID.</span><span class="sxs-lookup"><span data-stu-id="a9b36-125">As an alternative to using **\_\_uuidof**, you can use constants to refer to the CLSIDs.</span></span> <span data-ttu-id="a9b36-126">Le costanti seguenti sono definite in wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="a9b36-126">The following constants are defined in wmcodecdsp.h</span></span>



| <span data-ttu-id="a9b36-127">Nome di classe</span><span class="sxs-lookup"><span data-stu-id="a9b36-127">Class name</span></span>     | <span data-ttu-id="a9b36-128">Costante CLSID</span><span class="sxs-lookup"><span data-stu-id="a9b36-128">CLSID constant</span></span>        |
|----------------|-----------------------|
| <span data-ttu-id="a9b36-129">CTocEntry</span><span class="sxs-lookup"><span data-stu-id="a9b36-129">CTocEntry</span></span>      | <span data-ttu-id="a9b36-130">\_CTOCENTRY CLSID</span><span class="sxs-lookup"><span data-stu-id="a9b36-130">CLSID\_CTocEntry</span></span>      |
| <span data-ttu-id="a9b36-131">CTocEntryList</span><span class="sxs-lookup"><span data-stu-id="a9b36-131">CTocEntryList</span></span>  | <span data-ttu-id="a9b36-132">\_CTOCENTRYLIST CLSID</span><span class="sxs-lookup"><span data-stu-id="a9b36-132">CLSID\_CTocEntryList</span></span>  |
| <span data-ttu-id="a9b36-133">CToc</span><span class="sxs-lookup"><span data-stu-id="a9b36-133">CToc</span></span>           | <span data-ttu-id="a9b36-134">\_CTOC CLSID</span><span class="sxs-lookup"><span data-stu-id="a9b36-134">CLSID\_CToc</span></span>           |
| <span data-ttu-id="a9b36-135">CTocCollection</span><span class="sxs-lookup"><span data-stu-id="a9b36-135">CTocCollection</span></span> | <span data-ttu-id="a9b36-136">\_CTOCCOLLECTION CLSID</span><span class="sxs-lookup"><span data-stu-id="a9b36-136">CLSID\_CTocCollection</span></span> |
| <span data-ttu-id="a9b36-137">CTocParser</span><span class="sxs-lookup"><span data-stu-id="a9b36-137">CTocParser</span></span>     | <span data-ttu-id="a9b36-138">\_CTOCPARSER CLSID</span><span class="sxs-lookup"><span data-stu-id="a9b36-138">CLSID\_CTocParser</span></span>     |



 

### <a name="clsid-constants-defined-in-wmcodecdspuuidlib"></a><span data-ttu-id="a9b36-139">Costanti CLSID definite in Wmcodecdspuuid. lib</span><span class="sxs-lookup"><span data-stu-id="a9b36-139">CLSID Constants Defined in Wmcodecdspuuid.lib</span></span>

<span data-ttu-id="a9b36-140">La costante CLSID seguente è dichiarata, ma non definita, in wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="a9b36-140">The following CLSID constant is declared, but not defined, in wmcodecdsp.h.</span></span> <span data-ttu-id="a9b36-141">Per usarlo nel codice, è necessario eseguire il collegamento a wmcodecdspuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a9b36-141">To use it in code, you must link against wmcodecdspuuid.lib.</span></span>



| <span data-ttu-id="a9b36-142">Nome di classe</span><span class="sxs-lookup"><span data-stu-id="a9b36-142">Class name</span></span>       | <span data-ttu-id="a9b36-143">Costante CLSID</span><span class="sxs-lookup"><span data-stu-id="a9b36-143">CLSID constant</span></span>          |
|------------------|-------------------------|
| <span data-ttu-id="a9b36-144">CTocGeneratorDmo</span><span class="sxs-lookup"><span data-stu-id="a9b36-144">CTocGeneratorDmo</span></span> | <span data-ttu-id="a9b36-145">\_CTOCGENERATORDMO CLSID</span><span class="sxs-lookup"><span data-stu-id="a9b36-145">CLSID\_CTocGeneratorDmo</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="a9b36-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9b36-146">Requirements</span></span>



| <span data-ttu-id="a9b36-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9b36-147">Requirement</span></span> | <span data-ttu-id="a9b36-148">Valore</span><span class="sxs-lookup"><span data-stu-id="a9b36-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9b36-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9b36-149">Minimum supported client</span></span><br/> | <span data-ttu-id="a9b36-150">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a9b36-150">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a9b36-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9b36-151">Minimum supported server</span></span><br/> | <span data-ttu-id="a9b36-152">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a9b36-152">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a9b36-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9b36-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9b36-154"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9b36-154"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="a9b36-155">DLL</span><span class="sxs-lookup"><span data-stu-id="a9b36-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9b36-156"><dt>Wmvdspa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9b36-156"><dt>Wmvdspa.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a9b36-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9b36-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9b36-158">Oggetti parser del sommario</span><span class="sxs-lookup"><span data-stu-id="a9b36-158">Table of Contents Parser Objects</span></span>](toc-parser-objects.md)
</dt> </dl>

 

 




