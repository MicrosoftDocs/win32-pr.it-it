---
description: La classe CAMMsgEvent è un wrapper per oggetti evento che eseguono l'elaborazione dei messaggi.
ms.assetid: 4b94febe-169f-4f04-be93-043a8c75e3b4
title: Classe CAMMsgEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ebac7aae11f7a7b7d6b846e262e93b5759210b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329268"
---
# <a name="cammsgevent-class"></a><span data-ttu-id="4e0b9-103">Classe CAMMsgEvent</span><span class="sxs-lookup"><span data-stu-id="4e0b9-103">CAMMsgEvent class</span></span>

![gerarchia di classi cammsgevent](images/util06.png)

<span data-ttu-id="4e0b9-105">La `CAMMsgEvent` classe è un wrapper per gli oggetti evento che eseguono l'elaborazione dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="4e0b9-105">The `CAMMsgEvent` class is a wrapper for event objects that perform message processing.</span></span>

<span data-ttu-id="4e0b9-106">Questa classe deriva dall'oggetto [**CAMEvent**](camevent.md) .</span><span class="sxs-lookup"><span data-stu-id="4e0b9-106">This class derives from the [**CAMEvent**](camevent.md) object.</span></span> <span data-ttu-id="4e0b9-107">Viene aggiunto un metodo, [**CAMMsgEvent:: WaitMsg**](cammsgevent-waitmsg.md), che invia i messaggi in ingresso in attesa.</span><span class="sxs-lookup"><span data-stu-id="4e0b9-107">It adds one method, [**CAMMsgEvent::WaitMsg**](cammsgevent-waitmsg.md), which dispatches incoming messages while waiting.</span></span>



| <span data-ttu-id="4e0b9-108">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="4e0b9-108">Public Methods</span></span>                                 | <span data-ttu-id="4e0b9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e0b9-109">Description</span></span>                                                          |
|------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="4e0b9-110">**CAMMsgEvent**</span><span class="sxs-lookup"><span data-stu-id="4e0b9-110">**CAMMsgEvent**</span></span>](cammsgevent-cammsgevent.md) | <span data-ttu-id="4e0b9-111">Costruttore.</span><span class="sxs-lookup"><span data-stu-id="4e0b9-111">Constructor.</span></span>                                                         |
| [<span data-ttu-id="4e0b9-112">**WaitMsg**</span><span class="sxs-lookup"><span data-stu-id="4e0b9-112">**WaitMsg**</span></span>](cammsgevent-waitmsg.md)         | <span data-ttu-id="4e0b9-113">Attende la segnalazione dell'evento, durante l'invio dei messaggi inviati.</span><span class="sxs-lookup"><span data-stu-id="4e0b9-113">Waits for the event to be signaled, while dispatching sent messages.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="4e0b9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e0b9-114">Requirements</span></span>



| <span data-ttu-id="4e0b9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e0b9-115">Requirement</span></span> | <span data-ttu-id="4e0b9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4e0b9-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e0b9-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e0b9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4e0b9-118"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e0b9-118"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4e0b9-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="4e0b9-119">Library</span></span><br/> | <dl> <span data-ttu-id="4e0b9-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4e0b9-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




