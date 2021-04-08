---
title: Attributi relativi alle prestazioni
description: Utilizzare i seguenti attributi in un file IDL per ridurre le dimensioni del codice stub o per migliorare le prestazioni.
ms.assetid: 0f23265e-7f3e-4a15-ac3b-1d852a8110eb
keywords:
- MIDL, attributi e prestazioni di IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbfa518b400d237c9fd3789f61b7e74a0c38276
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045353"
---
# <a name="performance-attributes"></a><span data-ttu-id="b638f-104">Attributi relativi alle prestazioni</span><span class="sxs-lookup"><span data-stu-id="b638f-104">Performance Attributes</span></span>

<span data-ttu-id="b638f-105">Utilizzare i seguenti attributi in un file IDL per ridurre le dimensioni del codice stub o per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="b638f-105">Use the following attributes in an IDL file to reduce the size of the stub code or otherwise improve performance.</span></span>



| <span data-ttu-id="b638f-106">Attributo</span><span class="sxs-lookup"><span data-stu-id="b638f-106">Attribute</span></span>                             | <span data-ttu-id="b638f-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="b638f-107">Usage</span></span>                                                                                                                                                |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b638f-108">**ignorare**</span><span class="sxs-lookup"><span data-stu-id="b638f-108">**ignore**</span></span>](ignore.md)              | <span data-ttu-id="b638f-109">Indica che un puntatore contenuto in una struttura o in un'Unione e l'oggetto indicato dal puntatore non devono essere trasmessi.</span><span class="sxs-lookup"><span data-stu-id="b638f-109">Designates that a pointer contained in a structure or union and the object indicated by the pointer is not to be transmitted.</span></span>                        |
| [<span data-ttu-id="b638f-110">**locale**</span><span class="sxs-lookup"><span data-stu-id="b638f-110">**local**</span></span>](local.md)                | <span data-ttu-id="b638f-111">Definisce una funzione locale per l'applicazione per la quale MIDL non deve generare codice stub.</span><span class="sxs-lookup"><span data-stu-id="b638f-111">Designates a function that is local to the application for which MIDL does not need to generate stub code.</span></span>                                           |
| [<span data-ttu-id="b638f-112">**\_marshalling di rete**</span><span class="sxs-lookup"><span data-stu-id="b638f-112">**wire\_marshal**</span></span>](wire-marshal.md) | <span data-ttu-id="b638f-113">Definisce un tipo di dati come tipo più semplice per la trasmissione in rete e consente di implementare routine di marshalling e di unmarshalling per il tipo.</span><span class="sxs-lookup"><span data-stu-id="b638f-113">Defines a data type as a simpler type for transmission over a network and allows you to implement marshaling and unmarshaling routines for the type.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b638f-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b638f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b638f-115">Attributi ACF di gestione della memoria</span><span class="sxs-lookup"><span data-stu-id="b638f-115">Memory Management ACF Attributes</span></span>](memory-management-acf-attributes.md)
</dt> <dt>

[<span data-ttu-id="b638f-116">Attributi ACF di ottimizzazione Stub</span><span class="sxs-lookup"><span data-stu-id="b638f-116">Stub Optimization ACF Attributes</span></span>](stub-optimization-acf-attributes.md)
</dt> </dl>

 

 




