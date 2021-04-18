---
description: I set di stazioni monitorati tramite un collegamento di terze parti vengono modellati come un dispositivo a linee e possibilmente un dispositivo telefonico associato.
ms.assetid: 1d116734-cd8f-40f1-9069-2dad351a24bf
title: Stazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff497eb70d1a1fd8441eeb8ad24bae6e5d1cd03e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318932"
---
# <a name="stations"></a><span data-ttu-id="17cd2-103">Stazioni</span><span class="sxs-lookup"><span data-stu-id="17cd2-103">Stations</span></span>

<span data-ttu-id="17cd2-104">I set di stazioni monitorati tramite un collegamento di terze parti vengono modellati come un dispositivo a linee e possibilmente un dispositivo telefonico associato.</span><span class="sxs-lookup"><span data-stu-id="17cd2-104">Station sets being monitored through a third-party link are modeled as a line device and possibly an associated phone device.</span></span> <span data-ttu-id="17cd2-105">Il dispositivo a linee può avere più indirizzi, se il terminale modellato supporta più di un numero di directory (DN).</span><span class="sxs-lookup"><span data-stu-id="17cd2-105">The line device can have multiple addresses, if the modeled terminal supports more than one directory number (DN).</span></span> <span data-ttu-id="17cd2-106">È possibile modellare più aspetti della chiamata nello stesso DN come un singolo indirizzo che supporta più chiamate.</span><span class="sxs-lookup"><span data-stu-id="17cd2-106">Multiple call appearances on the same DN can be modeled as a single address that supports multiple calls.</span></span>

<span data-ttu-id="17cd2-107">Le chiamate tra due stazioni sull'opzione hanno due handle di chiamata, uno che fornisce la visualizzazione chiamata dalla prima stazione (sul dispositivo linea) e l'altro che fornisce la visualizzazione chiamata dalla seconda stazione (sul dispositivo a linee).</span><span class="sxs-lookup"><span data-stu-id="17cd2-107">Calls between two stations on the switch have two call handles, one giving the call view from the first station (on its line device), and the other giving the call view from the second station (on its line device).</span></span> <span data-ttu-id="17cd2-108">Ad esempio, un [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) di terze parti inserito da un'applicazione sul server verrebbe indirizzato al dispositivo a linee associato alla stazione da cui deve essere stabilita la chiamata; viene creato un handle di chiamata su tale riga, sull'indirizzo specificato in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) , dando così il controllo su quale DN viene usato in un telefono che supporta più DNS.</span><span class="sxs-lookup"><span data-stu-id="17cd2-108">For example, a third-party [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) placed by an application on the server would be directed to the line device associated with the station from which the call is to be dialed; a call handle would be created on that line, on the address specified in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) (thereby giving control over which DN is used on a phone that supports multiple DNs).</span></span> <span data-ttu-id="17cd2-109">Quando la chiamata viene offerta all'indirizzo di destinazione, viene creato un nuovo handle di chiamata che mostra una chiamata nello stato *offering* ; le applicazioni saprebbero che era un'altra visualizzazione della stessa chiamata eseguita dal membro **dwCallID** in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) per entrambe le chiamate.</span><span class="sxs-lookup"><span data-stu-id="17cd2-109">When the call is offered to the destination address, a new call handle showing a call in *offering* state is created; applications would know that it was another view of the same call by the **dwCallID** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) being equal for both calls.</span></span> <span data-ttu-id="17cd2-110">Entrambe le chiamate diventano *inattive* quando la chiamata è stata eliminata; una chiamata può essere eliminata dall'applicazione di terze parti eseguendo un [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) su uno degli handle di chiamata.</span><span class="sxs-lookup"><span data-stu-id="17cd2-110">Both calls would go *idle* when the call was dropped; a call could be dropped from the third-party application by doing a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) on either of the call handles.</span></span>

 

 



