---
title: Metodo Load
description: Metodo Load
ms.assetid: 72a37471-f69b-49a5-a6eb-d65bff970c0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0927fc8e49e55c2bdfcd7b1109bb8604540c199c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299699"
---
# <a name="load-method"></a><span data-ttu-id="8b27b-103">Metodo Load</span><span class="sxs-lookup"><span data-stu-id="8b27b-103">Load Method</span></span>

<span data-ttu-id="8b27b-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8b27b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8b27b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="8b27b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8b27b-106">Carica un carattere nella raccolta di [**caratteri**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="8b27b-106">Loads a character into the [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="8b27b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="8b27b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8b27b-108">\*agente ***. Characters. Load "*** CharacterID \* \* *",* \*  *provider*</span><span class="sxs-lookup"><span data-stu-id="8b27b-108">*agent ***.Characters.Load "*** CharacterID\*\*\*",*\* *Provider*</span></span>



| <span data-ttu-id="8b27b-109">Parte</span><span class="sxs-lookup"><span data-stu-id="8b27b-109">Part</span></span>          | <span data-ttu-id="8b27b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b27b-110">Description</span></span>                                                                                                                                                                                                                              |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b27b-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="8b27b-111">*CharacterID*</span></span> | <span data-ttu-id="8b27b-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8b27b-112">Required.</span></span> <span data-ttu-id="8b27b-113">Valore stringa che verrà utilizzato per fare riferimento ai dati di tipo carattere da caricare.</span><span class="sxs-lookup"><span data-stu-id="8b27b-113">A string value that you will use to refer to the character data to be loaded.</span></span>                                                                                                                                                  |
| <span data-ttu-id="8b27b-114">*Provider*</span><span class="sxs-lookup"><span data-stu-id="8b27b-114">*Provider*</span></span>    | <span data-ttu-id="8b27b-115">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8b27b-115">Required.</span></span> <span data-ttu-id="8b27b-116">Tipo di dati Variant che deve essere uno dei seguenti: **filespec** il percorso del file locale del file di definizione del carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="8b27b-116">A variant data type that must be one of the following: **Filespec** The local file location of the specified character's definition file.</span></span> <br/> <span data-ttu-id="8b27b-117">**URL** di Indirizzo HTTP per il file di definizione del carattere.</span><span class="sxs-lookup"><span data-stu-id="8b27b-117">**URL** The HTTP address for the character's definition file.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b27b-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="8b27b-118">Remarks</span></span>

<span data-ttu-id="8b27b-119">È possibile caricare caratteri dalla sottodirectory Agent specificando un percorso relativo (uno che non include i due punti o il carattere barra rovesciata).</span><span class="sxs-lookup"><span data-stu-id="8b27b-119">You can load characters from the Agent subdirectory by specifying a relative path (one that does not include a colon or leading slash character).</span></span> <span data-ttu-id="8b27b-120">Questa operazione previene il prefisso del percorso con la directory characters di Agent, che si trova nella directory msagent di Windows localizzata \\ .</span><span class="sxs-lookup"><span data-stu-id="8b27b-120">This prefixes the path with Agent's characters directory (located in the localized Windows\\msagent directory).</span></span> <span data-ttu-id="8b27b-121">Ad esempio, se si specifica quanto segue, viene caricato Genie. ACS dalla directory chars dell'agente:</span><span class="sxs-lookup"><span data-stu-id="8b27b-121">For example, specifying the following would load Genie.acs from Agent's Chars directory:</span></span>


```
   Agent.Character.Load "genie", "genie.acs"
```



<span data-ttu-id="8b27b-122">È anche possibile specificare la propria directory nella directory chars dell'agente.</span><span class="sxs-lookup"><span data-stu-id="8b27b-122">You can also specify your own directory in Agent's Chars directory.</span></span>


```
   Agent.Character.Load "genie", "MyCharacters\genie.acs"
```



