---
title: Metodi dell'oggetto character
description: Metodi dell'oggetto character
ms.assetid: 0f926b7b-c1cf-4bd6-ba8c-1b2877eb1d24
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19bb0dbb256c99660cbce1613c9fdd27d85a92dc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956362"
---
# <a name="character-object-methods"></a><span data-ttu-id="fe394-103">Metodi dell'oggetto character</span><span class="sxs-lookup"><span data-stu-id="fe394-103">Character Object Methods</span></span>

<span data-ttu-id="fe394-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fe394-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="fe394-105">Il server espone inoltre i metodi per ogni carattere in una raccolta di [**caratteri**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="fe394-105">The server also exposes methods for each character in a [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span> <span data-ttu-id="fe394-106">Sono supportati i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="fe394-106">The following methods are supported:</span></span>

-   [<span data-ttu-id="fe394-107">**Activate**</span><span class="sxs-lookup"><span data-stu-id="fe394-107">**Activate**</span></span>](activate-method.md)
-   [<span data-ttu-id="fe394-108">**GestureAt**</span><span class="sxs-lookup"><span data-stu-id="fe394-108">**GestureAt**</span></span>](gestureat-method.md)
-   [<span data-ttu-id="fe394-109">**Recupero**</span><span class="sxs-lookup"><span data-stu-id="fe394-109">**Get**</span></span>](get-method.md)
-   [<span data-ttu-id="fe394-110">**Nascondi**</span><span class="sxs-lookup"><span data-stu-id="fe394-110">**Hide**</span></span>](hide-method.md)
-   [<span data-ttu-id="fe394-111">**Interrompere**</span><span class="sxs-lookup"><span data-stu-id="fe394-111">**Interrupt**</span></span>](interrupt-method.md)
-   [<span data-ttu-id="fe394-112">**Attesa**</span><span class="sxs-lookup"><span data-stu-id="fe394-112">**Listen**</span></span>](listen-method.md)
-   [<span data-ttu-id="fe394-113">**MoveTo**</span><span class="sxs-lookup"><span data-stu-id="fe394-113">**MoveTo**</span></span>](moveto-method.md)
-   [<span data-ttu-id="fe394-114">**Esegui**</span><span class="sxs-lookup"><span data-stu-id="fe394-114">**Play**</span></span>](play-method.md)
-   [<span data-ttu-id="fe394-115">**Visualizza**</span><span class="sxs-lookup"><span data-stu-id="fe394-115">**Show**</span></span>](show-method.md)
-   [<span data-ttu-id="fe394-116">**ShowPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="fe394-116">**ShowPopupMenu**</span></span>](showpopupmenu-method.md)
-   [<span data-ttu-id="fe394-117">**Speak**</span><span class="sxs-lookup"><span data-stu-id="fe394-117">**Speak**</span></span>](speak-method.md)
-   [<span data-ttu-id="fe394-118">**Interrompere**</span><span class="sxs-lookup"><span data-stu-id="fe394-118">**Stop**</span></span>](stop-method.md)
-   [<span data-ttu-id="fe394-119">**StopAll**</span><span class="sxs-lookup"><span data-stu-id="fe394-119">**StopAll**</span></span>](stopall-method.md)
-   [<span data-ttu-id="fe394-120">**Pensare**</span><span class="sxs-lookup"><span data-stu-id="fe394-120">**Think**</span></span>](think-method.md)
-   [<span data-ttu-id="fe394-121">**Attesa**</span><span class="sxs-lookup"><span data-stu-id="fe394-121">**Wait**</span></span>](wait-method.md)

<span data-ttu-id="fe394-122">Per usare un metodo, fare riferimento al carattere nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="fe394-122">To use a method, reference the character in the collection.</span></span> <span data-ttu-id="fe394-123">In VBScript e Visual Basic è possibile eseguire questa operazione specificando l'ID per un carattere:</span><span class="sxs-lookup"><span data-stu-id="fe394-123">In VBScript and Visual Basic, you do this by specifying the ID for a character:</span></span>


```
   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Display the character
   Agent1.Characters("Genie").Show
   Agent1.Characters("Genie").Play "Greet"
   Agent1.Characters("Genie").Speak "Hello. "

   End Sub
```



