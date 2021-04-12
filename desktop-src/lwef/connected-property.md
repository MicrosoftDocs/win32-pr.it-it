---
title: Proprietà connessa
description: Proprietà connessa
ms.assetid: 61b7f550-d8d6-4719-a0d4-0bf3a8cf096c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bba78358c7c42f0754da017aa0c188d41acd189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331087"
---
# <a name="connected-property"></a><span data-ttu-id="47f26-103">Proprietà connessa</span><span class="sxs-lookup"><span data-stu-id="47f26-103">Connected Property</span></span>

<span data-ttu-id="47f26-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="47f26-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="47f26-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="47f26-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="47f26-106">Restituisce o imposta un valore che indica se il controllo corrente è connesso al server Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="47f26-106">Returns or sets whether the current control is connected to the Microsoft Agent server.</span></span>

</dd> <dt>

<span data-ttu-id="47f26-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="47f26-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="47f26-108">*agente. \* \* \* connesso* \*  \[  =  *valore booleano*\]</span><span class="sxs-lookup"><span data-stu-id="47f26-108">*agent.\*\*\*Connected*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="47f26-109">Parte</span><span class="sxs-lookup"><span data-stu-id="47f26-109">Part</span></span>      | <span data-ttu-id="47f26-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47f26-110">Description</span></span>                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47f26-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="47f26-111">*boolean*</span></span> | <span data-ttu-id="47f26-112">Espressione booleana che specifica se il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="47f26-112">A Boolean expression specifying whether the control is connected.</span></span> <span data-ttu-id="47f26-113">Valore **true** Il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="47f26-113">**True** The control is connected.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47f26-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="47f26-114">Remarks</span></span>

<span data-ttu-id="47f26-115">In molte situazioni, l'impostazione del controllo crea automaticamente una connessione al server Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="47f26-115">In many situations, specifying the control automatically creates a connection with the Microsoft Agent server.</span></span> <span data-ttu-id="47f26-116">Se, ad esempio, si specifica il CLSID del controllo Microsoft Agent nel <OBJECT> tag in una pagina Web, viene aperta automaticamente una connessione al server e l'uscita dalla pagina chiude la connessione.</span><span class="sxs-lookup"><span data-stu-id="47f26-116">For example, specifying the Microsoft Agent control's CLSID in the <OBJECT> tag in a webpage automatically opens a server connection and exiting the page closes the connection.</span></span> <span data-ttu-id="47f26-117">Analogamente, per Visual Basic o altri linguaggi che consentono di eliminare un controllo in un form, l'esecuzione del programma apre automaticamente una connessione e l'uscita dal programma chiude la connessione.</span><span class="sxs-lookup"><span data-stu-id="47f26-117">Similarly, for Visual Basic or other languages that enable you to drop a control on a form, running the program automatically opens a connection and exiting the program closes the connection.</span></span> <span data-ttu-id="47f26-118">Se il server non è attualmente in esecuzione, viene avviato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="47f26-118">If the server isn't currently running, it automatically starts.</span></span>

<span data-ttu-id="47f26-119">Tuttavia, se si desidera creare un controllo agente in fase di esecuzione, potrebbe essere necessario aprire in modo esplicito una nuova connessione al server utilizzando la proprietà **connessa** .</span><span class="sxs-lookup"><span data-stu-id="47f26-119">However, if you want to create an Agent control at run time, you may also need to explicitly open a new connection to the server using the **Connected** property.</span></span> <span data-ttu-id="47f26-120">In Visual Basic, ad esempio, è possibile creare un oggetto ActiveX in fase di esecuzione usando l'istruzione set con la parola chiave **New** (o la funzione CreateObject).</span><span class="sxs-lookup"><span data-stu-id="47f26-120">For example, in Visual Basic you can create an ActiveX object at run time using the Set statement with the **New** keyword (or CreateObject function).</span></span> <span data-ttu-id="47f26-121">Durante la creazione dell'oggetto, è possibile che non crei la connessione al server.</span><span class="sxs-lookup"><span data-stu-id="47f26-121">While this creates the object, it may not create the connection to the server.</span></span> <span data-ttu-id="47f26-122">È possibile usare la proprietà **Connected** prima del codice che chiama l'interfaccia di programmazione di Microsoft Agent, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="47f26-122">You can use the **Connected** property before any code that calls into Microsoft Agent's programming interface, as shown in the following example:</span></span>