<span data-ttu-id="8b27b-123">È possibile caricare il carattere attualmente impostato come carattere predefinito dell'utente corrente senza includere un percorso come secondo parametro del metodo **Load** .</span><span class="sxs-lookup"><span data-stu-id="8b27b-123">You can load the character currently set as the current user's default character by not including a path as the second parameter of the **Load** method.</span></span>


```
   Agent.Character.Load "character"
```



<span data-ttu-id="8b27b-124">Non è possibile caricare più volte lo stesso carattere, ovvero un carattere con lo stesso GUID, da una singola istanza del controllo.</span><span class="sxs-lookup"><span data-stu-id="8b27b-124">You cannot load the same character (a character having the same GUID) more than once from a single instance of the control.</span></span> <span data-ttu-id="8b27b-125">Analogamente, non è possibile caricare contemporaneamente il carattere predefinito e altri caratteri da una singola istanza del controllo, poiché il carattere predefinito potrebbe essere uguale a quello dell'altro carattere.</span><span class="sxs-lookup"><span data-stu-id="8b27b-125">Similarly, you cannot load the default character and other characters at the same time from a single instance of the control because the default character could be the same as the other character.</span></span> <span data-ttu-id="8b27b-126">Se si tenta di eseguire questa operazione, il server genera un errore.</span><span class="sxs-lookup"><span data-stu-id="8b27b-126">If you attempt to do this, the server raises an error.</span></span> <span data-ttu-id="8b27b-127">Tuttavia, è possibile creare un'altra istanza del controllo agente e caricare lo stesso carattere.</span><span class="sxs-lookup"><span data-stu-id="8b27b-127">However, you can create another instance of the Agent control and load the same character.</span></span>

<span data-ttu-id="8b27b-128">Il provider di dati Microsoft Agent supporta il caricamento di dati di tipo carattere archiviati come singolo file strutturato (. ACS) con dati di tipo carattere e dati di animazione insieme o come dati di tipo carattere separati (. ACF) e animazione (. File ACA).</span><span class="sxs-lookup"><span data-stu-id="8b27b-128">The Microsoft Agent Data Provider supports loading character data stored either as a single structured file (.ACS) with character data and animation data together or as separate character data (.ACF) and animation (.ACA) files.</span></span> <span data-ttu-id="8b27b-129">Usare il singolo oggetto strutturato. File ACS per caricare un carattere archiviato in un disco locale o in una rete a cui si accede utilizzando un protocollo file convenzionale, ad esempio i percorsi UNC.</span><span class="sxs-lookup"><span data-stu-id="8b27b-129">Use the single structured .ACS file to load a character that is stored on a local disk or network and accessed using a conventional file protocol (such as UNC pathnames).</span></span> <span data-ttu-id="8b27b-130">Usare l'oggetto separato. ACF e. File ACA quando si desidera caricare i file di animazione singolarmente da un sito remoto a cui si accede utilizzando il protocollo HTTP.</span><span class="sxs-lookup"><span data-stu-id="8b27b-130">Use the separate .ACF and .ACA files when you want to load the animation files individually from a remote site where they are accessed using the HTTP protocol.</span></span>

<span data-ttu-id="8b27b-131">Per. I file ACS, usando il metodo **Load** , consentono di accedere alle animazioni di un carattere.</span><span class="sxs-lookup"><span data-stu-id="8b27b-131">For .ACS files, using the **Load** method provides access to a character's animations.</span></span> <span data-ttu-id="8b27b-132">Per. File ACF, viene usato anche il metodo [**Get**](get-method.md) per caricare i dati dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="8b27b-132">For .ACF files, you also use the [**Get**](get-method.md) method to load animation data.</span></span> <span data-ttu-id="8b27b-133">Il metodo **Load** non supporta il download. File ACS da un sito HTTP.</span><span class="sxs-lookup"><span data-stu-id="8b27b-133">The **Load** method does not support downloading .ACS files from an HTTP site.</span></span>

