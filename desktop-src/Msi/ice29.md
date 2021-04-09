---
description: ICE29 convalida che i nomi di flusso troncati rimangano univoci. Viene convalidata qualsiasi tabella con una colonna binaria o oggetto. Vedere il tipo di dati della colonna binary.
ms.assetid: a51b641d-992b-4b6b-a208-d94bc7d05115
title: ICE29
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f606bd09314d045b643816c08349eba38bde72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967144"
---
# <a name="ice29"></a><span data-ttu-id="02abb-105">ICE29</span><span class="sxs-lookup"><span data-stu-id="02abb-105">ICE29</span></span>

<span data-ttu-id="02abb-106">ICE29 convalida che i nomi di flusso troncati rimangano univoci.</span><span class="sxs-lookup"><span data-stu-id="02abb-106">ICE29 validates that truncated stream names remain unique.</span></span> <span data-ttu-id="02abb-107">Viene convalidata qualsiasi tabella con una colonna binaria o oggetto.</span><span class="sxs-lookup"><span data-stu-id="02abb-107">Any table having a Binary or Object column is validated.</span></span> <span data-ttu-id="02abb-108">Vedere il tipo di dati della colonna [Binary](binary.md) .</span><span class="sxs-lookup"><span data-stu-id="02abb-108">See the [Binary](binary.md) column data type.</span></span>

<span data-ttu-id="02abb-109">La gestione dei flussi tramite l'implementazione dell'archiviazione con struttura OLE Win32 limita i nomi di flusso.</span><span class="sxs-lookup"><span data-stu-id="02abb-109">Handling of streams by the Win32 OLE structured storage implementation limits stream names.</span></span> <span data-ttu-id="02abb-110">Vedere [limitazioni OLE sui flussi](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="02abb-110">See [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span> <span data-ttu-id="02abb-111">Il programma di installazione può comprimere i nomi di flusso con una lunghezza di 62 caratteri.</span><span class="sxs-lookup"><span data-stu-id="02abb-111">The installer can compress stream names up to 62 characters in length.</span></span> <span data-ttu-id="02abb-112">I nomi più lunghi di questo sono troncati.</span><span class="sxs-lookup"><span data-stu-id="02abb-112">Names longer than this are truncated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02abb-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="02abb-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02abb-114">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="02abb-114">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



