---
title: Gestione degli errori (Windows Media Player SDK)
description: Gestione degli errori
ms.assetid: f0567c77-a855-4b93-9fb7-a36cde63859f
keywords:
- Windows Media Player, gestione degli errori
- Modello a oggetti di Windows Media Player, gestione degli errori
- modello a oggetti, gestione degli errori
- Controllo ActiveX di Windows Media Player, gestione degli errori
- Controllo ActiveX, gestione degli errori
- Controllo ActiveX Windows Media Player Mobile, gestione degli errori
- Windows Media Player Mobile, gestione degli errori
- Guida alla migrazione, gestione degli errori
- gestione degli errori nel modello a oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3b96e04d24009ee4b7e5819fdb26dfd6effd63
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118731"
---
# <a name="error-handling-windows-media-player-sdk"></a><span data-ttu-id="c8ba1-112">Gestione degli errori (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="c8ba1-112">Error Handling (Windows Media Player SDK)</span></span>

<span data-ttu-id="c8ba1-113">Il controllo ActiveX Windows Media Player 6,4 fornisce la gestione degli errori predefinita visualizzando i messaggi di errore nelle finestre di dialogo e sulla barra di stato.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-113">The Windows Media Player 6.4 ActiveX control provides default error handling by displaying error messages in dialog boxes and on the status bar.</span></span> <span data-ttu-id="c8ba1-114">È anche possibile fornire una gestione degli errori personalizzata elaborando gli errori nello script.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-114">You can also provide custom error handling by processing errors in your script.</span></span> <span data-ttu-id="c8ba1-115">La gestione degli errori è basata sugli eventi, ovvero si riceve una notifica per ogni errore e si deve decidere come gestire ogni evento di errore quando si verifica.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-115">Error handling is event driven, which means you receive a notification for each error, and must decide how to deal with each error event when it occurs.</span></span> <span data-ttu-id="c8ba1-116">Per ulteriori informazioni sulla gestione degli errori utilizzando il modello a oggetti della versione 6,4, vedere la sezione relativa alla gestione degli errori della guida del modello a oggetti di versione 6,4, che fa parte di Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-116">For more information about handling errors using the version 6.4 object model, see the Error Handling section of the Version 6.4 Player Object Model Guide, which is part of the Windows Media Player SDK.</span></span>

<span data-ttu-id="c8ba1-117">Il modello a oggetti di Windows Media Player 7 o versione successiva fornisce l'oggetto **errore** e l'oggetto **ErrorItem** per la gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-117">The Windows Media Player 7 or later object model provides the **Error** object and the **ErrorItem** object to handle errors.</span></span> <span data-ttu-id="c8ba1-118">Questi due oggetti interagiscono per fornire un meccanismo di gestione degli errori che offre un controllo completo e flessibile del processo di gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-118">These two objects work together to provide you with an error handling mechanism that gives you complete and flexible control of the error handling process.</span></span> <span data-ttu-id="c8ba1-119">L'oggetto **Error** fornisce l'accesso a una raccolta di oggetti **ErrorItem** . ogni oggetto **ErrorItem** fornisce informazioni dettagliate su un singolo messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-119">The **Error** object provides access to a collection of **ErrorItem** objects; each **ErrorItem** object provides details about an individual error message.</span></span>

<span data-ttu-id="c8ba1-120">Quando si verifica un errore, le informazioni sull'errore vengono inserite in una coda degli errori.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-120">When an error occurs, the error information is posted to an error queue.</span></span> <span data-ttu-id="c8ba1-121">La coda è una raccolta di oggetti **ErrorItem** .</span><span class="sxs-lookup"><span data-stu-id="c8ba1-121">The queue is a collection of **ErrorItem** objects.</span></span> <span data-ttu-id="c8ba1-122">Poiché ogni errore viene aggiunto alla coda, è associato a un numero di indice (a partire da zero) che può essere usato per identificare l'oggetto **ErrorItem** specifico.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-122">As each error is added to the queue, it is associated with an index number (beginning with zero) that can be used to identify the particular **ErrorItem** object.</span></span> <span data-ttu-id="c8ba1-123">*Errore*. la proprietà **ErrorCount** Recupera il numero di errori nella coda degli errori.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-123">The *Error*.**errorCount** property retrieves the number of errors in the error queue.</span></span> <span data-ttu-id="c8ba1-124">Poiché i numeri degli indici sono in base zero, l'errore più recente inserito nella coda avrà sempre un valore di indice uguale a *Error*. **ErrorCount** meno uno.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-124">Since the index numbers are zero-based, the most recent error posted to the queue will always have an index value equal to *Error*.**errorCount** minus one.</span></span>

