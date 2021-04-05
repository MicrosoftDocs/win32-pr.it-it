---
description: La classe CMediaControl fornisce la gestione delle classi di base dei metodi IDispatch dei IMediaControl a doppia interfaccia. Lascia come virtuale pura le proprietà e i metodi dell'interfaccia IMediaControl.
ms.assetid: 033a2de6-8046-408c-995f-ec2de6654c41
title: Classe CMediaControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae3a528263af4bd2fe5e4eccbe28793799c373a0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103886025"
---
# <a name="cmediacontrol-class"></a><span data-ttu-id="01ed7-104">Classe CMediaControl</span><span class="sxs-lookup"><span data-stu-id="01ed7-104">CMediaControl class</span></span>

![gerarchia di classi cmediacontrol](images/cutil02.png)

<span data-ttu-id="01ed7-106">La `CMediaControl` classe fornisce la gestione delle classi di base dei metodi [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) dei [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)a doppia interfaccia.</span><span class="sxs-lookup"><span data-stu-id="01ed7-106">The `CMediaControl` class provides base class handling of the [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) methods of the dual-interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol).</span></span> <span data-ttu-id="01ed7-107">Lascia come virtuale pura le proprietà e i metodi dell'interfaccia **IMediaControl** .</span><span class="sxs-lookup"><span data-stu-id="01ed7-107">It leaves as pure virtual the properties and methods of the **IMediaControl** interface.</span></span>

<span data-ttu-id="01ed7-108">In genere, Filter Graph Manager è l'unico oggetto che implementa l'interfaccia [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) .</span><span class="sxs-lookup"><span data-stu-id="01ed7-108">Typically, the filter graph manager is the only object that implements the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface.</span></span> <span data-ttu-id="01ed7-109">i filtri implementano l'interfaccia [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) , ereditata da [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), per ricevere i comandi di controllo da gestione grafico dei filtri. Questa libreria di classi è pertanto di uso limitato per filtrare gli sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="01ed7-109">(filters implement the [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) interface, inherited by [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), to receive control commands from the filter graph manager.) Therefore, this class library is of limited use to filter developers.</span></span>

<span data-ttu-id="01ed7-110">Le funzioni membro [**CMediaControl:: GetIDsOfNames**](cmediacontrol-getidsofnames.md), [**CMediaControl:: GetTypeInfo**](cmediacontrol-gettypeinfo.md), [**CMediaControl:: GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md)e [**CMediaControl:: Invoke**](cmediacontrol-invoke.md) sono implementazioni standard dei metodi [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) che usano la classe [**CBaseDispatch**](cbasedispatch.md) (e una libreria dei tipi) per analizzare i comandi e passarli ai metodi virtuali puri dell'interfaccia [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) .</span><span class="sxs-lookup"><span data-stu-id="01ed7-110">The [**CMediaControl::GetIDsOfNames**](cmediacontrol-getidsofnames.md), [**CMediaControl::GetTypeInfo**](cmediacontrol-gettypeinfo.md), [**CMediaControl::GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md), and [**CMediaControl::Invoke**](cmediacontrol-invoke.md) member functions are standard implementations of the [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) methods using the [**CBaseDispatch**](cbasedispatch.md) class (and a type library) to parse the commands and pass them to the pure virtual methods of the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface.</span></span>

<span data-ttu-id="01ed7-111">I metodi [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) , definiti in Control. FAD, vengono lasciati come virtuali puri.</span><span class="sxs-lookup"><span data-stu-id="01ed7-111">The [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) methods, defined in control.odl, are left as pure virtual.</span></span>



| <span data-ttu-id="01ed7-112">Funzioni di membro</span><span class="sxs-lookup"><span data-stu-id="01ed7-112">Member Functions</span></span>                                           | <span data-ttu-id="01ed7-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01ed7-113">Description</span></span>                                                                                                                                                                                                                             |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01ed7-114">**CMediaControl**</span><span class="sxs-lookup"><span data-stu-id="01ed7-114">**CMediaControl**</span></span>](cmediacontrol-cmediacontrol.md)       | <span data-ttu-id="01ed7-115">Costruisce un oggetto **CMediaControl** .</span><span class="sxs-lookup"><span data-stu-id="01ed7-115">Constructs a **CMediaControl** object.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="01ed7-116">IDispatch (metodi)</span><span class="sxs-lookup"><span data-stu-id="01ed7-116">IDispatch Methods</span></span>                                          | <span data-ttu-id="01ed7-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01ed7-117">Description</span></span>                                                                                                                                                                                                                             |
| [<span data-ttu-id="01ed7-118">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="01ed7-118">**GetIDsOfNames**</span></span>](cmediacontrol-getidsofnames.md)       | <span data-ttu-id="01ed7-119">Esegue il mapping di un singolo membro e di un set facoltativo di parametri a un set corrispondente di identificatori di invio di numeri interi (DISPID), che possono essere usati durante le chiamate successive al metodo [**CMediaControl:: Invoke**](cmediacontrol-invoke.md) .</span><span class="sxs-lookup"><span data-stu-id="01ed7-119">Maps a single member and an optional set of parameters to a corresponding set of integer dispatch identifiers (DISPIDs), which can be used during subsequent calls to the [**CMediaControl::Invoke**](cmediacontrol-invoke.md) method.</span></span> |
| [<span data-ttu-id="01ed7-120">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="01ed7-120">**GetTypeInfo**</span></span>](cmediacontrol-gettypeinfo.md)           | <span data-ttu-id="01ed7-121">Recupera un oggetto informazioni sul tipo, che può recuperare le informazioni sul tipo per un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="01ed7-121">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>                                                                                                                                          |
| [<span data-ttu-id="01ed7-122">**GetTypeInfoCount**</span><span class="sxs-lookup"><span data-stu-id="01ed7-122">**GetTypeInfoCount**</span></span>](cmediacontrol-gettypeinfocount.md) | <span data-ttu-id="01ed7-123">Recupera il numero di interfacce di informazioni sul tipo fornite da un oggetto.</span><span class="sxs-lookup"><span data-stu-id="01ed7-123">Retrieves the number of type-information interfaces provided by an object.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="01ed7-124">**Richiamare**</span><span class="sxs-lookup"><span data-stu-id="01ed7-124">**Invoke**</span></span>](cmediacontrol-invoke.md)                     | <span data-ttu-id="01ed7-125">Fornisce l'accesso a proprietà e metodi esposti da un oggetto.</span><span class="sxs-lookup"><span data-stu-id="01ed7-125">Provides access to properties and methods exposed by an object.</span></span>                                                                                                                                                                         |



 

 

 
