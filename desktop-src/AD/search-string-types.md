---
title: Stringhe di ricerca iniziali, mediali e finali
description: Sono disponibili tre tipi di ricerche con caratteri jolly a cui viene fatto riferimento in tutta la documentazione relativa alle query sulle stringhe di ricerca per la costruzione. Queste ricerche con caratteri jolly sono stringhe iniziali, mediali e di ricerca finale. In questo argomento vengono descritte queste ricerche.
ms.assetid: 23cc4771-2dd6-478c-9c7a-43052594cb71
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f502753a87afc81856524c7ae5565db3af678d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297719"
---
# <a name="initial-medial-and-final-search-strings"></a><span data-ttu-id="0e7db-105">Stringhe di ricerca iniziali, mediali e finali</span><span class="sxs-lookup"><span data-stu-id="0e7db-105">Initial, Medial, and Final Search Strings</span></span>

<span data-ttu-id="0e7db-106">Sono disponibili tre tipi di ricerche con caratteri jolly a cui viene fatto riferimento in tutta la documentazione relativa alle query sulle stringhe di ricerca per la costruzione.</span><span class="sxs-lookup"><span data-stu-id="0e7db-106">There are three types of wildcard searches that are referenced throughout the documentation about construction search string queries.</span></span> <span data-ttu-id="0e7db-107">Queste ricerche con caratteri jolly sono: stringhe iniziali, mediali e di ricerca finale.</span><span class="sxs-lookup"><span data-stu-id="0e7db-107">These wildcard searches are: initial-, medial-, and final-search strings.</span></span> <span data-ttu-id="0e7db-108">In questo argomento vengono descritte queste ricerche.</span><span class="sxs-lookup"><span data-stu-id="0e7db-108">This topics describes these searches.</span></span>

## <a name="initial-search-strings"></a><span data-ttu-id="0e7db-109">Stringhe di ricerca iniziali</span><span class="sxs-lookup"><span data-stu-id="0e7db-109">Initial Search Strings</span></span>

<span data-ttu-id="0e7db-110">Le stringhe di ricerca iniziali corrispondono a un set di caratteri specificato all'inizio di una stringa, seguito da un carattere jolly.</span><span class="sxs-lookup"><span data-stu-id="0e7db-110">Initial-search strings match a given set of characters at the beginning of a string, followed by a wildcard.</span></span> <span data-ttu-id="0e7db-111">Ad esempio, la stringa di ricerca iniziale `Act*` corrisponderà a "Active Directory".</span><span class="sxs-lookup"><span data-stu-id="0e7db-111">For example, the initial-search string `Act*` would match "Active Directory".</span></span>

## <a name="medial-search-strings"></a><span data-ttu-id="0e7db-112">Stringhe di Medial-Search</span><span class="sxs-lookup"><span data-stu-id="0e7db-112">Medial-Search Strings</span></span>

<span data-ttu-id="0e7db-113">Le stringhe di ricerca mediale corrispondono a un determinato set di caratteri all'interno di una stringa, preceduto da e/o seguito da un carattere jolly.</span><span class="sxs-lookup"><span data-stu-id="0e7db-113">Medial-search strings match a given set of characters in the middle of a string, preceded by and/or followed by a wildcard.</span></span> <span data-ttu-id="0e7db-114">Le stringhe di ricerca mediale `*Dir*` , `*ive*Dir*` e `*ve*Dir*tor*` corrisponderanno a "Active Directory".</span><span class="sxs-lookup"><span data-stu-id="0e7db-114">The medial-search strings `*Dir*`, `*ive*Dir*`, and `*ve*Dir*tor*` would all match "Active Directory".</span></span>

## <a name="final-search-strings"></a><span data-ttu-id="0e7db-115">Ultime-stringhe di ricerca</span><span class="sxs-lookup"><span data-stu-id="0e7db-115">Final-search Strings</span></span>

<span data-ttu-id="0e7db-116">Le stringhe di ricerca finale corrispondono a un set di caratteri specificato alla fine di una stringa, preceduta da un carattere jolly.</span><span class="sxs-lookup"><span data-stu-id="0e7db-116">Final-search strings match a given set of characters at the end of a string, preceded by a wildcard.</span></span> <span data-ttu-id="0e7db-117">Ad esempio, la stringa di ricerca finale `*ory` corrisponderà a "Active Directory".</span><span class="sxs-lookup"><span data-stu-id="0e7db-117">For example, the final-search string `*ory` would match "Active Directory".</span></span>

 

 