<span data-ttu-id="c8ba1-125">È possibile creare un gestore eventi di errore per Windows Media Player tramite script.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-125">You can create an error event handler for Windows Media Player using script.</span></span> <span data-ttu-id="c8ba1-126">Nell'esempio JScript seguente viene illustrato come recuperare l'elemento di errore più recente dalla coda degli errori e visualizzare il codice di errore e la descrizione dell'errore utilizzando il modello a oggetti di Windows Media Player 7 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-126">The following JScript example shows how to retrieve the most recent error item from the error queue and display the error code and error description using the Windows Media Player 7 or later object model.</span></span> <span data-ttu-id="c8ba1-127">L'oggetto **Player** è stato creato con ID = "WMP9".</span><span class="sxs-lookup"><span data-stu-id="c8ba1-127">The **Player** object was created with ID = "WMP9".</span></span>


```C++
<!-- Create an error event handler for Windows Media Player 7 or later errors. -->
<SCRIPT  LANGUAGE = "JScript"  FOR = WMP9  EVENT = error()>

// Store the number of errors in the error queue.
var max = WMP9.error.errorCount;

// Retrieve most recent ErrorItem object.
var err = WMP9.error.item(max-1)

// Store the error code number.
var errNum = err.errorCode;

// Store the error description string.
var errDesc = err.errorDescription;

// Build a message string to notify the user.
var msg = "Error number: " + errNum + "\n";
msg += "Error description: " + errDesc;

// Display the message box.
alert(msg);

</SCRIPT>

```



<span data-ttu-id="c8ba1-128">L'oggetto **Error** dispone di due metodi aggiuntivi che è possibile utilizzare.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-128">The **Error** object has two additional methods that you can use.</span></span> <span data-ttu-id="c8ba1-129">*Errore*. il metodo **clearErrorQueue** consente di rimuovere tutti gli errori dalla coda degli errori e di reimpostare il numero di indice su zero.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-129">The *Error*.**clearErrorQueue** method allows you to remove all the errors from the error queue and reset the index number to zero.</span></span> <span data-ttu-id="c8ba1-130">Si dispone del controllo completo su questo processo; è possibile tenere gli errori nella coda per tutto il tempo necessario per renderli disponibili e quindi svuotare la coda al termine della gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-130">You have complete control over this process; you can keep errors in the queue for as long as you need them to be available, and then empty the queue when you're finished handling the errors.</span></span>

<span data-ttu-id="c8ba1-131">*Errore*. il metodo **WebHelp** consente di visualizzare all'utente le informazioni più aggiornate sull'errore tramite Internet.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-131">The *Error*.**webHelp** method provides a way to display the most current error information to the user by using the Internet.</span></span> <span data-ttu-id="c8ba1-132">Quando viene chiamato, questo metodo trasferisce tutte le informazioni rilevanti sul primo errore nella coda (quella con indice zero) a Microsoft Windows Media Player Guida Web, che consente di visualizzare ulteriori informazioni sull'errore nella finestra del browser corrente.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-132">When called, this method transfers all relevant information about the first error in the queue (the one with index zero) to Microsoft Windows Media Player Web Help, which displays further information about the error in the current browser window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8ba1-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c8ba1-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8ba1-134">**Oggetto Error**</span><span class="sxs-lookup"><span data-stu-id="c8ba1-134">**Error Object**</span></span>](error-object.md)
</dt> <dt>

[<span data-ttu-id="c8ba1-135">**Oggetto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="c8ba1-135">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="c8ba1-136">**Guida alla migrazione del modello a oggetti**</span><span class="sxs-lookup"><span data-stu-id="c8ba1-136">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




