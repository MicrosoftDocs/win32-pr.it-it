---
description: Il rilevamento CallHub è una nuova funzionalità della versione 3,0 di TAPI.
ms.assetid: 29b6e585-6da8-46a2-a612-f42d0f65f68e
title: Supporto di CallHub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efe6891cfdad956a87745f8e4b35dd117fe775e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314633"
---
# <a name="callhub-support"></a><span data-ttu-id="2c527-103">Supporto di CallHub</span><span class="sxs-lookup"><span data-stu-id="2c527-103">CallHub Support</span></span>

<span data-ttu-id="2c527-104">Il rilevamento CallHub è una nuova funzionalità della versione 3,0 di TAPI.</span><span class="sxs-lookup"><span data-stu-id="2c527-104">CallHub tracking is a new feature in TAPI version 3.0.</span></span> <span data-ttu-id="2c527-105">La funzionalità CallHub è stata aggiunta agli elementi di programmazione TAPI 2,1 con la consegna di Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2c527-105">CallHub functionality was added to the TAPI 2.1 programming elements with the delivery of Windows 2000.</span></span> <span data-ttu-id="2c527-106">Un *CallHub* rappresenta una visualizzazione di una chiamata di terze parti e gli handle di chiamata di TAPI rappresentano la visualizzazione di una chiamata.</span><span class="sxs-lookup"><span data-stu-id="2c527-106">A *CallHub* represents a third-party view of a call, and TAPI's call handles represent the first-party view of a call.</span></span> <span data-ttu-id="2c527-107">Con il rilevamento CallHub, il provider di servizi deve seguire CallHubs e fornire informazioni sulla chiamata nel corso della durata di un CallHub.</span><span class="sxs-lookup"><span data-stu-id="2c527-107">With CallHub tracking, the service provider is requested to follow CallHubs and give information about the call during the lifetime of a CallHub.</span></span> <span data-ttu-id="2c527-108">Quando le nuove entità si uniscono e lasciano il CallHub, il provider di servizi deve informare TAPI.</span><span class="sxs-lookup"><span data-stu-id="2c527-108">As new parties join and leave the CallHub, the service provider should inform TAPI.</span></span>

<span data-ttu-id="2c527-109">Un provider di servizi non deve implementare nuove funzioni per supportare CallHub.</span><span class="sxs-lookup"><span data-stu-id="2c527-109">A service provider does not need to implement any new functions in order to support CallHub.</span></span> <span data-ttu-id="2c527-110">Deve semplicemente compilare il membro **dwCallID** della struttura [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="2c527-110">It simply needs to fill in the **dwCallID** member of the [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) structure.</span></span> <span data-ttu-id="2c527-111">In TAPI 3, TAPI raccoglie tutte le chiamate con lo stesso **dwCallID** e crea un handle CallHub che l'applicazione può usare per tenere traccia della chiamata.</span><span class="sxs-lookup"><span data-stu-id="2c527-111">In TAPI 3, TAPI collects all calls with the same **dwCallID** and creates a CallHub handle that the application can use to track the call.</span></span>

 

 
