---
title: Top-Level e puntatori incorporati
description: Per comprendere il modo in cui i puntatori e gli elementi dati associati vengono allocati in Microsoft RPC, è necessario distinguere tra puntatori di primo livello e puntatori incorporati.
ms.assetid: 217b9200-827c-4d36-9412-5e65858b8a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee84fcecdb70c67d7c99b4bbd3753c244a87cd07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471675"
---
# <a name="top-level-and-embedded-pointers"></a><span data-ttu-id="6df9f-103">Top-Level e puntatori incorporati</span><span class="sxs-lookup"><span data-stu-id="6df9f-103">Top-Level and Embedded Pointers</span></span>

<span data-ttu-id="6df9f-104">Per comprendere il modo in cui i puntatori e gli elementi dati associati vengono allocati in Microsoft RPC, è necessario distinguere tra *puntatori di primo livello* e *puntatori incorporati*.</span><span class="sxs-lookup"><span data-stu-id="6df9f-104">To understand how pointers and their associated data elements are allocated in Microsoft RPC, you have to differentiate between *top-level pointers* and *embedded pointers*.</span></span> <span data-ttu-id="6df9f-105">È inoltre utile fare riferimento al set di tutti i puntatori che non sono puntatori di primo livello.</span><span class="sxs-lookup"><span data-stu-id="6df9f-105">It is also useful to refer to the set of all pointers that are not top-level pointers.</span></span>

<span data-ttu-id="6df9f-106">I *puntatori di primo livello* sono quelli specificati come nomi dei parametri nei prototipi di funzione.</span><span class="sxs-lookup"><span data-stu-id="6df9f-106">*Top-level pointers* are those that are specified as the names of parameters in function prototypes.</span></span> <span data-ttu-id="6df9f-107">I puntatori di primo livello e i relativi riferimenti sono sempre allocati nel server.</span><span class="sxs-lookup"><span data-stu-id="6df9f-107">Top-level pointers and their referents are always allocated on the server.</span></span>

<span data-ttu-id="6df9f-108">I *puntatori incorporati* sono puntatori incorporati in strutture di dati quali matrici, strutture e unioni.</span><span class="sxs-lookup"><span data-stu-id="6df9f-108">*Embedded pointers* are pointers that are embedded in data structures such as arrays, structures, and unions.</span></span> <span data-ttu-id="6df9f-109">Quando i puntatori incorporati scrivono solo l'output in un buffer e sono null nell'input, l'applicazione server può modificare i valori in un valore diverso da null.</span><span class="sxs-lookup"><span data-stu-id="6df9f-109">When embedded pointers only write output to a buffer and are null on input, the server application can change their values to non-null.</span></span> <span data-ttu-id="6df9f-110">In questo caso, gli stub client allocano la nuova memoria per questi dati.</span><span class="sxs-lookup"><span data-stu-id="6df9f-110">In this case, the client stubs allocate new memory for this data.</span></span>

<span data-ttu-id="6df9f-111">Se il puntatore incorporato non è null nel client prima della chiamata, gli stub non allocano memoria sul client al ritorno.</span><span class="sxs-lookup"><span data-stu-id="6df9f-111">If the embedded pointer is not null on the client before the call, the stubs do not allocate memory on the client on return.</span></span> <span data-ttu-id="6df9f-112">Al contrario, gli stub tentano di scrivere la memoria associata al puntatore incorporato nella memoria esistente sul client associato a tale puntatore, sovrascrivendo i dati già presenti.</span><span class="sxs-lookup"><span data-stu-id="6df9f-112">Instead, the stubs attempt to write the memory associated with the embedded pointer into the existing memory on the client associated with that pointer, overwriting the data already there.</span></span>

> [!Note]  
> <span data-ttu-id="6df9f-113">Per i dati letti o scritti in un buffer e che non specifica le dimensioni del buffer, la lunghezza di output deve essere minore o uguale alla lunghezza di input.</span><span class="sxs-lookup"><span data-stu-id="6df9f-113">For data read from or writen to a buffer, and which does not specify the buffer size, output length must be less than or equal to input length.</span></span> <span data-ttu-id="6df9f-114">Viene generata un'eccezione RPC quando viene rilevato un overflow.</span><span class="sxs-lookup"><span data-stu-id="6df9f-114">An RPC exception is raised when overflow is detected.</span></span> <span data-ttu-id="6df9f-115">Per i dati di stringa, la lunghezza di output viene determinata controllando la lunghezza della stringa di input.</span><span class="sxs-lookup"><span data-stu-id="6df9f-115">For string data, output length is determined by checking length of the input string.</span></span> <span data-ttu-id="6df9f-116">Pertanto, le stringhe di output non possono superare la lunghezza delle stringhe di input.</span><span class="sxs-lookup"><span data-stu-id="6df9f-116">Therefore, output strings cannot exceed length of input strings.</span></span> <span data-ttu-id="6df9f-117">Le procedure consigliate consentono di evitare questo problema includendo sempre un parametro specificato per le dimensioni per indicare le dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="6df9f-117">Best practice guidance is to avoid this by always including a size-specified parameter to indicate size of the buffer.</span></span>

 

<span data-ttu-id="6df9f-118">I puntatori di sola scrittura incorporati vengono descritti nella [combinazione di attributi direzionali e direzionali](combining-pointer-and-directional-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="6df9f-118">Embedded write-only pointers are discussed in [Combining Pointer and Directional Attributes](combining-pointer-and-directional-attributes.md).</span></span>

<span data-ttu-id="6df9f-119">Il termine *puntatori a livello di nontop* fa riferimento a tutti i puntatori che non sono specificati come nomi di parametro nel prototipo di funzione, inclusi i puntatori incorporati e più livelli di puntatori annidati.</span><span class="sxs-lookup"><span data-stu-id="6df9f-119">The term *nontop-level pointers* refers to all pointers that are not specified as parameter names in the function prototype, including both embedded pointers and multiple levels of nested pointers.</span></span>

 

 




