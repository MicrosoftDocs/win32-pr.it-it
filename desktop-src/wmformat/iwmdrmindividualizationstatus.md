---
title: Interfaccia IWMDRMIndividualizationStatus
description: L'interfaccia IWMDRMIndividualizationStatus consente il recupero delle informazioni di stato avanzate sullo stato di avanzamento della singola. Questa interfaccia viene fornita con gli eventi MEWMDRMIndividualizationProgress.
ms.assetid: 3a148005-22fa-4495-a47c-d9463db16293
keywords:
- Formato Windows Media Interface IWMDRMIndividualizationStatus
- Interfaccia IWMDRMIndividualizationStatus-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19a369bf9b70d9a43af8a48f13f1b8bbb87525b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963333"
---
# <a name="iwmdrmindividualizationstatus-interface"></a><span data-ttu-id="88e76-105">Interfaccia IWMDRMIndividualizationStatus</span><span class="sxs-lookup"><span data-stu-id="88e76-105">IWMDRMIndividualizationStatus interface</span></span>

<span data-ttu-id="88e76-106">L'interfaccia **IWMDRMIndividualizationStatus** consente il recupero delle informazioni di stato avanzate sullo stato di avanzamento della singola.</span><span class="sxs-lookup"><span data-stu-id="88e76-106">The **IWMDRMIndividualizationStatus** interface enables retrieval of advanced status information about the progress of individualization.</span></span>

<span data-ttu-id="88e76-107">Questa interfaccia viene fornita con gli eventi MEWMDRMIndividualizationProgress.</span><span class="sxs-lookup"><span data-stu-id="88e76-107">This interface is delivered with MEWMDRMIndividualizationProgress events.</span></span> <span data-ttu-id="88e76-108">Molti di questi eventi vengono generati tra una chiamata a [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) e il completamento del processo di individualizzazione, segnalato dalla generazione di un evento **MEWMDRMIndividualizationCompleted** .</span><span class="sxs-lookup"><span data-stu-id="88e76-108">Many such events are generated between a call to [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) and the completion of the individualization process, which is signaled by the generation of an **MEWMDRMIndividualizationCompleted** event.</span></span>

<span data-ttu-id="88e76-109">Per recuperare un puntatore a un'istanza dell'interfaccia **IWMDRMIndividualizationStatus** , è prima necessario chiamare il metodo **IMFMediaEvent:: GetValue** dell'evento Progress.</span><span class="sxs-lookup"><span data-stu-id="88e76-109">To retrieve a pointer to an instance of the **IWMDRMIndividualizationStatus** interface, you must first call the **IMFMediaEvent::GetValue** method of the progress event.</span></span> <span data-ttu-id="88e76-110">Il valore recuperato dall'evento è un puntatore all'interfaccia **IUnknown** dell'oggetto che implementa l'interfaccia **IWMDRMIndividualizationStatus** .</span><span class="sxs-lookup"><span data-stu-id="88e76-110">The value you retrieve from the event is a pointer to the **IUnknown** interface of the object that implements the **IWMDRMIndividualizationStatus** interface.</span></span>

## <a name="members"></a><span data-ttu-id="88e76-111">Membri</span><span class="sxs-lookup"><span data-stu-id="88e76-111">Members</span></span>

<span data-ttu-id="88e76-112">L'interfaccia **IWMDRMIndividualizationStatus** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="88e76-112">The **IWMDRMIndividualizationStatus** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="88e76-113">**IWMDRMIndividualizationStatus** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="88e76-113">**IWMDRMIndividualizationStatus** also has these types of members:</span></span>

-   [<span data-ttu-id="88e76-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="88e76-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="88e76-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="88e76-115">Methods</span></span>

<span data-ttu-id="88e76-116">L'interfaccia **IWMDRMIndividualizationStatus** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="88e76-116">The **IWMDRMIndividualizationStatus** interface has these methods.</span></span>



| <span data-ttu-id="88e76-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="88e76-117">Method</span></span>                                                       | <span data-ttu-id="88e76-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88e76-118">Description</span></span>                                                        |
|:-------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="88e76-119">**GetStatus**</span><span class="sxs-lookup"><span data-stu-id="88e76-119">**GetStatus**</span></span>](iwmdrmindividualizationstatus-getstatus.md) | <span data-ttu-id="88e76-120">Recupera informazioni dettagliate sulla individualizzazione.</span><span class="sxs-lookup"><span data-stu-id="88e76-120">Retrieves detailed information about individualization.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="88e76-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88e76-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88e76-122">**Interfacce**</span><span class="sxs-lookup"><span data-stu-id="88e76-122">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

