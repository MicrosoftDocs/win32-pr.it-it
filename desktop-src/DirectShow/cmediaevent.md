---
description: La classe CMediaEvent fornisce l'implementazione della classe di base dei metodi IDispatch dei IMediaEvent a doppia interfaccia. Lascia come virtuale pura le proprietà e i metodi dell'interfaccia IMediaEvent.
ms.assetid: 849e08ac-8d1b-4c86-94eb-ab5c4f10d68a
title: Classe CMediaEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 927e561fa557ac33b1669ca7353377f7814ca448
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104234528"
---
# <a name="cmediaevent-class"></a><span data-ttu-id="6811f-104">Classe CMediaEvent</span><span class="sxs-lookup"><span data-stu-id="6811f-104">CMediaEvent class</span></span>

![gerarchia di classi cmediaevent](images/cutil03.png)

<span data-ttu-id="6811f-106">La `CMediaEvent` classe fornisce l'implementazione della classe di base dei metodi **IDispatch** dei [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)a doppia interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6811f-106">The `CMediaEvent` class provides base class implementation of the **IDispatch** methods of the dual-interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).</span></span> <span data-ttu-id="6811f-107">Lascia come virtuale pura le proprietà e i metodi dell'interfaccia **IMediaEvent** .</span><span class="sxs-lookup"><span data-stu-id="6811f-107">It leaves as pure virtual the properties and methods of the **IMediaEvent** interface.</span></span>

<span data-ttu-id="6811f-108">La `CMediaEvent` classe fornisce anche l'implementazione della classe di base dell'interfaccia [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) che deriva da [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).</span><span class="sxs-lookup"><span data-stu-id="6811f-108">The `CMediaEvent` class also provides base class implementation of the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface which derives from [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).</span></span>

<span data-ttu-id="6811f-109">Le funzioni membro [**CMediaEvent:: GetIDsOfNames**](cmediaevent-getidsofnames.md), [**CMediaEvent:: GetTypeInfo**](cmediaevent-gettypeinfo.md), [**CMediaEvent:: GetTypeInfoCount**](cmediaevent-gettypeinfocount.md)e [**CMediaEvent:: Invoke**](cmediaevent-invoke.md) sono implementazioni standard dell'interfaccia **IDispatch** usando la classe [**CBaseDispatch**](cbasedispatch.md) (e una libreria dei tipi) per analizzare i comandi e passarli ai metodi virtuali puri dell'interfaccia [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .</span><span class="sxs-lookup"><span data-stu-id="6811f-109">The [**CMediaEvent::GetIDsOfNames**](cmediaevent-getidsofnames.md), [**CMediaEvent::GetTypeInfo**](cmediaevent-gettypeinfo.md), [**CMediaEvent::GetTypeInfoCount**](cmediaevent-gettypeinfocount.md), and [**CMediaEvent::Invoke**](cmediaevent-invoke.md) member functions are standard implementations of the **IDispatch** interface using the [**CBaseDispatch**](cbasedispatch.md) class (and a type library) to parse the commands and pass them to the pure virtual methods of the [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interface.</span></span>



| <span data-ttu-id="6811f-110">Funzioni di membro</span><span class="sxs-lookup"><span data-stu-id="6811f-110">Member Functions</span></span>                                         | <span data-ttu-id="6811f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6811f-111">Description</span></span>                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6811f-112">**CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="6811f-112">**CMediaEvent**</span></span>](cmediaevent-cmediaevent.md)           | <span data-ttu-id="6811f-113">Costruisce un oggetto **CMediaEvent** .</span><span class="sxs-lookup"><span data-stu-id="6811f-113">Constructs a **CMediaEvent** object.</span></span>                                                                                                                                                          |
| <span data-ttu-id="6811f-114">IDispatch (metodi)</span><span class="sxs-lookup"><span data-stu-id="6811f-114">IDispatch Methods</span></span>                                        | <span data-ttu-id="6811f-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6811f-115">Description</span></span>                                                                                                                                                                                   |
| [<span data-ttu-id="6811f-116">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="6811f-116">**GetIDsOfNames**</span></span>](cmediaevent-getidsofnames.md)       | <span data-ttu-id="6811f-117">Esegue il mapping di un singolo membro e di un set facoltativo di parametri a un set corrispondente di identificatori di invio di numeri interi, che possono essere usati durante le chiamate successive al metodo **IDispatch:: Invoke** .</span><span class="sxs-lookup"><span data-stu-id="6811f-117">Maps a single member and an optional set of parameters to a corresponding set of integer dispatch identifiers, which can be used during subsequent calls to the **IDispatch::Invoke** method.</span></span> |
| [<span data-ttu-id="6811f-118">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="6811f-118">**GetTypeInfo**</span></span>](cmediaevent-gettypeinfo.md)           | <span data-ttu-id="6811f-119">Recupera un oggetto informazioni sul tipo, che recupera le informazioni sul tipo per un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6811f-119">Retrieves a type-information object, which retrieves the type information for an interface.</span></span>                                                                                                   |
| [<span data-ttu-id="6811f-120">**GetTypeInfoCount**</span><span class="sxs-lookup"><span data-stu-id="6811f-120">**GetTypeInfoCount**</span></span>](cmediaevent-gettypeinfocount.md) | <span data-ttu-id="6811f-121">Recupera il numero di interfacce di informazioni sul tipo fornite da un oggetto.</span><span class="sxs-lookup"><span data-stu-id="6811f-121">Retrieves the number of type-information interfaces provided by an object.</span></span>                                                                                                                    |
| [<span data-ttu-id="6811f-122">**Richiamare**</span><span class="sxs-lookup"><span data-stu-id="6811f-122">**Invoke**</span></span>](cmediaevent-invoke.md)                     | <span data-ttu-id="6811f-123">Fornisce l'accesso a proprietà e metodi esposti da un oggetto.</span><span class="sxs-lookup"><span data-stu-id="6811f-123">Provides access to properties and methods exposed by an object.</span></span>                                                                                                                               |



 

 

 



