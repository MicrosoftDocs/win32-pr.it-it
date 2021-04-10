---
description: Panoramica dell'uso dei movimenti.
ms.assetid: 5bc80086-7acf-4f86-a9fb-a663de489f8b
title: Uso di movimenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c267cff446d1bb6d092ba50bde21c1b3e25184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966651"
---
# <a name="using-gestures"></a><span data-ttu-id="73c38-103">Uso di movimenti</span><span class="sxs-lookup"><span data-stu-id="73c38-103">Using Gestures</span></span>

<span data-ttu-id="73c38-104">La piattaforma Tablet PC fornisce il riconoscitore di movimento Microsoft per supportare i movimenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="73c38-104">The Tablet PC platform provides the Microsoft gesture recognizer for supporting application gestures.</span></span> <span data-ttu-id="73c38-105">Per un elenco dei movimenti supportati dal riconoscitore di movimento Microsoft, vedere la tabella dei movimenti dell'applicazione nell'enumerazione [**ApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="73c38-105">For a list of gestures supported by the Microsoft gesture recognizer, see the table of application gestures in the [**ApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration.</span></span> <span data-ttu-id="73c38-106">Il Tablet PC supporta inoltre i movimenti di sistema.</span><span class="sxs-lookup"><span data-stu-id="73c38-106">The Tablet PC also supports system gestures.</span></span> <span data-ttu-id="73c38-107">Per un elenco dei movimenti del sistema supportati dal Tablet PC, vedere la tabella dei movimenti di sistema nell'enumerazione [**SystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) .</span><span class="sxs-lookup"><span data-stu-id="73c38-107">For a list of system gestures supported by the Tablet PC, see the table of system gestures in the [**SystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration.</span></span>

## <a name="microsoft-gesture-recognizer"></a><span data-ttu-id="73c38-108">Riconoscimento movimento Microsoft</span><span class="sxs-lookup"><span data-stu-id="73c38-108">Microsoft Gesture Recognizer</span></span>

<span data-ttu-id="73c38-109">È possibile utilizzare il riconoscitore di movimento Microsoft utilizzando la proprietà [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) dell'oggetto [**InkCollector**](inkcollector-class.md) , l'oggetto [**InkOverlay**](inkoverlay-class.md) o il controllo [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="73c38-109">You can employ the Microsoft gesture recognizer by using the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) property of the [**InkCollector**](inkcollector-class.md) object, the [**InkOverlay**](inkoverlay-class.md) object, or the [InkPicture](inkpicture-control-reference.md) control.</span></span> <span data-ttu-id="73c38-110">Se si imposta la proprietà **CollectionMode** su modalità mista (**InkAndGesture**) o la modalità solo movimento (**GestureOnly**), per impostazione predefinita viene passato l'input penna al riconoscimento di movimento Microsoft.</span><span class="sxs-lookup"><span data-stu-id="73c38-110">Setting the **CollectionMode** property to mixed mode (**InkAndGesture**) or gesture-only mode (**GestureOnly**) passes ink to the Microsoft gesture recognizer by default.</span></span> <span data-ttu-id="73c38-111">È possibile usare il riconoscitore di movimento Microsoft con il controllo [InkEdit](inkedit-control-reference.md) impostando la proprietà [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) su **InkAndGesture**.</span><span class="sxs-lookup"><span data-stu-id="73c38-111">You can employ the Microsoft gesture recognizer with the [InkEdit](inkedit-control-reference.md) control by setting the [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) property to **InkAndGesture**.</span></span> <span data-ttu-id="73c38-112">È anche possibile usare il riconoscimento dei movimenti con l'oggetto [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) aggiungendo un oggetto [**GestureRecognizer**](gesturerecognizer-class.md) a una delle relative raccolte di plug-in.</span><span class="sxs-lookup"><span data-stu-id="73c38-112">You can also use gesture recognition with the [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) object by adding a [**GestureRecognizer**](gesturerecognizer-class.md) object to one of its plug-in collections.</span></span>

<span data-ttu-id="73c38-113">Tuttavia, se i movimenti che si vuole usare non sono supportati dalla versione corrente del riconoscitore di movimento Microsoft, è possibile creare il proprio sistema di riconoscimento e usarlo in combinazione con il riconoscitore di movimento Microsoft.</span><span class="sxs-lookup"><span data-stu-id="73c38-113">However, if the gestures that you want to use are not supported by the current version of the Microsoft gesture recognizer, you can build your own recognizer and use it in conjunction with the Microsoft gesture recognizer.</span></span> <span data-ttu-id="73c38-114">Questo consente il supporto completo per i movimenti nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="73c38-114">This allows full support for the gestures in your application.</span></span>

<span data-ttu-id="73c38-115">Il Tablet PC usa una penna per alcuni o tutti gli input.</span><span class="sxs-lookup"><span data-stu-id="73c38-115">The Tablet PC uses a pen for some or all input.</span></span> <span data-ttu-id="73c38-116">Questo rende estremamente semplice scrivere input penna.</span><span class="sxs-lookup"><span data-stu-id="73c38-116">This makes it extremely easy to write ink.</span></span> <span data-ttu-id="73c38-117">La piattaforma Tablet PC fornisce l'architettura per input penna che supporta una struttura a più livelli dei movimenti.</span><span class="sxs-lookup"><span data-stu-id="73c38-117">The Tablet PC platform delivers architecture for pen input that supports a tiered structure of gestures.</span></span> <span data-ttu-id="73c38-118">I movimenti e il mapping vengono definiti per consentire all'utente di scrivere e richiamare movimenti avanzati su nuove superfici, riservando al tempo stesso i movimenti che richiamano i tradizionali messaggi del mouse di altre applicazioni basate su Windows.</span><span class="sxs-lookup"><span data-stu-id="73c38-118">Gestures and mapping are defined to allow the user to write and invoke advanced gestures on new surfaces, while reserving gestures that invoke traditional mouse messages of other Windows-based applications.</span></span>

<span data-ttu-id="73c38-119">La piattaforma Tablet PC introduce due livelli di movimenti: i movimenti di sistema, noti anche come eventi di sistema e i movimenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="73c38-119">The Tablet PC platform introduces two levels of gestures: system gestures, also known as system events, and application gestures.</span></span> <span data-ttu-id="73c38-120">L'architettura Pen supporta i movimenti del sistema e dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="73c38-120">The pen architecture supports both system and application gestures.</span></span> <span data-ttu-id="73c38-121">Sono supportati sia i movimenti di applicazione a tratto singolo che quelli a più tratti.</span><span class="sxs-lookup"><span data-stu-id="73c38-121">Both single-stroke and multiple-stroke application gestures are supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73c38-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="73c38-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73c38-123">Movimenti dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="73c38-123">Application Gestures</span></span>](application-gestures.md)
</dt> <dt>

[<span data-ttu-id="73c38-124">Movimenti rapidi</span><span class="sxs-lookup"><span data-stu-id="73c38-124">Flicks Gestures</span></span>](flicks-gestures.md)
</dt> <dt>

[<span data-ttu-id="73c38-125">Movimenti di sistema</span><span class="sxs-lookup"><span data-stu-id="73c38-125">System Gestures</span></span>](system-gestures.md)
</dt> </dl>

 

 



