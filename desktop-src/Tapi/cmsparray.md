---
description: Il modello CMSPArray implementa una Smart Array che aumenterà su richiesta.
ms.assetid: 9b30885c-01a4-4aea-a1c3-5d7966e4697f
title: CMSPArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a6c14d4bdc0b57a295efa5bcc2adfd79d23d31d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967601"
---
# <a name="cmsparray"></a><span data-ttu-id="b78ad-103">CMSPArray</span><span class="sxs-lookup"><span data-stu-id="b78ad-103">CMSPArray</span></span>

<span data-ttu-id="b78ad-104">Il modello CMSPArray implementa una Smart Array che aumenterà su richiesta.</span><span class="sxs-lookup"><span data-stu-id="b78ad-104">The CMSPArray template implements a smart array that will grow on demand.</span></span> <span data-ttu-id="b78ad-105">È progettato per mantenere piccole matrici con tipi di dati semplici.</span><span class="sxs-lookup"><span data-stu-id="b78ad-105">It is designed to hold small arrays with simple data types.</span></span> <span data-ttu-id="b78ad-106">Non ha una sezione critica.</span><span class="sxs-lookup"><span data-stu-id="b78ad-106">It doesn't have a critical section.</span></span> <span data-ttu-id="b78ad-107">Le uniche dipendenze sono **realloc** e **memmove**.</span><span class="sxs-lookup"><span data-stu-id="b78ad-107">Its only dependencies are **realloc** and **memmove**.</span></span> <span data-ttu-id="b78ad-108">Viene usato internamente per contenere elenchi di puntatori a oggetti.</span><span class="sxs-lookup"><span data-stu-id="b78ad-108">It is used internally to keep lists of object pointers.</span></span> <span data-ttu-id="b78ad-109">È simile all'implementazione **CSimpleArray** di ATL, ma è più efficiente per le allocazioni iniziali.</span><span class="sxs-lookup"><span data-stu-id="b78ad-109">It is similar to ATL's **CSimpleArray** implementation, but it is more efficient for initial allocations.</span></span>

<span data-ttu-id="b78ad-110">Questo modello è definito in MSPutils. h.</span><span class="sxs-lookup"><span data-stu-id="b78ad-110">This template is defined in MSPutils.h.</span></span>

 

 