```
   ' Declare a global variable for the control
   Dim MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```



<span data-ttu-id="47f26-123">La creazione di un controllo utilizzando questa tecnica non espone gli eventi del controllo agente.</span><span class="sxs-lookup"><span data-stu-id="47f26-123">Creating a control using this technique does not expose the Agent control's events.</span></span> <span data-ttu-id="47f26-124">In Visual Basic 5,0 (e versioni successive) è possibile accedere agli eventi del controllo includendo il controllo nei riferimenti del progetto e usare la parola chiave **WithEvents** nella dichiarazione di variabile:</span><span class="sxs-lookup"><span data-stu-id="47f26-124">In Visual Basic 5.0 (and later), you can access the control's events by including the control in your project's references, and use the **WithEvents** keyword in your variable declaration:</span></span>


```
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent
```



<span data-ttu-id="47f26-125">L'utilizzo di **WithEvents** per creare un'istanza del controllo agente in fase di esecuzione apre automaticamente la connessione al server Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="47f26-125">Using **WithEvents** to create an instance of the Agent control at run time automatically opens the connection with the Microsoft Agent server.</span></span> <span data-ttu-id="47f26-126">Non è quindi necessario includere un'istruzione **connessa** .</span><span class="sxs-lookup"><span data-stu-id="47f26-126">Therefore, you don't need to include a **Connected** statement.</span></span>

<span data-ttu-id="47f26-127">È possibile chiudere la connessione al server rilasciando tutti i riferimenti creati agli oggetti di Agent, ad esempio IAgentCtlCharacterEx e IAgentCtlCommandEx.</span><span class="sxs-lookup"><span data-stu-id="47f26-127">You can close your connection to the server by releasing all references you created to Agent objects, such as IAgentCtlCharacterEx and IAgentCtlCommandEx.</span></span> <span data-ttu-id="47f26-128">È inoltre necessario rilasciare il riferimento al controllo agente stesso.</span><span class="sxs-lookup"><span data-stu-id="47f26-128">You must also release your reference to the Agent control itself.</span></span> <span data-ttu-id="47f26-129">In Visual Basic è possibile rilasciare un riferimento a un oggetto impostando la relativa variabile su **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="47f26-129">In Visual Basic, you can release a reference to an object by setting its variable to **Nothing**.</span></span> <span data-ttu-id="47f26-130">Se sono stati caricati caratteri, scaricarli prima di rilasciare l'oggetto carattere.</span><span class="sxs-lookup"><span data-stu-id="47f26-130">If you have loaded characters, unload them before releasing the character object.</span></span>


```
   Dim WithEvents MyAgent as Agent
   Dim Genie as IAgentCtlCharacterEx
   
   Sub Form_Load

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load the character into the Characters collection
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Create a reference to the character
   Set Genie = MyAgent.Characters("Genie")

   End Sub

   Sub CloseConnection

   ' Unload the character
   MyAgent.Characters.Unload "Genie"

   ' Release the reference to the character object
   Set Genie = Nothing

   ' Release the reference to the Agent control
   Set MyAgent = Nothing
   End Sub
```



> [!Note]  
> <span data-ttu-id="47f26-131">Non è possibile chiudere la connessione al server rilasciando i riferimenti in cui è stato aggiunto il componente.</span><span class="sxs-lookup"><span data-stu-id="47f26-131">You cannot close your connection to the server by releasing references where the component has been added.</span></span> <span data-ttu-id="47f26-132">Non è ad esempio possibile chiudere la connessione al server nelle pagine Web in cui si usa il <OBJECT> tag per dichiarare il controllo o in un'applicazione Visual Basic in cui si rilascia il controllo in un form.</span><span class="sxs-lookup"><span data-stu-id="47f26-132">For example, you cannot close your connection to the server on webpages where you use the <OBJECT> tag to declare the control or in a Visual Basic application where you drop the control on a form.</span></span> <span data-ttu-id="47f26-133">Quando si rilasciano tutti i riferimenti all'agente, il working set dell'agente viene ridotto, la connessione rimane fino a quando non si passa alla pagina successiva o si esce dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="47f26-133">While releasing all Agent references will reduce Agent's working set, the connection remains until you navigate to the next page or exit the application.</span></span>

 

 

 





