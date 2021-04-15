---
description: I codici di errore seguenti sono specifici dell'API di installazione.
ms.assetid: C4EB130F-2A83-4A14-BBA8-DB10225D0C0A
title: Codici di errore (API di installazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ce77fd224abb16c519f4b77fa93f775fe203d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485533"
---
# <a name="error-codes-setup-api"></a><span data-ttu-id="e2150-103">Codici di errore (API di installazione)</span><span class="sxs-lookup"><span data-stu-id="e2150-103">Error Codes (Setup API)</span></span>

<span data-ttu-id="e2150-104">I codici di errore seguenti sono specifici dell'API di installazione.</span><span class="sxs-lookup"><span data-stu-id="e2150-104">The following error codes are specific to the Setup API.</span></span>



| <span data-ttu-id="e2150-105">Errori di analisi INF</span><span class="sxs-lookup"><span data-stu-id="e2150-105">INF Parsing Errors</span></span>              | <span data-ttu-id="e2150-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2150-106">Description</span></span>                                                                                                         |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2150-107">ERRORE \_ previsto \_ nome della sezione \_</span><span class="sxs-lookup"><span data-stu-id="e2150-107">ERROR\_EXPECTED\_SECTION\_NAME</span></span>  | <span data-ttu-id="e2150-108">Il nome di una sezione è previsto e non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="e2150-108">A section name was expected and not found.</span></span>                                                                          |
| <span data-ttu-id="e2150-109">\_ \_ \_ riga nome sezione non valida errore \_</span><span class="sxs-lookup"><span data-stu-id="e2150-109">ERROR\_BAD\_SECTION\_NAME\_LINE</span></span> | <span data-ttu-id="e2150-110">Il formato del nome della sezione non è corretto.</span><span class="sxs-lookup"><span data-stu-id="e2150-110">The section name was not of the correct format.</span></span> <span data-ttu-id="e2150-111">(Ad esempio, un nome non terminato da una parentesi graffa destra ( \] ).</span><span class="sxs-lookup"><span data-stu-id="e2150-111">(For example, a name not terminated by a right-hand bracket ( \] ).</span></span> |
| <span data-ttu-id="e2150-112">nome della sezione di errore \_ \_ \_ troppo \_ lungo</span><span class="sxs-lookup"><span data-stu-id="e2150-112">ERROR\_SECTION\_NAME\_TOO\_LONG</span></span> | <span data-ttu-id="e2150-113">Il nome della sezione supera la lunghezza massima del nome della sezione MAX \_ \_ \_ Len.</span><span class="sxs-lookup"><span data-stu-id="e2150-113">The section name exceeded the maximum length of MAX\_SECT\_NAME\_LEN.</span></span>                                               |
| <span data-ttu-id="e2150-114">\_sintassi generale \_ errore</span><span class="sxs-lookup"><span data-stu-id="e2150-114">ERROR\_GENERAL\_SYNTAX</span></span>          | <span data-ttu-id="e2150-115">La sintassi generale non è corretta.</span><span class="sxs-lookup"><span data-stu-id="e2150-115">The general syntax is incorrect.</span></span>                                                                                    |



 



| <span data-ttu-id="e2150-116">Errori di runtime INF</span><span class="sxs-lookup"><span data-stu-id="e2150-116">INF Runtime Errors</span></span>         | <span data-ttu-id="e2150-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2150-117">Description</span></span>                                                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2150-118">ERRORE \_ di \_ tipo inf errato \_</span><span class="sxs-lookup"><span data-stu-id="e2150-118">ERROR\_WRONG\_INF\_STYLE</span></span>   | <span data-ttu-id="e2150-119">Il file INF non è del tipo specificato nella chiamata di funzione.</span><span class="sxs-lookup"><span data-stu-id="e2150-119">The INF file is not of the type specified in the function call.</span></span> <span data-ttu-id="e2150-120">Ad esempio, questo errore può essere restituito dalla funzione [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) se il file inf è destinato a una versione precedente di Windows.</span><span class="sxs-lookup"><span data-stu-id="e2150-120">For example, this error may be returned by the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function if the INF file was intended for an early version of Windows.</span></span> |
| <span data-ttu-id="e2150-121">\_sezione errore \_ non \_ trovata</span><span class="sxs-lookup"><span data-stu-id="e2150-121">ERROR\_SECTION\_NOT\_FOUND</span></span> | <span data-ttu-id="e2150-122">La sezione non è stata trovata nel file INF.</span><span class="sxs-lookup"><span data-stu-id="e2150-122">The section was not found in the INF file.</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="e2150-123">riga di errore \_ \_ non \_ trovata</span><span class="sxs-lookup"><span data-stu-id="e2150-123">ERROR\_LINE\_NOT\_FOUND</span></span>    | <span data-ttu-id="e2150-124">La riga non è stata trovata nella sezione INF.</span><span class="sxs-lookup"><span data-stu-id="e2150-124">The line was not found in the INF section.</span></span>                                                                                                                                                                                                     |



 

 

 



