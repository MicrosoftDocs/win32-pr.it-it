---
description: Se si sceglie di eseguire questa operazione, l'applicazione può fornire le proprie implementazioni di riconoscimento. In questa sezione vengono descritti i requisiti per la creazione di un sistema di riconoscimento di applicazioni personalizzato per l'applicazione che è possibile utilizzare con l'API della piattaforma Tablet PC.
ms.assetid: 502ef3fb-ba45-4f8b-bbd5-19c24e313439
title: Creazione di un riconoscimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc71f56dc7095c6c72d18b36c3a12caa493ec9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305347"
---
# <a name="creating-a-recognizer"></a><span data-ttu-id="8de6a-104">Creazione di un riconoscimento</span><span class="sxs-lookup"><span data-stu-id="8de6a-104">Creating a Recognizer</span></span>

<span data-ttu-id="8de6a-105">Se si sceglie di eseguire questa operazione, l'applicazione può fornire le proprie implementazioni di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="8de6a-105">If you choose to do so, your application can provide its own recognizer implementations.</span></span> <span data-ttu-id="8de6a-106">In questa sezione vengono descritti i requisiti per la creazione di un sistema di riconoscimento di applicazioni personalizzato per l'applicazione che è possibile utilizzare con l'API della piattaforma Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="8de6a-106">This section describes the requirements for creating a custom application recognizer for your application that you can use with the Tablet PC Platform API.</span></span>

> [!Note]  
> <span data-ttu-id="8de6a-107">I sistemi di riconoscimento delle applicazioni personalizzati non vengono utilizzati dal pannello input penna di Tablet PC o da Microsoft Windows Journal.</span><span class="sxs-lookup"><span data-stu-id="8de6a-107">Custom application recognizers are not used by the Tablet PC Input Panel or Microsoft Windows Journal.</span></span> <span data-ttu-id="8de6a-108">Questi accessori utilizzano solo i riconoscitori per i quali sono stati testati.</span><span class="sxs-lookup"><span data-stu-id="8de6a-108">These accessories use only recognizers with which they have been tested.</span></span>

 

<span data-ttu-id="8de6a-109">Le sezioni seguenti illustrano in dettaglio l'implementazione di un sistema di riconoscimento personalizzato:</span><span class="sxs-lookup"><span data-stu-id="8de6a-109">The following sections detail the implementation of a custom recognizer:</span></span>

-   [<span data-ttu-id="8de6a-110">Architettura dell'API di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="8de6a-110">Recognition API Architecture</span></span>](recognition-api-architecture.md)
-   <span data-ttu-id="8de6a-111">[API di riconoscimento richieste](/previous-versions//ms701664(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8de6a-111">[Required Recognition APIs](/previous-versions//ms701664(v=vs.85))</span></span>
-   [<span data-ttu-id="8de6a-112">HRECOGNIZER e HRECOCONTEXT</span><span class="sxs-lookup"><span data-stu-id="8de6a-112">HRECOGNIZER and HRECOCONTEXT</span></span>](hrecognizer-and-hrecocontext.md)
-   [<span data-ttu-id="8de6a-113">Struttura del reticolo del riconoscitore</span><span class="sxs-lookup"><span data-stu-id="8de6a-113">Recognizer Lattice Structure</span></span>](recognizer-lattice-structure.md)
-   [<span data-ttu-id="8de6a-114">Registrazione della DLL del riconoscitore</span><span class="sxs-lookup"><span data-stu-id="8de6a-114">Registering Your Recognizer DLL</span></span>](registering-your-recognizer-dll.md)
-   [<span data-ttu-id="8de6a-115">Considerazioni sul threading del riconoscimento</span><span class="sxs-lookup"><span data-stu-id="8de6a-115">Recognizer Threading Considerations</span></span>](recognizer-threading-considerations.md)
-   [<span data-ttu-id="8de6a-116">Sequenza di chiamata tipica</span><span class="sxs-lookup"><span data-stu-id="8de6a-116">Typical Calling Sequence</span></span>](typical-calling-sequence.md)
-   [<span data-ttu-id="8de6a-117">Modello di esempio della DLL di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="8de6a-117">Recognizer DLL Sample Template</span></span>](recognizer-dll-sample-template.md)
-   [<span data-ttu-id="8de6a-118">Valori di intervallo Unicode dei movimenti</span><span class="sxs-lookup"><span data-stu-id="8de6a-118">Unicode Range Values of Gestures</span></span>](unicode-range-values-of-gestures.md)
-   [<span data-ttu-id="8de6a-119">API di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="8de6a-119">Recognizer APIs</span></span>](recognizer-apis.md)

 

 
