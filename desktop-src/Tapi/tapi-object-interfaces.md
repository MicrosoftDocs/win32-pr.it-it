---
description: L'oggetto TAPI è l'oggetto principale per TAPI 3.
ms.assetid: 046f2646-6043-4d68-a42a-8750c016b3c8
title: Interfacce di oggetti TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906bda205f0d00a54cdb14cf408431cc45cad124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316021"
---
# <a name="tapi-object-interfaces"></a><span data-ttu-id="2bcb9-103">Interfacce di oggetti TAPI</span><span class="sxs-lookup"><span data-stu-id="2bcb9-103">TAPI Object Interfaces</span></span>

<span data-ttu-id="2bcb9-104">L' [oggetto TAPI](tapi-object.md) è l'oggetto principale per TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="2bcb9-104">The [TAPI Object](tapi-object.md) is the main object for TAPI 3.</span></span>

<span data-ttu-id="2bcb9-105">L'interfaccia [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) non è esposta direttamente nell'oggetto TAPI, ma è strettamente correlata e viene elencata qui per praticità di riferimento.</span><span class="sxs-lookup"><span data-stu-id="2bcb9-105">The [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) interface is not directly exposed on the TAPI Object, but is tightly related to it and is listed here for reference convenience.</span></span>



| <span data-ttu-id="2bcb9-106">Interfacce</span><span class="sxs-lookup"><span data-stu-id="2bcb9-106">Interfaces</span></span>                                                 | <span data-ttu-id="2bcb9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2bcb9-107">Description</span></span>                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2bcb9-108">**ITTAPI**</span><span class="sxs-lookup"><span data-stu-id="2bcb9-108">**ITTAPI**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi)                                   | <span data-ttu-id="2bcb9-109">Interfaccia TAPI 3 primaria.</span><span class="sxs-lookup"><span data-stu-id="2bcb9-109">Primary TAPI 3 interface.</span></span>                                                                                                                              |
| [<span data-ttu-id="2bcb9-110">**ITTAPI2**</span><span class="sxs-lookup"><span data-stu-id="2bcb9-110">**ITTAPI2**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2)                                 | <span data-ttu-id="2bcb9-111">Deriva da [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi); fornisce metodi aggiuntivi che supportano i dispositivi telefonici.</span><span class="sxs-lookup"><span data-stu-id="2bcb9-111">Derives from [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi); provides additional methods that support phone devices.</span></span>                                                         |
| [<span data-ttu-id="2bcb9-112">**ITTAPIEventNotification**</span><span class="sxs-lookup"><span data-stu-id="2bcb9-112">**ITTAPIEventNotification**</span></span>](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) | <span data-ttu-id="2bcb9-113">Interfaccia in uscita utilizzata per ricevere informazioni asincrone sugli eventi TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="2bcb9-113">Outgoing interface used to receive asynchronous information about TAPI 3 events.</span></span>                                                                       |
| [<span data-ttu-id="2bcb9-114">**ITTAPICallCenter**</span><span class="sxs-lookup"><span data-stu-id="2bcb9-114">**ITTAPICallCenter**</span></span>](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter)               | <span data-ttu-id="2bcb9-115">Fornisce un'interfaccia di ingresso nei controlli del Call Center.</span><span class="sxs-lookup"><span data-stu-id="2bcb9-115">Provides an entry interface into call center controls.</span></span>                                                                                                 |
| [<span data-ttu-id="2bcb9-116">**ITTAPIObjectEvent**</span><span class="sxs-lookup"><span data-stu-id="2bcb9-116">**ITTAPIObjectEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | <span data-ttu-id="2bcb9-117">Fornisce metodi per recuperare le informazioni relative agli eventi degli oggetti TAPI.</span><span class="sxs-lookup"><span data-stu-id="2bcb9-117">Provides methods to retrieve information concerning TAPI object events.</span></span>                                                                                |
| [<span data-ttu-id="2bcb9-118">**ITTAPIObjectEvent2**</span><span class="sxs-lookup"><span data-stu-id="2bcb9-118">**ITTAPIObjectEvent2**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | <span data-ttu-id="2bcb9-119">Estende [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent); fornisce un metodo per recuperare un puntatore all'oggetto Phone che ha causato l'evento dell'oggetto TAPI.</span><span class="sxs-lookup"><span data-stu-id="2bcb9-119">Extends [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent); provides a method to retrieve a pointer to the phone object that caused the TAPI object event.</span></span> |



 

 

 
