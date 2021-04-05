---
description: L'oggetto CallHub espone metodi che recuperano informazioni relative ai partecipanti a una chiamata a più parti.
ms.assetid: 928c3abb-1b4e-42f3-a8cc-41889ad573ed
title: Interfacce oggetto CallHub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe448c7f559d38bef671144c1a6457f43d4a6b67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883234"
---
# <a name="callhub-object-interfaces"></a><span data-ttu-id="eb12e-103">Interfacce oggetto CallHub</span><span class="sxs-lookup"><span data-stu-id="eb12e-103">CallHub Object Interfaces</span></span>

<span data-ttu-id="eb12e-104">L' [oggetto CallHub](callhub-object.md) espone metodi che recuperano informazioni relative ai partecipanti a una chiamata a più parti.</span><span class="sxs-lookup"><span data-stu-id="eb12e-104">The [CallHub object](callhub-object.md) exposes methods that retrieve information concerning participants in a multi-party call.</span></span>

<span data-ttu-id="eb12e-105">Le interfacce [**ITCallHubEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhubevent) e [**IEnumCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallhub) non sono direttamente esposte sull'oggetto CallHub, ma sono strettamente correlate e sono elencate di seguito per praticità di riferimento.</span><span class="sxs-lookup"><span data-stu-id="eb12e-105">The [**ITCallHubEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhubevent) and [**IEnumCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallhub) interfaces are not directly exposed on the CallHub Object, but are tightly related to it and are listed here for reference convenience.</span></span>



| <span data-ttu-id="eb12e-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="eb12e-106">Interface</span></span>                                | <span data-ttu-id="eb12e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb12e-107">Description</span></span>                                                           |
|------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="eb12e-108">**ITCallHub**</span><span class="sxs-lookup"><span data-stu-id="eb12e-108">**ITCallHub**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub)           | <span data-ttu-id="eb12e-109">Fornisce metodi per recuperare le informazioni relative a un oggetto CallHub.</span><span class="sxs-lookup"><span data-stu-id="eb12e-109">Provides methods to retrieve information concerning a CallHub object.</span></span> |
| [<span data-ttu-id="eb12e-110">**ITCallHubEvent**</span><span class="sxs-lookup"><span data-stu-id="eb12e-110">**ITCallHubEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhubevent) | <span data-ttu-id="eb12e-111">Utilizzato per acquisire informazioni relative agli eventi CallHub.</span><span class="sxs-lookup"><span data-stu-id="eb12e-111">Used to acquire information concerning CallHub events.</span></span>                |
| [<span data-ttu-id="eb12e-112">**IEnumCallHub**</span><span class="sxs-lookup"><span data-stu-id="eb12e-112">**IEnumCallHub**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallhub)     | <span data-ttu-id="eb12e-113">Enumera [**ITCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub).</span><span class="sxs-lookup"><span data-stu-id="eb12e-113">Enumerates [**ITCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub).</span></span>                            |



 

 

 