<span data-ttu-id="8b27b-134">Il caricamento di un carattere non visualizza automaticamente il carattere.</span><span class="sxs-lookup"><span data-stu-id="8b27b-134">Loading a character does not automatically display the character.</span></span> <span data-ttu-id="8b27b-135">Usare prima il metodo [**show**](show-method.md) per rendere visibile il carattere.</span><span class="sxs-lookup"><span data-stu-id="8b27b-135">Use the [**Show**](show-method.md) method first to make the character visible.</span></span>

<span data-ttu-id="8b27b-136">Se si usa il metodo **Load** per caricare un file di caratteri archiviato nel computer locale e la chiamata ha esito negativo; ad esempio, poiché il file non viene trovato, Agent genera un errore.</span><span class="sxs-lookup"><span data-stu-id="8b27b-136">If you use the **Load** method to load a character file stored on the local machine and the call fails; for example, because the file is not found, Agent raises an error.</span></span> <span data-ttu-id="8b27b-137">È possibile utilizzare il supporto nel linguaggio di programmazione per fornire una routine di gestione degli errori per intercettare ed elaborare l'errore.</span><span class="sxs-lookup"><span data-stu-id="8b27b-137">You can use the support in your programming language to provide an error handling routine to catch and process the error.</span></span>


```
   Sub Form_Load
      On Error GoTo ErrorHandler
      Agent1.Characters.Load "mychar", "genie.acs"
      ' Successful load
      . . .
      Exit Sub
      ErrorHandler:
      ' Unsuccessful load
      . . .
      Resume Next
   End Sub
```



<span data-ttu-id="8b27b-138">È anche possibile gestire l'errore impostando [**RaiseRequestErrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) su **false**, dichiarando un oggetto e assegnando la richiesta di **caricamento** .</span><span class="sxs-lookup"><span data-stu-id="8b27b-138">You can also handle the error by setting [**RaiseRequestErrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) to **False**, declaring a object, and assigning the **Load** request to it.</span></span> <span data-ttu-id="8b27b-139">Seguire quindi la chiamata di **caricamento** con un'istruzione che controlla lo stato dell'oggetto [**Request**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="8b27b-139">Then follow the **Load** call with a statement that checks the status of the [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>


```
Dim LoadRequest as Object

   Sub Form_Load
      Agent1.RaiseRequestErrors = False
      Set LoadRequest = Agent1.Characters.Load _
         ("mychar", "c:\some directory\some character.acs")
      If LoadRequest.Status Not 0 Then
         ' Unsuccessful load
         . . .
         Exit Sub
      Else 
         ' Successful load
         . . .
   End Sub
```



<span data-ttu-id="8b27b-140">Se si carica un carattere non locale; Se ad esempio si usa il protocollo HTTP, è anche possibile verificare la presenza di un errore di **caricamento** assegnando un oggetto [**Request**](/windows/desktop/lwef/the-request-object) al metodo **Load** .</span><span class="sxs-lookup"><span data-stu-id="8b27b-140">If you load a character that is not local; for example, using HTTP protocol, you can also check for a **Load** failure by assigning a [**Request**](/windows/desktop/lwef/the-request-object) object to the **Load** method.</span></span> <span data-ttu-id="8b27b-141">Tuttavia, poiché questo metodo di caricamento di un carattere viene gestito in modo asincrono, verificarne lo stato nell'evento [**RequestComplete**](requestcomplete-event.md) .</span><span class="sxs-lookup"><span data-stu-id="8b27b-141">However, because this method of loading a character is handled asynchronously, check its status in the [**RequestComplete**](requestcomplete-event.md) event.</span></span> <span data-ttu-id="8b27b-142">Questa tecnica non funzionerà il caricamento di un carattere usando il protocollo UNC perché il metodo **Load** viene elaborato in modo sincrono.</span><span class="sxs-lookup"><span data-stu-id="8b27b-142">This technique will not work loading a character using the UNC protocol because the **Load** method is processed synchronously.</span></span>

 

