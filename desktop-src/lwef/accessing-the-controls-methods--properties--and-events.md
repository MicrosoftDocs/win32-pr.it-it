---
title: Accesso ai metodi, alle proprietà e agli eventi dei controlli
description: Accesso ai metodi, alle proprietà e agli eventi dei controlli
ms.assetid: 70a3b011-0290-4df4-9b66-23b27bcb14e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750ad6280b521cf50c2ecd1fb7f1fcec3e2c4164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395846"
---
# <a name="accessing-the-controls-methods-properties-and-events"></a><span data-ttu-id="0e287-103">Accesso ai metodi, alle proprietà e agli eventi dei controlli</span><span class="sxs-lookup"><span data-stu-id="0e287-103">Accessing the Controls Methods, Properties, and Events</span></span>

<span data-ttu-id="0e287-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0e287-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="0e287-105">L'utilizzo del controllo di Microsoft Agent con Visual Basic è molto simile all'utilizzo del controllo con VBScript, ad eccezione del fatto che gli eventi in Visual Basic devono includere il tipo di dati dei parametri passati.</span><span class="sxs-lookup"><span data-stu-id="0e287-105">Using Microsoft Agent's control with Visual Basic is very similar to using the control with VBScript, except that events in Visual Basic must include the data type of passed parameters.</span></span> <span data-ttu-id="0e287-106">Se si aggiunge il controllo Microsoft Agent a un modulo, verranno automaticamente inclusi gli eventi di Microsoft Agent con i relativi parametri appropriati.</span><span class="sxs-lookup"><span data-stu-id="0e287-106">Adding the Microsoft Agent control to a form will automatically include Microsoft Agent's events with their appropriate parameters.</span></span> <span data-ttu-id="0e287-107">Verrà inoltre creata automaticamente una connessione al Server Agent durante l'esecuzione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0e287-107">It will also automatically create a connection to the Agent server when the application runs.</span></span>

<span data-ttu-id="0e287-108">È anche possibile usare la sintassi di creazione object's del linguaggio di programmazione per creare un'istanza del controllo in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0e287-108">You may also be able to use your programming language's object's creation syntax to create an instance of the control at runtime.</span></span> <span data-ttu-id="0e287-109">Ad esempio, in Visual Basic (5,0 o versioni successive), se si include il controllo Microsoft Agent 2,0 nei riferimenti del progetto, è possibile usare un [**con eventi**](https://www.bing.com/search?q=**With+Events**). [**Nuova**](https://www.bing.com/search?q=**New**) dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="0e287-109">For example, in Visual Basic (5.0 or later), if you include the Microsoft Agent 2.0 Control in your project's references, you can use a [**With Events**](https://www.bing.com/search?q=**With+Events**)..[**New**](https://www.bing.com/search?q=**New**) declaration.</span></span> <span data-ttu-id="0e287-110">Se non si include il riferimento, VB genera un errore che indica che non è stato possibile avviare Microsoft Agent (codice errore 80042502).</span><span class="sxs-lookup"><span data-stu-id="0e287-110">If you do not include the reference, VB raises an error indicating that Microsoft Agent was unable to start (error code 80042502).</span></span>

``` syntax
   ' Declare a global variable for the control
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```

