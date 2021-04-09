---
description: In questa sezione vengono descritte le strutture che è possibile utilizzare per sviluppare parser. Queste strutture sono utilizzate da funzioni che è possibile utilizzare per sviluppare parser e funzioni che è possibile utilizzare per sviluppare parser o esperti.
ms.assetid: ce45a8ef-4355-46fd-909e-3ab4d63a3bf1
title: Strutture del parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a9b767974214472f24ea9e1ec9359c97d26fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968753"
---
# <a name="parser-structures"></a><span data-ttu-id="e2e0b-104">Strutture del parser</span><span class="sxs-lookup"><span data-stu-id="e2e0b-104">Parser Structures</span></span>

<span data-ttu-id="e2e0b-105">In questa sezione vengono descritte le strutture che è possibile utilizzare per sviluppare parser.</span><span class="sxs-lookup"><span data-stu-id="e2e0b-105">This section describes structures you can use to develop parsers.</span></span> <span data-ttu-id="e2e0b-106">Queste strutture sono utilizzate da funzioni che è possibile utilizzare per sviluppare parser e funzioni che è possibile utilizzare per sviluppare parser o esperti.</span><span class="sxs-lookup"><span data-stu-id="e2e0b-106">These structures are used by functions you can use to develop parsers and functions you can use to develop either parsers or experts.</span></span>