<span data-ttu-id="fe394-124">Per semplificare la sintassi del codice, è possibile definire una variabile oggetto e impostarla in modo che faccia riferimento a un oggetto character nella raccolta [**Characters**](/windows/desktop/lwef/the-characters-object) . è quindi possibile usare la variabile per fare riferimento a metodi o proprietà del carattere.</span><span class="sxs-lookup"><span data-stu-id="fe394-124">To simplify the syntax of your code, you can define an object variable and set it to reference a character object in the [**Characters**](/windows/desktop/lwef/the-characters-object) collection; then you can use your variable to reference methods or properties of the character.</span></span> <span data-ttu-id="fe394-125">Nell'esempio seguente viene illustrato come è possibile eseguire questa operazione utilizzando l'istruzione set Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="fe394-125">The following example demonstrates how you can do this using the Visual Basic Set statement:</span></span>


```
   'Define a global object variable
   Dim Genie as Object

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", " Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   'Get the Restpose animation
   Genie.Get "animation", "RestPose"

   'Make the character say Hello
   Genie.Speak "Hello."

   End Sub
```



<span data-ttu-id="fe394-126">In Visual Basic 5,0, è anche possibile creare il riferimento dichiarando la variabile come oggetto [**character**](/windows/desktop/lwef/the-characters-object):</span><span class="sxs-lookup"><span data-stu-id="fe394-126">In Visual Basic 5.0, you can also create your reference by declaring your variable as a [**Character**](/windows/desktop/lwef/the-characters-object)object:</span></span>


```
   Dim Genie as IAgentCtlCharacterEx

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   End Sub
```



<span data-ttu-id="fe394-127">La dichiarazione di un oggetto di tipo IAgentCtlCharacterEx consente di associare in anticipo l'oggetto, con un conseguente miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="fe394-127">Declaring your object of type IAgentCtlCharacterEx enables early binding on the object, which results in better performance.</span></span>

<span data-ttu-id="fe394-128">In VBScript non è possibile dichiarare un riferimento come un tipo particolare.</span><span class="sxs-lookup"><span data-stu-id="fe394-128">In VBScript, you cannot declare a reference as a particular type.</span></span> <span data-ttu-id="fe394-129">È tuttavia possibile dichiarare semplicemente il riferimento alla variabile:</span><span class="sxs-lookup"><span data-stu-id="fe394-129">However, you can simply declare the variable reference:</span></span>


```
<SCRIPT LANGUAGE = "VBSCRIPT">
<!—--

   Dim Genie
   
   Sub window_OnLoad
   
   'Load the character
   AgentCtl.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   'Create an object reference to the character in the collection
   set Genie= AgentCtl.Characters ("Genie")

   'Get the Showing state animation
   Genie.Get "state", "Showing"

   'Display the character
   Genie.Show

   End Sub

-->
   </SCRIPT>
```



<span data-ttu-id="fe394-130">Alcuni linguaggi di programmazione non supportano le raccolte.</span><span class="sxs-lookup"><span data-stu-id="fe394-130">Some programming languages do not support collections.</span></span> <span data-ttu-id="fe394-131">È tuttavia possibile accedere ai metodi di un oggetto [**character**](/windows/desktop/lwef/the-characters-object) con il metodo [**character**](character-method.md) :</span><span class="sxs-lookup"><span data-stu-id="fe394-131">However, you can access a [**Character**](/windows/desktop/lwef/the-characters-object) object's methods with the [**Character**](character-method.md) method:</span></span>


```
   agent.Characters.Character("CharacterID").method
```



<span data-ttu-id="fe394-132">Inoltre, è possibile creare un riferimento all'oggetto [**carattere**](/windows/desktop/lwef/the-characters-object) per semplificare il codice di script:</span><span class="sxs-lookup"><span data-stu-id="fe394-132">In addition, you can also create a reference to the [**Character**](/windows/desktop/lwef/the-characters-object) object to make your script code easier to follow:</span></span>


```
<SCRIPT LANGUAGE="JScript" FOR="window" EVENT="onLoad()">
<!--
   
   //Load the character's data
   AgentCtl.Characters.Load ("Genie", _
      "https://agent.microsoft.com/characters/v2/genie/genie.acf");   

   //Create a reference to this object
   Genie = AgentCtl.Characters.Character("Genie");
   
   //Get the Showing state animation
   Genie.Get("state", "Showing");

   //Display the character
   Genie.Show();

-->
</SCRIPT>
```



 

 