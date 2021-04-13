---
title: Funzioni ADSI
description: Active Directory interfacce del servizio espongono le funzioni di supporto seguenti ai client che non utilizzano l'automazione.
ms.assetid: 4f0e90e2-afcc-4cf7-a731-9b38a83ca229
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, informazioni di riferimento, funzioni
- ADSI funzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c814cf4f59a391a3242fa748856eaacb35dbcc53
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328444"
---
# <a name="adsi-functions"></a><span data-ttu-id="64580-105">Funzioni ADSI</span><span class="sxs-lookup"><span data-stu-id="64580-105">ADSI Functions</span></span>

<span data-ttu-id="64580-106">Active Directory interfacce del servizio espongono le funzioni di supporto seguenti ai client che non utilizzano l'automazione.</span><span class="sxs-lookup"><span data-stu-id="64580-106">Active Directory Service Interfaces expose the following helper functions to clients that do not use Automation.</span></span>



| <span data-ttu-id="64580-107">Funzione</span><span class="sxs-lookup"><span data-stu-id="64580-107">Function</span></span>                                           | <span data-ttu-id="64580-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64580-108">Description</span></span>                                                                                        |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64580-109">**ADsBuildEnumerator**</span><span class="sxs-lookup"><span data-stu-id="64580-109">**ADsBuildEnumerator**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator)   | <span data-ttu-id="64580-110">Crea un oggetto enumeratore per l'oggetto contenitore ADSI specificato.</span><span class="sxs-lookup"><span data-stu-id="64580-110">Creates an enumerator object for the specified ADSI container object.</span></span>                              |
| [<span data-ttu-id="64580-111">**ADsBuildVarArrayInt**</span><span class="sxs-lookup"><span data-stu-id="64580-111">**ADsBuildVarArrayInt**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararrayint) | <span data-ttu-id="64580-112">Compila una matrice Variant da una matrice di **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="64580-112">Builds a variant array from an array of **DWORD** s.</span></span>                                                |
| [<span data-ttu-id="64580-113">**ADsBuildVarArrayStr**</span><span class="sxs-lookup"><span data-stu-id="64580-113">**ADsBuildVarArrayStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararraystr) | <span data-ttu-id="64580-114">Compila una matrice Variant da una matrice di stringhe Unicode.</span><span class="sxs-lookup"><span data-stu-id="64580-114">Builds a variant array from an array of Unicode strings.</span></span>                                           |
| [<span data-ttu-id="64580-115">**ADsEncodeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="64580-115">**ADsEncodeBinaryData**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) | <span data-ttu-id="64580-116">Converte un BLOB di dati binari nel formato appropriato per un filtro di ricerca.</span><span class="sxs-lookup"><span data-stu-id="64580-116">Converts a blob of binary data to the format suitable for a search filter.</span></span>                         |
| [<span data-ttu-id="64580-117">**ADsEnumerateNext**</span><span class="sxs-lookup"><span data-stu-id="64580-117">**ADsEnumerateNext**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)       | <span data-ttu-id="64580-118">Popola una matrice Variant con gli elementi recuperati dall'oggetto enumeratore specificato.</span><span class="sxs-lookup"><span data-stu-id="64580-118">Populates a variant array with elements retrieved from the specified enumerator object.</span></span>            |
| [<span data-ttu-id="64580-119">**ADsFreeEnumerator**</span><span class="sxs-lookup"><span data-stu-id="64580-119">**ADsFreeEnumerator**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator)     | <span data-ttu-id="64580-120">Libera un oggetto enumeratore creato in precedenza da [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator).</span><span class="sxs-lookup"><span data-stu-id="64580-120">Frees an enumerator object previously created by [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator).</span></span> |
| [<span data-ttu-id="64580-121">**ADsGetLastError**</span><span class="sxs-lookup"><span data-stu-id="64580-121">**ADsGetLastError**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror)         | <span data-ttu-id="64580-122">Recupera l'ultimo valore del codice di errore del thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="64580-122">Retrieves the last error code value of the calling thread.</span></span>                                         |
| [<span data-ttu-id="64580-123">**ADsGetObject**</span><span class="sxs-lookup"><span data-stu-id="64580-123">**ADsGetObject**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)               | <span data-ttu-id="64580-124">Esegue l'associazione a un oggetto ADSI utilizzando le credenziali correnti.</span><span class="sxs-lookup"><span data-stu-id="64580-124">Binds to an ADSI object using the current credentials.</span></span>                                             |
| [<span data-ttu-id="64580-125">**ADsOpenObject**</span><span class="sxs-lookup"><span data-stu-id="64580-125">**ADsOpenObject**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)             | <span data-ttu-id="64580-126">Esegue l'associazione a un oggetto ADSI utilizzando le credenziali specificate</span><span class="sxs-lookup"><span data-stu-id="64580-126">Binds to an ADSI object using specified credentials</span></span>                                                |
| [<span data-ttu-id="64580-127">**ADsSetLastError**</span><span class="sxs-lookup"><span data-stu-id="64580-127">**ADsSetLastError**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adssetlasterror)         | <span data-ttu-id="64580-128">Imposta il valore del codice di errore del thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="64580-128">Sets the error code value of the calling thread.</span></span>                                                   |
| [<span data-ttu-id="64580-129">**AllocADsMem**</span><span class="sxs-lookup"><span data-stu-id="64580-129">**AllocADsMem**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem)                 | <span data-ttu-id="64580-130">Alloca un blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="64580-130">Allocates a block of memory.</span></span>                                                                       |
| [<span data-ttu-id="64580-131">**AllocADsStr**</span><span class="sxs-lookup"><span data-stu-id="64580-131">**AllocADsStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-allocadsstr)                 | <span data-ttu-id="64580-132">Alloca memoria per una determinata stringa.</span><span class="sxs-lookup"><span data-stu-id="64580-132">Allocates memory for a given string.</span></span>                                                               |
| [<span data-ttu-id="64580-133">**FreeADsMem**</span><span class="sxs-lookup"><span data-stu-id="64580-133">**FreeADsMem**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem)                   | <span data-ttu-id="64580-134">Libera la memoria allocata da [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem).</span><span class="sxs-lookup"><span data-stu-id="64580-134">Frees the memory allocated by [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem).</span></span>                                  |
| [<span data-ttu-id="64580-135">**FreeADsStr**</span><span class="sxs-lookup"><span data-stu-id="64580-135">**FreeADsStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-freeadsstr)                   | <span data-ttu-id="64580-136">Libera la memoria allocata per la stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="64580-136">Frees the memory allocated for the given string.</span></span>                                                   |
| [<span data-ttu-id="64580-137">**ReallocADsMem**</span><span class="sxs-lookup"><span data-stu-id="64580-137">**ReallocADsMem**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsmem)             | <span data-ttu-id="64580-138">Assegna il contenuto di memoria esistente a una posizione di memoria appena creata.</span><span class="sxs-lookup"><span data-stu-id="64580-138">Assigns the existing memory content to a newly created memory location.</span></span>                            |
| [<span data-ttu-id="64580-139">**ReallocADsStr**</span><span class="sxs-lookup"><span data-stu-id="64580-139">**ReallocADsStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsstr)             | <span data-ttu-id="64580-140">Sostituisce una stringa esistente con una nuova.</span><span class="sxs-lookup"><span data-stu-id="64580-140">Replaces an existing string with a new one.</span></span>                                                        |



 

