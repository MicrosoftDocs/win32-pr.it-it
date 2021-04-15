---
description: Per impostazione predefinita, il riconoscimento utilizza un dizionario di sistema che contiene tutte le parole scritte comunemente in un linguaggio.
ms.assetid: 2ddf04dd-613b-4570-9474-0e33208c4012
title: Uso di dizionari applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74dfda443a688af9dfcec44a81f0e5ed2d50846c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484788"
---
# <a name="using-application-dictionaries"></a><span data-ttu-id="32b90-103">Uso di dizionari applicazioni</span><span class="sxs-lookup"><span data-stu-id="32b90-103">Using Application Dictionaries</span></span>

<span data-ttu-id="32b90-104">Per impostazione predefinita, il riconoscimento utilizza un dizionario di sistema che contiene tutte le parole scritte comunemente in un linguaggio.</span><span class="sxs-lookup"><span data-stu-id="32b90-104">By default, the recognizer uses a system dictionary that contains all of the commonly written words in a language.</span></span> <span data-ttu-id="32b90-105">Il riconoscimento dispone inoltre di un dizionario utente che contiene parole che l'utente ha aggiunto al dizionario.</span><span class="sxs-lookup"><span data-stu-id="32b90-105">In addition, the recognizer has a user dictionary that contains words that the user has added to the dictionary.</span></span> <span data-ttu-id="32b90-106">Gli utenti aggiungono una parola al dizionario utente tramite il pannello input penna di Tablet PC attraverso le selezioni in:</span><span class="sxs-lookup"><span data-stu-id="32b90-106">Users add a word to the user dictionary through Tablet PC Input Panel through selections in:</span></span>

-   <span data-ttu-id="32b90-107">Elenco alternativo (durante la scrittura).</span><span class="sxs-lookup"><span data-stu-id="32b90-107">The alternate list (when writing).</span></span>
-   <span data-ttu-id="32b90-108">Menu strumenti vocali (in lingua inglese).</span><span class="sxs-lookup"><span data-stu-id="32b90-108">The Speech Tools menu (when speaking).</span></span>

<span data-ttu-id="32b90-109">Se si sta progettando un'applicazione in cui si prevede che l'utente scriva parole che non sono presenti nel dizionario di sistema o nel dizionario utente, creare un dizionario dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="32b90-109">If you are designing an application into which you anticipate the user will write words that are not found in either the system dictionary or the user dictionary, create an application dictionary.</span></span> <span data-ttu-id="32b90-110">Un dizionario applicazioni migliora ulteriormente l'accuratezza del riconoscimento fornendo al sistema di riconoscimento un elenco personalizzato aggiuntivo di parole che è probabile immettere come grafia in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="32b90-110">An application dictionary further improves recognition accuracy by providing the recognizer with an additional customized list of words likely to be entered as handwriting into an application.</span></span>

<span data-ttu-id="32b90-111">Per creare un dizionario applicazioni, usare l'oggetto [**WordList**](inkwordlist-class.md) .</span><span class="sxs-lookup"><span data-stu-id="32b90-111">You create an application dictionary by using the [**WordList**](inkwordlist-class.md) object.</span></span> <span data-ttu-id="32b90-112">Il dizionario applicazioni risultante aumenta l'accuratezza del riconoscimento fornendo al riconoscimento un elenco di parole previste.</span><span class="sxs-lookup"><span data-stu-id="32b90-112">The ensuing application dictionary increases recognition accuracy by providing the recognizer with a list of expected words.</span></span> <span data-ttu-id="32b90-113">Ad esempio, un dizionario di applicazioni che contiene la terminologia medica aumenta l'accuratezza del riconoscimento all'interno di un'applicazione sviluppata per il settore medico in cui è probabile che i termini vengano scritti.</span><span class="sxs-lookup"><span data-stu-id="32b90-113">For example, an application dictionary that contains medical terminology increases recognition accuracy within an application developed for the medical industry into which the terms are likely to be written.</span></span>

<span data-ttu-id="32b90-114">Come altro esempio, quando si progetta un modulo per un utente per ordinare gli strumenti musicali, creare un oggetto [**WordList**](inkwordlist-class.md) contenente i nomi dei produttori di strumenti più comuni.</span><span class="sxs-lookup"><span data-stu-id="32b90-114">As another example, when designing a form for someone to order musical instruments, create a [**WordList**](inkwordlist-class.md) object that contains the names of the most common instrument manufacturers.</span></span> <span data-ttu-id="32b90-115">Impostare la proprietà [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) dell'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) sull'oggetto **WordList** creato.</span><span class="sxs-lookup"><span data-stu-id="32b90-115">Set the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object to the **WordList** object you created.</span></span> <span data-ttu-id="32b90-116">Questo elenco di parole viene quindi passato al riconoscimento dall'oggetto **RecognizerContext** .</span><span class="sxs-lookup"><span data-stu-id="32b90-116">This list of words is then passed to the recognizer by the **RecognizerContext** object.</span></span> <span data-ttu-id="32b90-117">Il dizionario applicazioni aumenta l'accuratezza del riconoscimento quando tali nomi vengono scritti in un campo nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="32b90-117">The application dictionary increases recognition accuracy when those names are written in a field in the application.</span></span>

<span data-ttu-id="32b90-118">Negli argomenti seguenti viene descritto come utilizzare i dizionari applicazione.</span><span class="sxs-lookup"><span data-stu-id="32b90-118">The following topics describe how to use application dictionaries.</span></span>

-   [<span data-ttu-id="32b90-119">Informazioni sugli elenchi di parole, contesto di riconoscimento e factoids</span><span class="sxs-lookup"><span data-stu-id="32b90-119">Understanding Word Lists, Recognizer Context, and Factoids</span></span>](understanding-wordlists--the-recognizercontext--and-factoids.md)
-   [<span data-ttu-id="32b90-120">Uso dei dizionari applicazioni con le API della piattaforma Tablet PC</span><span class="sxs-lookup"><span data-stu-id="32b90-120">Using Application Dictionaries with the Tablet PC Platform APIs</span></span>](using-application-dictionaries-with-the-tablet-pc-platform-apis.md)
-   [<span data-ttu-id="32b90-121">Creazione di dizionari personalizzati per il riconoscimento della grafia</span><span class="sxs-lookup"><span data-stu-id="32b90-121">Creating Custom Dictionaries for Handwriting Recognition</span></span>](creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2.md)

 

 



