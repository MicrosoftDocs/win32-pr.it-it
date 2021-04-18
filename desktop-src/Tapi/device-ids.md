---
description: Altre funzioni telefoniche TAPI usano un handle per un dispositivo telefonico aperto per identificare il dispositivo telefono aperto.
ms.assetid: 3e8e18fc-d577-4406-8225-048813c4cb9e
title: ID dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8eb9d43b22ab6cd39a90ab8ed0776c4e043ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307204"
---
# <a name="device-ids"></a><span data-ttu-id="6b4c6-103">ID dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="6b4c6-103">Device IDs</span></span>

<span data-ttu-id="6b4c6-104">Altre funzioni telefoniche TAPI usano un handle per un dispositivo telefonico aperto per identificare il dispositivo telefono aperto.</span><span class="sxs-lookup"><span data-stu-id="6b4c6-104">Other TAPI phone functions use a handle to an open phone device to identify the open phone device.</span></span> <span data-ttu-id="6b4c6-105">Le uniche funzioni per i dispositivi telefonici che accettano un parametro dell'identificatore del dispositivo telefonico (in contrapposizione a un handle telefonico) sono le funzioni [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) e [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) .</span><span class="sxs-lookup"><span data-stu-id="6b4c6-105">The only functions for phone devices that take a phone device identifier parameter (as opposed to a phone handle) are the [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) and [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) functions.</span></span> <span data-ttu-id="6b4c6-106">Un'applicazione può recuperare l'identificatore del dispositivo del telefono usando la funzione [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) con l'handle telefonico come parametro.</span><span class="sxs-lookup"><span data-stu-id="6b4c6-106">An application can retrieve the phone's device identifier by using the [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function with the phone handle as a parameter.</span></span>

<span data-ttu-id="6b4c6-107">Un'applicazione può anche ottenere gli identificatori di dispositivo per varie classi di dispositivi associate a un telefono aperto richiamando [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span><span class="sxs-lookup"><span data-stu-id="6b4c6-107">An application can also obtain device identifiers for various device classes associated with an opened phone by invoking [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span></span> <span data-ttu-id="6b4c6-108">Vedere [le classi di dispositivi TAPI](tapi-device-classes.md) per i nomi delle classi di dispositivi.</span><span class="sxs-lookup"><span data-stu-id="6b4c6-108">See [TAPI Device Classes](tapi-device-classes.md) for device class names.</span></span>

<span data-ttu-id="6b4c6-109">Questa funzione accetta un handle del telefono e una descrizione della classe del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b4c6-109">This function takes a phone handle and a device class description.</span></span> <span data-ttu-id="6b4c6-110">Restituisce l'identificatore del dispositivo per il dispositivo della classe del dispositivo specificata associata al dispositivo telefonico aperto.</span><span class="sxs-lookup"><span data-stu-id="6b4c6-110">It returns the device identifier for the device of the given device class that is associated with the open phone device.</span></span> <span data-ttu-id="6b4c6-111">Se la classe del dispositivo è "TAPI/Phone", viene restituito l'identificatore del dispositivo del telefono.</span><span class="sxs-lookup"><span data-stu-id="6b4c6-111">If the device class is "tapi/phone", the device identifier of the phone device is returned.</span></span>

<span data-ttu-id="6b4c6-112">A differenza dei dispositivi line, per i quali i servizi linea di base forniscono l'equivalente di POTS, non viene definito alcun set di funzioni minimo garantito per i dispositivi telefonici.</span><span class="sxs-lookup"><span data-stu-id="6b4c6-112">In contrast with line devices, for which the basic line services provide the equivalent of POTS, no minimum guaranteed set of functions is defined for phone devices.</span></span> <span data-ttu-id="6b4c6-113">Sebbene ogni dispositivo telefonico fornisca almeno le funzioni e i messaggi descritti in questa sezione, non offre alcuna operazione effettiva sul dispositivo telefonico fisico.</span><span class="sxs-lookup"><span data-stu-id="6b4c6-113">While each phone device provides at least the functions and messages described in this section, they do not offer any actual operations on the physical phone device.</span></span>

 

 



