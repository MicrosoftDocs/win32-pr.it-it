---
description: 'Il riconoscitore gestisce:'
ms.assetid: d7c694a2-0da6-4172-b434-2b0f94e1b649
title: Riferimento al riconoscimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e193b6098f6d82751951d1a39630ad30023c84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058282"
---
# <a name="recognizer-reference"></a><span data-ttu-id="3abe6-103">Riferimento al riconoscimento</span><span class="sxs-lookup"><span data-stu-id="3abe6-103">Recognizer Reference</span></span>

<span data-ttu-id="3abe6-104">Il riconoscitore gestisce:</span><span class="sxs-lookup"><span data-stu-id="3abe6-104">The recognizer handles:</span></span>

-   <span data-ttu-id="3abe6-105">Determinare quali riconoscitori sono disponibili nel computer.</span><span class="sxs-lookup"><span data-stu-id="3abe6-105">Determine which recognizers are available on the computer.</span></span>
-   <span data-ttu-id="3abe6-106">Identificare il riconoscimento da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="3abe6-106">Identify which recognizer to use.</span></span>
-   <span data-ttu-id="3abe6-107">Creare un contesto del riconoscitore.</span><span class="sxs-lookup"><span data-stu-id="3abe6-107">Create a recognizer context.</span></span>
-   <span data-ttu-id="3abe6-108">Recuperare i risultati del riconoscimento e le alternative.</span><span class="sxs-lookup"><span data-stu-id="3abe6-108">Retrieve recognizer results and alternates.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3abe6-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="3abe6-109">In This Section</span></span>



| <span data-ttu-id="3abe6-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="3abe6-110">Topic</span></span>                                                      | <span data-ttu-id="3abe6-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3abe6-111">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3abe6-112">Handle HRECOALT</span><span class="sxs-lookup"><span data-stu-id="3abe6-112">HRECOALT Handle</span></span>](hrecoalt-handle.md)                     | <span data-ttu-id="3abe6-113">Recupera i valori di stringa e proprietà alternativi, ad esempio il livello di confidenza e le metriche.</span><span class="sxs-lookup"><span data-stu-id="3abe6-113">Retrieves the alternate string and property values, such as confidence level and metrics.</span></span><br/>                                                                  |
| [<span data-ttu-id="3abe6-114">Handle HRECOCONTEXT</span><span class="sxs-lookup"><span data-stu-id="3abe6-114">HRECOCONTEXT Handle</span></span>](hrecocontext-handle.md)             | <span data-ttu-id="3abe6-115">Aggiunge input penna al contesto, esegue il riconoscimento dell'input penna e recupera il risultato del riconoscimento e le alternative.</span><span class="sxs-lookup"><span data-stu-id="3abe6-115">Adds ink to the context, performs ink recognition, and retrieves the recognition result and alternates.</span></span><br/>                                                    |
| [<span data-ttu-id="3abe6-116">Handle HRECOGNIZER</span><span class="sxs-lookup"><span data-stu-id="3abe6-116">HRECOGNIZER Handle</span></span>](hrecognizer-handle.md)               | <span data-ttu-id="3abe6-117">Consente di creare un contesto di riconoscimento, di recuperarne gli attributi e delle proprietà e di determinare le proprietà dei pacchetti necessarie al riconoscimento per eseguire il riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="3abe6-117">Creates a recognizer context, retrieves its attributes and properties, and determines which packet properties the recognizer needs to perform recognition.</span></span><br/> |
| [<span data-ttu-id="3abe6-118">Handle HRECOWORDLIST</span><span class="sxs-lookup"><span data-stu-id="3abe6-118">HRECOWORDLIST Handle</span></span>](hrecowordlist-handle.md)           | <span data-ttu-id="3abe6-119">Gestisce un elenco di parole che è possibile connettersi a un contesto di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="3abe6-119">Manages a word list that you attach to a recognizer context.</span></span> <span data-ttu-id="3abe6-120">Questo elenco migliora i risultati del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="3abe6-120">This list improves the recognition results.</span></span><br/>                                                   |
| [<span data-ttu-id="3abe6-121">Enumerazioni di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="3abe6-121">Recognizer Enumerations</span></span>](recognizer-api-enumerations.md) | <span data-ttu-id="3abe6-122">Descrive i tipi di enumerazione del riconoscitore.</span><span class="sxs-lookup"><span data-stu-id="3abe6-122">Describes the recognizer enumeration types.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="3abe6-123">Strutture di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="3abe6-123">Recognizer Structures</span></span>](recognizer-api-structures.md)     | <span data-ttu-id="3abe6-124">Descrive le strutture di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="3abe6-124">Describes the recognizer structures.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="3abe6-125">GUID del riconoscitore</span><span class="sxs-lookup"><span data-stu-id="3abe6-125">Recognizer GUIDs</span></span>](recognizer-guids.md)                   | <span data-ttu-id="3abe6-126">Specifica il tipo di proprietà per le proprietà del pacchetto e le proprietà del riconoscitore.</span><span class="sxs-lookup"><span data-stu-id="3abe6-126">Specifies the type of property for packet properties and recognizer properties.</span></span><br/>                                                                            |



 

 

 