| <span data-ttu-id="e2e0b-107">Struttura</span><span class="sxs-lookup"><span data-stu-id="e2e0b-107">Structure</span></span>                                 | <span data-ttu-id="e2e0b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2e0b-108">Description</span></span>                                                                                                                     |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2e0b-109">MACFRAME</span><span class="sxs-lookup"><span data-stu-id="e2e0b-109">MACFRAME</span></span>](macframe.md)                  | <span data-ttu-id="e2e0b-110">Definisce i protocolli iniziali usati più di frequente.</span><span class="sxs-lookup"><span data-stu-id="e2e0b-110">Defines the most commonly used initial protocols.</span></span>                                                                               |
| [<span data-ttu-id="e2e0b-111">ENTRYPOINTS</span><span class="sxs-lookup"><span data-stu-id="e2e0b-111">ENTRYPOINTS</span></span>](entrypoints.md)            | <span data-ttu-id="e2e0b-112">Specifica i puntatori ai punti di ingresso per la DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="e2e0b-112">Specifies pointers to the entry points for the Parser DLL.</span></span>                                                                      |
| [<span data-ttu-id="e2e0b-113">PF \_ FOLLOWENTRY</span><span class="sxs-lookup"><span data-stu-id="e2e0b-113">PF\_FOLLOWENTRY</span></span>](pf-followentry.md)     | <span data-ttu-id="e2e0b-114">Specifica il protocollo che segue il protocollo corrente.</span><span class="sxs-lookup"><span data-stu-id="e2e0b-114">Specifies the protocol that follows the current protocol.</span></span>                                                                       |
| [<span data-ttu-id="e2e0b-115">PF \_</span><span class="sxs-lookup"><span data-stu-id="e2e0b-115">PF\_FOLLOWSET</span></span>](pf-followset.md)         | <span data-ttu-id="e2e0b-116">Specifica il set di protocolli che segue il protocollo corrente.</span><span class="sxs-lookup"><span data-stu-id="e2e0b-116">Specifies the set of protocols that follows the current protocol.</span></span>                                                               |
| [<span data-ttu-id="e2e0b-117">PF \_ HANDOFFENTRY</span><span class="sxs-lookup"><span data-stu-id="e2e0b-117">PF\_HANDOFFENTRY</span></span>](pf-handoffentry.md)   | <span data-ttu-id="e2e0b-118">Specifica il protocollo che passa al protocollo corrente o al protocollo che il protocollo corrente passa a.</span><span class="sxs-lookup"><span data-stu-id="e2e0b-118">Specifies either the protocol that hands off to the current protocol or the protocol that the current protocol hands off to.</span></span>    |
| [<span data-ttu-id="e2e0b-119">PF \_ HANDOFFSET</span><span class="sxs-lookup"><span data-stu-id="e2e0b-119">PF\_HANDOFFSET</span></span>](pf-handoffset.md)       | <span data-ttu-id="e2e0b-120">Specifica il set di protocolli che passa al protocollo corrente o il set di protocolli a cui il protocollo corrente passa.</span><span class="sxs-lookup"><span data-stu-id="e2e0b-120">Specifies the set of protocols that hand off to the current protocol or the set of protocols the current protocol hands off to.</span></span> |
| [<span data-ttu-id="e2e0b-121">PF \_ PARSERDLLINFO</span><span class="sxs-lookup"><span data-stu-id="e2e0b-121">PF\_PARSERDLLINFO</span></span>](pf-parserdllinfo.md) | <span data-ttu-id="e2e0b-122">Specifica il numero di parser nella DLL del parser e le informazioni su ogni parser.</span><span class="sxs-lookup"><span data-stu-id="e2e0b-122">Specifies the number of parsers in the parser DLL and information about each parser.</span></span>                                            |
| [<span data-ttu-id="e2e0b-123">PF \_ PARSERINFO</span><span class="sxs-lookup"><span data-stu-id="e2e0b-123">PF\_PARSERINFO</span></span>](pf-parserinfo.md)       | <span data-ttu-id="e2e0b-124">Specifica le informazioni su un parser specifico.</span><span class="sxs-lookup"><span data-stu-id="e2e0b-124">Specifies information about a specific parser.</span></span>                                                                                  |
| [<span data-ttu-id="e2e0b-125">con etichetta \_ bit</span><span class="sxs-lookup"><span data-stu-id="e2e0b-125">LABELED\_BIT</span></span>](labeled-bit.md)           | <span data-ttu-id="e2e0b-126">Specifica gli handle, i campi di BIT o i flag.</span><span class="sxs-lookup"><span data-stu-id="e2e0b-126">Specifies handles, BIT fields, or flags.</span></span>                                                                                        |
| [<span data-ttu-id="e2e0b-127">BYTE con etichetta \_</span><span class="sxs-lookup"><span data-stu-id="e2e0b-127">LABELED\_BYTE</span></span>](labeled-byte.md)         | <span data-ttu-id="e2e0b-128">Specifica una coppia di etichette di **byte** .</span><span class="sxs-lookup"><span data-stu-id="e2e0b-128">Specifies a **BYTE** label pair.</span></span>                                                                                                |
| [<span data-ttu-id="e2e0b-129">DWORD con etichetta \_</span><span class="sxs-lookup"><span data-stu-id="e2e0b-129">LABELED\_DWORD</span></span>](labeled-dword.md)       | <span data-ttu-id="e2e0b-130">Specifica una coppia di etichette **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="e2e0b-130">Specifies a **DWORD** label pair.</span></span>                                                                                               |
| [<span data-ttu-id="e2e0b-131">parola con etichetta \_</span><span class="sxs-lookup"><span data-stu-id="e2e0b-131">LABELED\_WORD</span></span>](labeled-word.md)         | <span data-ttu-id="e2e0b-132">Specifica una coppia di etichette di **Word** .</span><span class="sxs-lookup"><span data-stu-id="e2e0b-132">Specifies a **WORD** label pair.</span></span>                                                                                                |
| [<span data-ttu-id="e2e0b-133">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="e2e0b-133">PROPERTYINFO</span></span>](propertyinfo.md)          | <span data-ttu-id="e2e0b-134">Specifica le proprietà richieste dal parser di protocollo per descrivere i frame.</span><span class="sxs-lookup"><span data-stu-id="e2e0b-134">Specifies the properties that the protocol parser requires to describe frames.</span></span>                                                  |
| [<span data-ttu-id="e2e0b-135">PROPERTYINST</span><span class="sxs-lookup"><span data-stu-id="e2e0b-135">PROPERTYINST</span></span>](propertyinst.md)          | <span data-ttu-id="e2e0b-136">Specifica un'istanza di una proprietà in un frame.</span><span class="sxs-lookup"><span data-stu-id="e2e0b-136">Specifies an instance of a property in a frame.</span></span>                                                                                 |
| [<span data-ttu-id="e2e0b-137">PROPERTYINSTEX</span><span class="sxs-lookup"><span data-stu-id="e2e0b-137">PROPERTYINSTEX</span></span>](propertyinstex.md)      | <span data-ttu-id="e2e0b-138">Specifica un'istanza di proprietà estesa in formato libero.</span><span class="sxs-lookup"><span data-stu-id="e2e0b-138">Specifies a free-form, extended property instance.</span></span>                                                                              |
| [<span data-ttu-id="e2e0b-139">PROTOCOLINFO</span><span class="sxs-lookup"><span data-stu-id="e2e0b-139">PROTOCOLINFO</span></span>](protocolinfo.md)          | <span data-ttu-id="e2e0b-140">Specifica un protocollo.</span><span class="sxs-lookup"><span data-stu-id="e2e0b-140">Specifies a protocol.</span></span>                                                                                                           |
| [<span data-ttu-id="e2e0b-141">INTERVALLO</span><span class="sxs-lookup"><span data-stu-id="e2e0b-141">RANGE</span></span>](range.md)                        | <span data-ttu-id="e2e0b-142">Specifica un intervallo per un numero.</span><span class="sxs-lookup"><span data-stu-id="e2e0b-142">Specifies a range for a number.</span></span>                                                                                                 |
| [<span data-ttu-id="e2e0b-143">SET</span><span class="sxs-lookup"><span data-stu-id="e2e0b-143">SET</span></span>](set.md)                            | <span data-ttu-id="e2e0b-144">Specifica una tabella di valori per una proprietà.</span><span class="sxs-lookup"><span data-stu-id="e2e0b-144">Specifies a table of values for a property.</span></span>                                                                                     |



 

