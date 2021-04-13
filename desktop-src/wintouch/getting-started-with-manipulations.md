---
title: Modifiche
description: In questa sezione viene illustrata la manipolazione degli oggetti per Windows Touch.
ms.assetid: 7f905c36-7804-422c-8a60-a281e03c5e15
keywords:
- Windows Touch, modifiche
- modifiche, informazioni
- manipolazioni, differenze di movimento
- movimenti, differenze di manipolazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10fe65494de990305e4268aa4191b5dabaa267f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328615"
---
# <a name="manipulations"></a><span data-ttu-id="7b6be-107">Modifiche</span><span class="sxs-lookup"><span data-stu-id="7b6be-107">Manipulations</span></span>

<span data-ttu-id="7b6be-108">In questa sezione viene illustrata la manipolazione degli oggetti per Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="7b6be-108">This section explains object manipulation for Windows Touch.</span></span>

## <a name="manipulation-overview"></a><span data-ttu-id="7b6be-109">Panoramica della manipolazione</span><span class="sxs-lookup"><span data-stu-id="7b6be-109">Manipulation Overview</span></span>

<span data-ttu-id="7b6be-110">Un modo pratico per considerare le manipolazioni consiste nel considerare un superset dei movimenti.</span><span class="sxs-lookup"><span data-stu-id="7b6be-110">A convenient way to think about manipulations is to consider them a superset of gestures.</span></span> <span data-ttu-id="7b6be-111">Che cosa è possibile fare con i movimenti, è possibile farlo con una maggiore flessibilità e con precisione maggiore usando le manipolazioni.</span><span class="sxs-lookup"><span data-stu-id="7b6be-111">What you can do with gestures, you can do with more flexibility and with finer precision by using manipulations.</span></span> <span data-ttu-id="7b6be-112">La differenza tra le modifiche e i movimenti è illustrata in modo ottimale con un semplice esempio.</span><span class="sxs-lookup"><span data-stu-id="7b6be-112">The difference between manipulations and gestures is best demonstrated with a simple example.</span></span> <span data-ttu-id="7b6be-113">È possibile espandere un oggetto e allo stesso tempo convertirlo utilizzando le modifiche. con i movimenti è possibile eseguire una sola operazione alla volta.</span><span class="sxs-lookup"><span data-stu-id="7b6be-113">You can expand an object and at the same time translate it using manipulations; with gestures, you can do only one at a time.</span></span> <span data-ttu-id="7b6be-114">La possibilità di modificare un oggetto in tempo reale rende le applicazioni più intuitive per gli utenti, consentendo un'esperienza più realistica.</span><span class="sxs-lookup"><span data-stu-id="7b6be-114">This ability to manipulate an object in real time makes applications more intuitive to users by enabling a more realistic experience.</span></span>

<span data-ttu-id="7b6be-115">Le API di manipolazione vengono usate per semplificare le operazioni di trasformazione sugli oggetti per le applicazioni abilitate per il tocco.</span><span class="sxs-lookup"><span data-stu-id="7b6be-115">The Manipulation APIs are used to simplify transformation operations on objects for touch-enabled applications.</span></span> <span data-ttu-id="7b6be-116">Le modifiche vengono eseguite in Windows 7 tramite l'oggetto COM di manipolazione.</span><span class="sxs-lookup"><span data-stu-id="7b6be-116">Manipulations are performed in Windows 7 through the manipulations COM object.</span></span> <span data-ttu-id="7b6be-117">Utilizzando le modifiche, gli sviluppatori possono supportare più facilmente l'inerzia (fisica degli oggetti) e possono eseguire facilmente trasformazioni sugli oggetti in modo coerente con altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="7b6be-117">By using manipulations, developers can more easily support inertia (object physics) and can easily perform transformations on objects in a way that is consistent with other applications.</span></span> <span data-ttu-id="7b6be-118">Nelle sezioni seguenti vengono illustrati i vari modi in cui è possibile eseguire le modifiche.</span><span class="sxs-lookup"><span data-stu-id="7b6be-118">The following sections explain various ways that you can perform manipulations.</span></span>



| <span data-ttu-id="7b6be-119">Sezione</span><span class="sxs-lookup"><span data-stu-id="7b6be-119">Section</span></span>                                                                                            | <span data-ttu-id="7b6be-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b6be-120">Description</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b6be-121">Aggiunta del supporto per la manipolazione a codice non gestito</span><span class="sxs-lookup"><span data-stu-id="7b6be-121">Adding Manipulation Support to Unmanaged Code</span></span>](adding-manipulation-support-in-unmanaged-code.md) | <span data-ttu-id="7b6be-122">Viene illustrato come implementare un sink di evento per l'interfaccia [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) e aggiungere gestori di eventi al codice.</span><span class="sxs-lookup"><span data-stu-id="7b6be-122">Explains how to implement an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface and add event handlers to your code.</span></span> |
| [<span data-ttu-id="7b6be-123">Manipolazioni avanzate</span><span class="sxs-lookup"><span data-stu-id="7b6be-123">Advanced Manipulations</span></span>](advanced-manipulations.md)                                               | <span data-ttu-id="7b6be-124">Viene illustrato come eseguire manipolazioni complesse.</span><span class="sxs-lookup"><span data-stu-id="7b6be-124">Explains how to perform complex manipulations.</span></span>                                                                                                       |
| [<span data-ttu-id="7b6be-125">Rotazione di un singolo dito</span><span class="sxs-lookup"><span data-stu-id="7b6be-125">Single Finger Rotation</span></span>](single-finger-rotation.md)                                               | <span data-ttu-id="7b6be-126">Viene illustrato come ruotare un oggetto utilizzando un punto pivot e il processore di manipolazione.</span><span class="sxs-lookup"><span data-stu-id="7b6be-126">Explains how to rotate an object by using a pivot point and the manipulation processor.</span></span>                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="7b6be-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7b6be-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b6be-128">Modifiche e inerzia</span><span class="sxs-lookup"><span data-stu-id="7b6be-128">Manipulations and Inertia</span></span>](manipulation-and-inertia.md)
</dt> </dl>

 

 




