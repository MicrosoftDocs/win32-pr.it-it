---
description: Oltre a riconoscere il testo, i riconoscitori possono riconoscere una classe di oggetti correlati.
ms.assetid: 53b6137d-2998-4a3b-b469-3d1204ea194b
title: Riconoscitori di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a258c8486bcf773f5f94c4de51c501e107fac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968039"
---
# <a name="object-recognizers"></a><span data-ttu-id="df19c-103">Riconoscitori di oggetti</span><span class="sxs-lookup"><span data-stu-id="df19c-103">Object Recognizers</span></span>

<span data-ttu-id="df19c-104">Oltre a riconoscere il testo, i riconoscitori possono riconoscere una classe di oggetti correlati.</span><span class="sxs-lookup"><span data-stu-id="df19c-104">In addition to recognizing text, recognizers can recognize a class of related objects.</span></span> <span data-ttu-id="df19c-105">I riconoscitori di oggetti riconoscono le forme generali, in base allo scopo.</span><span class="sxs-lookup"><span data-stu-id="df19c-105">Object recognizers recognize general shapes, according to their purpose.</span></span> <span data-ttu-id="df19c-106">I riconoscitori di oggetti vengono usati per riconoscere:</span><span class="sxs-lookup"><span data-stu-id="df19c-106">Object recognizers are used to recognize:</span></span>

-   <span data-ttu-id="df19c-107">Note musicali</span><span class="sxs-lookup"><span data-stu-id="df19c-107">Musical notes</span></span>
-   <span data-ttu-id="df19c-108">Forme geometriche</span><span class="sxs-lookup"><span data-stu-id="df19c-108">Geometric shapes</span></span>
-   <span data-ttu-id="df19c-109">Equazioni matematiche</span><span class="sxs-lookup"><span data-stu-id="df19c-109">Math equations</span></span>
-   <span data-ttu-id="df19c-110">Elementi del diagramma di flusso</span><span class="sxs-lookup"><span data-stu-id="df19c-110">Flow chart elements</span></span>

<span data-ttu-id="df19c-111">In genere, gli oggetti riconosciuti da un riconoscimento di questo tipo si trovano in una relazione spaziale o funzionale bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="df19c-111">Usually, the objects that are recognized by such a recognizer are in a two-dimensional spatial or functional relationship with each other.</span></span> <span data-ttu-id="df19c-112">Ad esempio, all'interno delle relazioni complesse in un'equazione matematica, un riconoscitore può restituire risultati diversi per un limite superiore su un integrale definito anziché un numeratore in una frazione.</span><span class="sxs-lookup"><span data-stu-id="df19c-112">For example, within the complex relationships in a math equation, a recognizer can return different results for an upper limit on a definite integral as opposed to a numerator in a fraction.</span></span>

<span data-ttu-id="df19c-113">A causa della natura generale di queste relazioni, è estremamente difficile definire il set di interfacce che funzioneranno per ogni riconoscimento di oggetti.</span><span class="sxs-lookup"><span data-stu-id="df19c-113">Because of the very general nature of these relationships, it is extremely difficult to define the set of interfaces that will work for every object recognizer.</span></span>

<span data-ttu-id="df19c-114">La tecnologia Tablet PC fornisce un Framework di base per i riconoscitori di oggetti nelle interfacce di automazione e libreria gestita.</span><span class="sxs-lookup"><span data-stu-id="df19c-114">The Tablet PC Technology provides a basic framework for object recognizers in the Managed Library and Automation interfaces.</span></span> <span data-ttu-id="df19c-115">È tuttavia necessario sviluppare interfacce personalizzate che descrivono relazioni spaziali complesse tra oggetti riconosciuti per ogni riconoscimento di oggetti.</span><span class="sxs-lookup"><span data-stu-id="df19c-115">However, you must develop custom interfaces that describe complex spatial relationships between recognized objects for each object recognizer.</span></span> <span data-ttu-id="df19c-116">In particolare, per i riconoscitori di oggetti, la piattaforma fornisce l'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) di base per associare l'oggetto [**Ink**](inkdisp-class.md) al contesto di riconoscimento e per chiamare il riconoscimento per eseguire il riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="df19c-116">Specifically, for object recognizers, the platform provides the basic [**RecognizerContext**](inkrecognizercontext-class.md) object for associating the [**Ink**](inkdisp-class.md) object with the recognizer context and for calling the recognizer to perform the recognition.</span></span>

 

 



