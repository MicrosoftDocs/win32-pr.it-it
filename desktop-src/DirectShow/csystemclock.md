---
description: La classe CSystemClock implementa un clock che restituisce l'ora di sistema.
ms.assetid: 22f8b641-6472-433f-bff4-4e62eae25c9b
title: Classe CSystemClock
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock
api_type:
- COM
api_location: ''
ms.openlocfilehash: e9cc5e0bde8983cfd8c544d3898d4af628e10f87
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104551309"
---
# <a name="csystemclock-class"></a><span data-ttu-id="2487b-103">Classe CSystemClock</span><span class="sxs-lookup"><span data-stu-id="2487b-103">CSystemClock class</span></span>

![gerarchia di classi csystemclock](images/sclock01.png)

<span data-ttu-id="2487b-105">La `CSystemClock` classe implementa un clock che restituisce l'ora di sistema.</span><span class="sxs-lookup"><span data-stu-id="2487b-105">The `CSystemClock` class implements a clock that returns the system time.</span></span>

<span data-ttu-id="2487b-106">Questa classe deriva dalla classe [**CBaseReferenceClock**](cbasereferenceclock.md) e aggiunge il supporto per le interfacce **IPersist** e [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) .</span><span class="sxs-lookup"><span data-stu-id="2487b-106">This class derives from the [**CBaseReferenceClock**](cbasereferenceclock.md) class, and adds support for the **IPersist** and [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) interfaces.</span></span>



| <span data-ttu-id="2487b-107">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="2487b-107">Public Methods</span></span>                                        | <span data-ttu-id="2487b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2487b-108">Description</span></span>                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="2487b-109">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="2487b-109">**CreateInstance**</span></span>](csystemclock-createinstance.md) | <span data-ttu-id="2487b-110">Crea una nuova istanza di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="2487b-110">Creates a new instance of this object.</span></span>              |
| [<span data-ttu-id="2487b-111">**CSystemClock**</span><span class="sxs-lookup"><span data-stu-id="2487b-111">**CSystemClock**</span></span>](csystemclock-csystemclock.md)     | <span data-ttu-id="2487b-112">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="2487b-112">Constructor method.</span></span>                                 |
| <span data-ttu-id="2487b-113">Metodi IAMClockAdjust</span><span class="sxs-lookup"><span data-stu-id="2487b-113">IAMClockAdjust Methods</span></span>                                | <span data-ttu-id="2487b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2487b-114">Description</span></span>                                         |
| [<span data-ttu-id="2487b-115">**SetClockDelta**</span><span class="sxs-lookup"><span data-stu-id="2487b-115">**SetClockDelta**</span></span>](csystemclock-setclockdelta.md)   | <span data-ttu-id="2487b-116">Regola l'ora dell'orologio.</span><span class="sxs-lookup"><span data-stu-id="2487b-116">Adjusts the clock time.</span></span>                             |
| <span data-ttu-id="2487b-117">Metodi IPersist</span><span class="sxs-lookup"><span data-stu-id="2487b-117">IPersist Methods</span></span>                                      | <span data-ttu-id="2487b-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2487b-118">Description</span></span>                                         |
| [<span data-ttu-id="2487b-119">**GetClassID**</span><span class="sxs-lookup"><span data-stu-id="2487b-119">**GetClassID**</span></span>](csystemclock-getclassid.md)         | <span data-ttu-id="2487b-120">Restituisce l'identificatore di classe (CLSID) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2487b-120">Returns the class identifier (CLSID) of the object.</span></span> |



 

 

 



