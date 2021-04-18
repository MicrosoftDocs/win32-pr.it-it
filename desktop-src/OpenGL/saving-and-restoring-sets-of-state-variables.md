---
title: Salvataggio e ripristino di set di variabili di stato
description: È possibile salvare e ripristinare i valori di una raccolta di variabili di stato in uno stack di attributi con le funzioni glPushAttrib e glPopAttrib.
ms.assetid: 339de633-4158-4907-b985-2d75b465fb2a
keywords:
- Variabili di stato OpenGL
- salvataggio delle variabili di stato OpenGL
- ripristino delle variabili di stato OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b3192c228ea35005c5755802d3cd1b873f7b7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298523"
---
# <a name="saving-and-restoring-sets-of-state-variables"></a><span data-ttu-id="22a93-106">Salvataggio e ripristino di set di variabili di stato</span><span class="sxs-lookup"><span data-stu-id="22a93-106">Saving and Restoring Sets of State Variables</span></span>

<span data-ttu-id="22a93-107">È possibile salvare e ripristinare i valori di una raccolta di variabili di stato in uno stack di attributi con le funzioni [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) .</span><span class="sxs-lookup"><span data-stu-id="22a93-107">You can save and restore the values of a collection of state variables on an attribute stack with the [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) functions.</span></span> <span data-ttu-id="22a93-108">Lo stack degli attributi ha una profondità di almeno 16.</span><span class="sxs-lookup"><span data-stu-id="22a93-108">The attribute stack has a depth of at least 16.</span></span> <span data-ttu-id="22a93-109">Per ottenere la profondità effettiva, usare la \_ \_ \_ profondità dello stack GL max attrib \_ con [**glGetIntegerv**](glgetintegerv.md).</span><span class="sxs-lookup"><span data-stu-id="22a93-109">To obtain the actual depth, use GL\_MAX\_ATTRIB\_STACK\_DEPTH with [**glGetIntegerv**](glgetintegerv.md).</span></span> <span data-ttu-id="22a93-110">Il push di uno stack completo o la visualizzazione di un oggetto vuoto genera un errore.</span><span class="sxs-lookup"><span data-stu-id="22a93-110">Pushing a full stack or popping an empty one generates an error.</span></span>

<span data-ttu-id="22a93-111">È in genere più veloce usare **glPushAttrib** e **glPopAttrib** anziché ottenere e ripristinare i valori manualmente.</span><span class="sxs-lookup"><span data-stu-id="22a93-111">It is generally faster to use **glPushAttrib** and **glPopAttrib** than to get and restore the values yourself.</span></span> <span data-ttu-id="22a93-112">Alcuni valori potrebbero essere inseriti e estratti nell'hardware e il salvataggio e il ripristino possono richiedere un utilizzo intensivo delle risorse.</span><span class="sxs-lookup"><span data-stu-id="22a93-112">Some values might be pushed and popped in the hardware, and saving and restoring them can be resource-intensive.</span></span> <span data-ttu-id="22a93-113">Inoltre, se si opera su un client remoto, tutti i dati degli attributi devono essere trasferiti attraverso la connessione di rete e viceversa mentre vengono salvati e ripristinati.</span><span class="sxs-lookup"><span data-stu-id="22a93-113">Also, if you're operating on a remote client, all of the attribute data must be transferred across the network connection and back as it is saved and restored.</span></span> <span data-ttu-id="22a93-114">Tuttavia, l'implementazione di OpenGL mantiene lo stack degli attributi sul server, evitando ritardi di rete non necessari.</span><span class="sxs-lookup"><span data-stu-id="22a93-114">However, your OpenGL implementation keeps the attribute stack on the server, avoiding unnecessary network delays.</span></span>

<span data-ttu-id="22a93-115">Il prototipo di **glPushAttrib** è:</span><span class="sxs-lookup"><span data-stu-id="22a93-115">The prototype of **glPushAttrib** is:</span></span>

<span data-ttu-id="22a93-116">**void** **glPushAttrib**(**GLbitfield** *mask* );</span><span class="sxs-lookup"><span data-stu-id="22a93-116">**void** **glPushAttrib**(**GLbitfield** *mask* );</span></span>

<span data-ttu-id="22a93-117">L'uso di [**glPushAttrib**](glpushattrib.md) Salva tutti gli attributi indicati dai bit nella *maschera* inserendoli nello stack degli attributi.</span><span class="sxs-lookup"><span data-stu-id="22a93-117">Using [**glPushAttrib**](glpushattrib.md) saves all the attributes indicated by bits in *mask* by pushing them onto the attribute stack.</span></span> <span data-ttu-id="22a93-118">Per un elenco dei bit di maschera possibili che è possibile combinare logicamente o insieme per salvare qualsiasi combinazione di attributi, vedere [gruppi](attribute-groups.md)di attributi.</span><span class="sxs-lookup"><span data-stu-id="22a93-118">For a list of the possible mask bits you can logically OR together to save any combination of attributes, see [Attribute Groups](attribute-groups.md).</span></span> <span data-ttu-id="22a93-119">Ogni bit corrisponde a una raccolta di singole variabili di stato.</span><span class="sxs-lookup"><span data-stu-id="22a93-119">Each bit corresponds to a collection of individual state variables.</span></span> <span data-ttu-id="22a93-120">Ad esempio, il \_ bit di illuminazione GL \_ si riferisce a tutte le variabili di stato correlate all'illuminazione, che includono il colore del materiale corrente, l'ambiente, la diffusione, il speculare e la luce emessa, un elenco delle luci abilitate e le direzioni dei faretti.</span><span class="sxs-lookup"><span data-stu-id="22a93-120">For example, GL\_LIGHTING\_BIT refers to all the state variables related to lighting, which include the current material color; the ambient, diffuse, specular, and emitted light; a list of the lights that are enabled; and the directions of the spotlights.</span></span> <span data-ttu-id="22a93-121">Quando si chiama [**glPopAttrib**](glpopattrib.md), vengono ripristinate tutte le variabili.</span><span class="sxs-lookup"><span data-stu-id="22a93-121">When you call [**glPopAttrib**](glpopattrib.md), all those variables are restored.</span></span> <span data-ttu-id="22a93-122">Per conoscere esattamente quali attributi vengono salvati per determinati valori di maschera, vedere [variabili di stato OpenGL](opengl-state-variables.md).</span><span class="sxs-lookup"><span data-stu-id="22a93-122">To find out exactly which attributes are saved for particular mask values, see [OpenGL State Variables](opengl-state-variables.md).</span></span>

 

 