<span data-ttu-id="0e287-111">Per le versioni di VB precedenti alla 5,0, è possibile usare la parola chiave VB [**New**](https://www.bing.com/search?q=**New**) senza Dichiarazione [**WithEvents**](https://www.bing.com/search?q=**WithEvents**) o la funzione [**CreateObject**](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx) di VB, ma queste convenzioni non esporrà gli eventi del controllo agente.</span><span class="sxs-lookup"><span data-stu-id="0e287-111">For versions of VB prior to 5.0, you can use the VB [**New**](https://www.bing.com/search?q=**New**) keyword without [**WithEvents**](https://www.bing.com/search?q=**WithEvents**) declaration or the VB [**CreateObject**](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx) function, but these conventions will not expose the Agent control's events.</span></span> <span data-ttu-id="0e287-112">È anche necessario usare la proprietà [**Connected**](https://www.bing.com/search?q=**Connected**) prima di fare riferimento a qualsiasi proprietà o metodo di Agent.</span><span class="sxs-lookup"><span data-stu-id="0e287-112">You also need to use the [**Connected**](https://www.bing.com/search?q=**Connected**) property before you reference any Agent methods or properties.</span></span> <span data-ttu-id="0e287-113">In caso contrario, VB genererà un errore che indica che non è stato possibile avviare Microsoft Agent (codice errore 80042502).</span><span class="sxs-lookup"><span data-stu-id="0e287-113">If this is not done, VB will raise an error indicating that Microsoft Agent was unable to start (error code 80042502).</span></span>

<span data-ttu-id="0e287-114">Analogamente per altri linguaggi di programmazione, potrebbe essere necessario utilizzare la proprietà [**Connected**](https://www.bing.com/search?q=**Connected**) per stabilire una connessione al server dell'agente Component Object Model (com) prima che il codice possa chiamare qualsiasi metodo o proprietà del controllo agente.</span><span class="sxs-lookup"><span data-stu-id="0e287-114">Similarly for other programming languages, you may have to use the [**Connected**](https://www.bing.com/search?q=**Connected**) property to establish a connection to the Agent Component Object Model (COM) server before your code can call any of the Agent control's methods or properties.</span></span> <span data-ttu-id="0e287-115">Per alcuni linguaggi di programmazione, inoltre, i metodi e le proprietà dell'agente potrebbero non essere esposti direttamente, a meno che non si dichiari il controllo Agent utilizzando il relativo tipo.</span><span class="sxs-lookup"><span data-stu-id="0e287-115">In addition, for some programming languages, Agent's methods and properties may not be directly exposed unless you declare the Agent control using its type.</span></span> <span data-ttu-id="0e287-116">Ad esempio, in Microsoft Access 97, è necessario dichiarare l'oggetto come tipo Agent per visualizzare i metodi e le proprietà visualizzati nella casella di riepilogo a discesa elenco automatico membri quando si digita.</span><span class="sxs-lookup"><span data-stu-id="0e287-116">For example, in Microsoft Access 97, you will need to declare the object as type Agent to see the methods and properties display in the Auto List Members drop-down box when you type.</span></span>

<span data-ttu-id="0e287-117">La maggior parte dei linguaggi di programmazione che supportano i controlli ActiveX seguono convenzioni simili a Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0e287-117">Most programming languages that support ActiveX controls follow conventions similar to Visual Basic.</span></span> <span data-ttu-id="0e287-118">Per i linguaggi di programmazione che non supportano le raccolte di oggetti, è possibile usare il metodo [**character**](https://www.bing.com/search?q=**Character**) e il metodo [**Command**](https://www.bing.com/search?q=**Command**) per accedere ai metodi e alle proprietà degli elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="0e287-118">For programming languages that do not support object collections, you can use the [**Character**](https://www.bing.com/search?q=**Character**) method and [**Command**](https://www.bing.com/search?q=**Command**) method to access methods and properties of items in the collection.</span></span>

<span data-ttu-id="0e287-119">I linguaggi di programmazione come Visual Basic, che forniscono accesso ai tipi di oggetti esposti dal controllo agente, consentono di usarli nelle dichiarazioni di oggetti.</span><span class="sxs-lookup"><span data-stu-id="0e287-119">Programming languages like Visual Basic, that provide access to the object types exposed by the Agent control, enable you to use these in your object declarations.</span></span> <span data-ttu-id="0e287-120">Ad esempio, anziché dichiarare un oggetto come tipo generico:</span><span class="sxs-lookup"><span data-stu-id="0e287-120">For example, instead of declaring an object as a generic type:</span></span>

``` syntax
   Dim Genie as Object
```

<span data-ttu-id="0e287-121">È possibile dichiarare un oggetto come tipo specifico:</span><span class="sxs-lookup"><span data-stu-id="0e287-121">You can declare an object as a specific type:</span></span>

``` syntax
   Dim Genie as IAgentCtlCharacterEx
```

<span data-ttu-id="0e287-122">Questo può migliorare le prestazioni complessive dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0e287-122">This may improve the overall performance of your application.</span></span>

<span data-ttu-id="0e287-123">Per alcuni tipi di oggetti, è possibile che siano presenti due tipi uguali, ad eccezione del suffisso "ex".</span><span class="sxs-lookup"><span data-stu-id="0e287-123">For some object types, you may find two types that are the same except for the "Ex" suffix.</span></span> <span data-ttu-id="0e287-124">In entrambi i casi, usare il tipo "ex" perché fornisce le funzionalità complete di Agent.</span><span class="sxs-lookup"><span data-stu-id="0e287-124">Where both exist, use the "Ex" type because this provides the full functionality of Agent.</span></span> <span data-ttu-id="0e287-125">Le controparti non "ex" sono incluse solo per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="0e287-125">The non-"Ex" counterparts are included only for backward compatibility.</span></span>

 

 