<span data-ttu-id="64580-141">Le funzioni ADSI seguenti sono obsolete.</span><span class="sxs-lookup"><span data-stu-id="64580-141">The following ADSI functions are obsolete.</span></span>



| <span data-ttu-id="64580-142">Funzione</span><span class="sxs-lookup"><span data-stu-id="64580-142">Function</span></span>                                                  | <span data-ttu-id="64580-143">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64580-143">Description</span></span> |
|-----------------------------------------------------------|-------------|
| [<span data-ttu-id="64580-144">**AdsFreeAllErrorRecords**</span><span class="sxs-lookup"><span data-stu-id="64580-144">**AdsFreeAllErrorRecords**</span></span>](obsolete-adsi-functions.md) | <span data-ttu-id="64580-145">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="64580-145">Obsolete.</span></span>   |
| [<span data-ttu-id="64580-146">**AdsDecodeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="64580-146">**AdsDecodeBinaryData**</span></span>](obsolete-adsi-functions.md)    | <span data-ttu-id="64580-147">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="64580-147">Obsolete.</span></span>   |
| [<span data-ttu-id="64580-148">**PropVariantToAdsType**</span><span class="sxs-lookup"><span data-stu-id="64580-148">**PropVariantToAdsType**</span></span>](obsolete-adsi-functions.md)   | <span data-ttu-id="64580-149">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="64580-149">Obsolete.</span></span>   |
| [<span data-ttu-id="64580-150">**AdsTypeToPropVariant**</span><span class="sxs-lookup"><span data-stu-id="64580-150">**AdsTypeToPropVariant**</span></span>](obsolete-adsi-functions.md)   | <span data-ttu-id="64580-151">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="64580-151">Obsolete.</span></span>   |
| [<span data-ttu-id="64580-152">**AdsFreeAdsValues**</span><span class="sxs-lookup"><span data-stu-id="64580-152">**AdsFreeAdsValues**</span></span>](obsolete-adsi-functions.md)       | <span data-ttu-id="64580-153">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="64580-153">Obsolete.</span></span>   |
| [<span data-ttu-id="64580-154">**InitAdsMem**</span><span class="sxs-lookup"><span data-stu-id="64580-154">**InitAdsMem**</span></span>](obsolete-adsi-functions.md)             | <span data-ttu-id="64580-155">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="64580-155">Obsolete.</span></span>   |
| [<span data-ttu-id="64580-156">**AssertAdsmemLeaks**</span><span class="sxs-lookup"><span data-stu-id="64580-156">**AssertAdsmemLeaks**</span></span>](obsolete-adsi-functions.md)      | <span data-ttu-id="64580-157">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="64580-157">Obsolete.</span></span>   |
| [<span data-ttu-id="64580-158">**DumpMemorytracker**</span><span class="sxs-lookup"><span data-stu-id="64580-158">**DumpMemorytracker**</span></span>](obsolete-adsi-functions.md)      | <span data-ttu-id="64580-159">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="64580-159">Obsolete.</span></span>   |



 

 

 




