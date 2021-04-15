---
title: Livello di debug Direct2D
description: Estensione di runtime per Direct2D che offre messaggi di errore descrittivi, rilevamento delle perdite di oggetti, notifiche sulle prestazioni e altri suggerimenti per la creazione di app Direct2D.
ms.assetid: 23b522d4-0733-4892-b93d-28f899fa0f17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f71b1364e645859059fb090634cbdae6f8c084e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395458"
---
# <a name="direct2d-debug-layer"></a><span data-ttu-id="7d7bc-103">Livello di debug Direct2D</span><span class="sxs-lookup"><span data-stu-id="7d7bc-103">Direct2D Debug Layer</span></span>

## <a name="purpose"></a><span data-ttu-id="7d7bc-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="7d7bc-104">Purpose</span></span>

<span data-ttu-id="7d7bc-105">Il livello di debug Direct2D, implementato separatamente da Direct2D nella propria DLL denominata d2d1debug.dll, fornisce messaggi di debug in fase di progettazione per ridurre al minimo l'errore dell'applicazione di Runtime.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-105">The Direct2D debug layer, implemented separately from Direct2D in its own DLL named d2d1debug.dll, provides design-time debug messages for you to minimize runtime application failure.</span></span> <span data-ttu-id="7d7bc-106">I messaggi di debug spesso derivano da violazioni dei contratti API, ad esempio parametri non validi (potrebbe essere correlato a Direct3D), risorse non valide, violazioni del threading e altri problemi di prestazioni, ad esempio l'utilizzo di un livello quando il clip sarebbe sufficiente.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-106">The debug messages often result from violations of API contracts such as invalid parameters (could be Direct3D-related), invalid resources, threading violations, and other performance issues such as using a layer when a clip would suffice.</span></span>

<span data-ttu-id="7d7bc-107">Per decidere la quantità di informazioni tracciate dal livello di debug, il livello di debug offre tre livelli di debug: informazioni, avviso ed errore.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-107">To help you decide how much information is traced by the debug layer, the debug layer offers three debug levels: information, warning, and error.</span></span> <span data-ttu-id="7d7bc-108">Questi tre livelli sono interpretati nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="7d7bc-108">These three levels are interpreted as follows:</span></span>

-   <span data-ttu-id="7d7bc-109">**Errore:** Direct2D invia messaggi di errore gravi al livello di debug.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-109">**Error:** Direct2D sends severe error messages to the debug layer.</span></span> <span data-ttu-id="7d7bc-110">Se ad esempio si interrompe un vincolo di threading, verrà generato un errore grave.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-110">For example, breaking a threading constraint will generate a severe error.</span></span>

    <span data-ttu-id="7d7bc-111">Inoltre, un messaggio di errore di livello attiva il punto di interruzione per facilitare il debug.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-111">Further, a message of level error triggers the breakpoint to help you debug.</span></span>

-   <span data-ttu-id="7d7bc-112">**Avviso:** Direct2D invia messaggi di errore e avvisi al livello di debug in modo che sia possibile risolvere uno di questi messaggi.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-112">**Warning:** Direct2D sends error messages and warnings to the debug layer so that you can address any of these messages.</span></span>

-   <span data-ttu-id="7d7bc-113">**Informazioni:** Direct2D invia messaggi di errore, avvisi e informazioni di diagnostica aggiuntive al livello di debug.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-113">**Information:** Direct2D sends error messages, warnings, and additional diagnostic information to the debug layer.</span></span> <span data-ttu-id="7d7bc-114">Ad esempio, i messaggi di miglioramento delle prestazioni verranno inviati a questo livello di debug.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-114">For example, performance improvement messages will be sent at this debug level.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7d7bc-115">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="7d7bc-115">In this section</span></span>



| <span data-ttu-id="7d7bc-116">Argomento</span><span class="sxs-lookup"><span data-stu-id="7d7bc-116">Topic</span></span>                                                                                     | <span data-ttu-id="7d7bc-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d7bc-117">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="7d7bc-118">Installazione del livello di debug Direct2D</span><span class="sxs-lookup"><span data-stu-id="7d7bc-118">Installing the Direct2D Debug Layer</span></span>](installing-the-direct2d-debug-layer.md)<br/> | <span data-ttu-id="7d7bc-119">Viene descritto come installare il livello di debug Direct2D.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-119">Describes how to install the Direct2D debug layer.</span></span><br/>      |
| [<span data-ttu-id="7d7bc-120">Panoramica del livello di debug Direct2D</span><span class="sxs-lookup"><span data-stu-id="7d7bc-120">Direct2D Debug Layer Overview</span></span>](direct2ddebuglayer-overview.md)<br/>               |                                                                    |
| [<span data-ttu-id="7d7bc-121">Messaggi di debug</span><span class="sxs-lookup"><span data-stu-id="7d7bc-121">Debug Messages</span></span>](direct2ddebuglayer-debugmessages.md)<br/>                         | <span data-ttu-id="7d7bc-122">Elenca i messaggi di debug dal livello di debug Direct2D.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-122">Lists the debug messages from the Direct2D Debug Layer.</span></span><br/> |



 

 

 





