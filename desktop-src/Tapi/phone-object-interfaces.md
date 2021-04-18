---
description: L'oggetto telefono è l'entità che rappresenta il dispositivo telefonico effettivo e tutti i relativi controlli.
ms.assetid: 5bc2f595-8e2b-4938-b813-1574a9390084
title: Interfacce per oggetti telefono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f39b163e895a512e7adc7be5c2fb848c5849361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315275"
---
# <a name="phone-object-interfaces"></a><span data-ttu-id="db6ef-103">Interfacce per oggetti telefono</span><span class="sxs-lookup"><span data-stu-id="db6ef-103">Phone Object Interfaces</span></span>

<span data-ttu-id="db6ef-104">L'oggetto telefono è l'entità che rappresenta il dispositivo telefonico effettivo e tutti i relativi controlli.</span><span class="sxs-lookup"><span data-stu-id="db6ef-104">The Phone object is the entity that represents the actual phone device and all of its controls.</span></span>

<span data-ttu-id="db6ef-105">Le interfacce [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) e [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) non sono direttamente esposte sull'oggetto Phone, ma sono strettamente correlate e sono elencate di seguito per praticità di riferimento.</span><span class="sxs-lookup"><span data-stu-id="db6ef-105">The [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) and [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) interfaces are not directly exposed on the Phone object, but are tightly related to it and are listed here for convenience of reference.</span></span>



| <span data-ttu-id="db6ef-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="db6ef-106">Interface</span></span>                                                  | <span data-ttu-id="db6ef-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db6ef-107">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="db6ef-108">**ITPhone**</span><span class="sxs-lookup"><span data-stu-id="db6ef-108">**ITPhone**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                 | <span data-ttu-id="db6ef-109">Consente l'accesso al dispositivo telefonico a un livello paragonabile a quello disponibile con TAPI 2. API *x* C.</span><span class="sxs-lookup"><span data-stu-id="db6ef-109">Allows access to the phone device at a level comparable to that available with the TAPI 2.*x* C API.</span></span>                                      |
| [<span data-ttu-id="db6ef-110">**ITAutomatedPhoneControl**</span><span class="sxs-lookup"><span data-stu-id="db6ef-110">**ITAutomatedPhoneControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) | <span data-ttu-id="db6ef-111">Fornisce metodi per il controllo automatizzato dei toni e degli anelli di un telefono e per la gestione automatica delle chiamate in base allo stato hookswitch del telefono.</span><span class="sxs-lookup"><span data-stu-id="db6ef-111">Provides methods for automated control of a phone's tones and rings, and for automated call handling based on a phone's hookswitch state.</span></span> |
| [<span data-ttu-id="db6ef-112">**ITPhoneEvent**</span><span class="sxs-lookup"><span data-stu-id="db6ef-112">**ITPhoneEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)                       | <span data-ttu-id="db6ef-113">Recupera la descrizione degli eventi del telefono.</span><span class="sxs-lookup"><span data-stu-id="db6ef-113">Retrieves the description of phone events.</span></span>                                                                                                |
| [<span data-ttu-id="db6ef-114">**IEnumPhone**</span><span class="sxs-lookup"><span data-stu-id="db6ef-114">**IEnumPhone**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)                           | <span data-ttu-id="db6ef-115">Enumera [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone).</span><span class="sxs-lookup"><span data-stu-id="db6ef-115">Enumerates [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone).</span></span>                                                                                                    |



 

 

 