<span data-ttu-id="e2e0b-145">Per informazioni sulle funzioni usate per lo sviluppo di dll del parser, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="e2e0b-145">For information about functions used to develop parser DLLs, see the following topics.</span></span>



| <span data-ttu-id="e2e0b-146">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="e2e0b-146">For information about</span></span>                                         | <span data-ttu-id="e2e0b-147">Vedere</span><span class="sxs-lookup"><span data-stu-id="e2e0b-147">See</span></span>                                                                          |
|---------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e2e0b-148">Funzioni che vengono esportate dalle DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="e2e0b-148">Functions that the parser DLLs export.</span></span>                        | [<span data-ttu-id="e2e0b-149">Funzioni di esportazione DLL del parser</span><span class="sxs-lookup"><span data-stu-id="e2e0b-149">Parser DLL Export Functions</span></span>](parser-dll-export-functions.md)               |
| <span data-ttu-id="e2e0b-150">Funzioni che è possibile usare per sviluppare dll del parser.</span><span class="sxs-lookup"><span data-stu-id="e2e0b-150">Functions that you can use to develop parser DLLs.</span></span>            | [<span data-ttu-id="e2e0b-151">Funzioni del parser</span><span class="sxs-lookup"><span data-stu-id="e2e0b-151">Parser Functions</span></span>](parser-functions.md)                                     |
| <span data-ttu-id="e2e0b-152">Funzioni che è possibile usare per sviluppare dll di parser ed esperti.</span><span class="sxs-lookup"><span data-stu-id="e2e0b-152">Functions that you can use to develop parser and expert DLLs.</span></span> | [<span data-ttu-id="e2e0b-153">Funzioni comuni di esperti e parser</span><span class="sxs-lookup"><span data-stu-id="e2e0b-153">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |



 

 

 



