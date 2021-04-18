---
description: In questa sezione viene descritto come stampare da un programma Windows nativo.
ms.assetid: D0AE8FF8-D02D-43D3-80CA-E13EAA894F87
title: 'Procedura: stampare da un programma Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84229823944d7f7104da359b953e579f1b21cdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318378"
---
# <a name="how-to-print-from-a-windows-program"></a><span data-ttu-id="babff-103">Procedura: stampare da un programma Windows</span><span class="sxs-lookup"><span data-stu-id="babff-103">How To: Print from a Windows Program</span></span>

<span data-ttu-id="babff-104">In questa sezione viene descritto come stampare da un programma Windows nativo.</span><span class="sxs-lookup"><span data-stu-id="babff-104">This section describes how to print from a native Windows program.</span></span>

## <a name="overview"></a><span data-ttu-id="babff-105">Panoramica</span><span class="sxs-lookup"><span data-stu-id="babff-105">Overview</span></span>

<span data-ttu-id="babff-106">La stampa è in genere parte integrante di un programma Windows nativo.</span><span class="sxs-lookup"><span data-stu-id="babff-106">Printing is usually an integral part of a native Windows program.</span></span> <span data-ttu-id="babff-107">Pertanto, non è una funzionalità che è possibile aggiungere facilmente dopo aver scritto il programma.</span><span class="sxs-lookup"><span data-stu-id="babff-107">Therefore, it is not a feature that you can add easily after you have written the program.</span></span> <span data-ttu-id="babff-108">Detto questo, se il programma è progettato per l'utilizzo di documenti XPS, non sarà necessario molto altro codice aggiuntivo per eseguire il rendering del contenuto del documento per la stampa.</span><span class="sxs-lookup"><span data-stu-id="babff-108">That being said, if the program is designed to use XPS documents it will not need much, if any, additional code to render the document content for printing.</span></span> <span data-ttu-id="babff-109">I documenti XPS dell'applicazione possono essere inviati direttamente a una stampante che dispone di un driver della stampante XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="babff-109">The XPS documents of the application can be sent directly to a printer that has an XPSDrv printer driver.</span></span>

<span data-ttu-id="babff-110">Utilizzare l' [API documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) per creare il contenuto del documento e l' [API di stampa XPS](xps-printing.md) per inviare il contenuto del documento alla stampante.</span><span class="sxs-lookup"><span data-stu-id="babff-110">Use the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) to create the document content and the [XPS Print API](xps-printing.md) to send the document content to the printer.</span></span> <span data-ttu-id="babff-111">L'API di stampa XPS elabora il contenuto del documento per la stampante di destinazione.</span><span class="sxs-lookup"><span data-stu-id="babff-111">The XPS Print API processes the document content for the destination printer.</span></span> <span data-ttu-id="babff-112">Se la stampante selezionata dispone di un driver della stampante XPSDrv, il documento verrà inviato alla stampante senza alcuna conversione aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="babff-112">If the selected printer has an XPSDrv printer driver, the document will be sent to the printer without any additional conversion.</span></span> <span data-ttu-id="babff-113">Se la stampante selezionata dispone di un driver della stampante basato su GDI, il programma può anche inviare il contenuto alla stampante e l'API di stampa XPS converte il contenuto del documento in modo che sia compatibile con il driver della stampante basato su GDI.</span><span class="sxs-lookup"><span data-stu-id="babff-113">If the selected printer has a GDI-based printer driver, the program can also send the content to the printer, and the XPS Print API converts the document content so that it will be compatible with the GDI-based printer driver.</span></span> <span data-ttu-id="babff-114">In entrambi i casi, l'elaborazione eseguita dall'applicazione è la stessa.</span><span class="sxs-lookup"><span data-stu-id="babff-114">In either case, the processing that the application performs is the same.</span></span>

## <a name="printing-tasks"></a><span data-ttu-id="babff-115">Attività di stampa</span><span class="sxs-lookup"><span data-stu-id="babff-115">Printing tasks</span></span>

<span data-ttu-id="babff-116">Negli argomenti seguenti vengono descritti i passaggi di base per la stampa del contenuto del programma.</span><span class="sxs-lookup"><span data-stu-id="babff-116">The following topics describe the basic steps of printing program content.</span></span>

1.  <span data-ttu-id="babff-117">**Raccoglie le informazioni sul processo di stampa dall'utente.**</span><span class="sxs-lookup"><span data-stu-id="babff-117">**Collect print job information from user.**</span></span>

    <span data-ttu-id="babff-118">In genere, un utente avvia un processo di stampa quando seleziona l'opzione stampa da un menu e il programma visualizza una finestra di dialogo Stampa per raccogliere i dettagli del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="babff-118">Typically, a user initiates a print job when they select the print option from a menu and the program displays a print dialog box to collect the details of the print job.</span></span> <span data-ttu-id="babff-119">L'utente in genere seleziona la stampante, il numero di copie e i dettagli di configurazione della stampante, ad esempio la stampa su due lati e la graffettatura.</span><span class="sxs-lookup"><span data-stu-id="babff-119">The user typically selects the printer, the number of copies, and printer configuration details such as two-sided printing and stapling.</span></span>

    <span data-ttu-id="babff-120">Per informazioni su come eseguire questa operazione, vedere [procedura: raccogliere informazioni sui processi di stampa dall'utente](preparing-to-print.md).</span><span class="sxs-lookup"><span data-stu-id="babff-120">For information about how to do this, see [How To: Collect Print Job Information from the User](preparing-to-print.md).</span></span>

2.  <span data-ttu-id="babff-121">**Creazione indicatore di stato.**</span><span class="sxs-lookup"><span data-stu-id="babff-121">**Create progress indicator.**</span></span>

    <span data-ttu-id="babff-122">Un indicatore di stato consente all'utente di ricevere commenti e suggerimenti sull'avanzamento del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="babff-122">A progress indicator provides the user with feedback about how the print job is progressing.</span></span> <span data-ttu-id="babff-123">L'indicatore di stato può essere una barra di stato che fa parte di una finestra di dialogo che include il pulsante **Annulla** per il processo oppure un indicatore di stato nella barra di stato nella parte inferiore della finestra principale.</span><span class="sxs-lookup"><span data-stu-id="babff-123">The progress indicator can be a progress bar that is part of a dialog box that includes the **Cancel** button for the job, or it can be a progress bar in the status bar at the bottom of the main window.</span></span>

    <span data-ttu-id="babff-124">Per informazioni sul funzionamento dell'indicatore di stato, vedere [procedura: visualizzare lo stato di avanzamento del processo di stampa](cancel-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="babff-124">For information about the progress indicator works, see [How To: Display the Print Job Progress](cancel-dialog-box.md).</span></span>

    <span data-ttu-id="babff-125">Per ulteriori informazioni su come visualizzare lo stato di avanzamento del processo di stampa, vedere le informazioni nelle linee guida per [lo sviluppo dell'interfaccia utente delle applicazioni Windows](/windows/desktop/windows-application-ui-development) .</span><span class="sxs-lookup"><span data-stu-id="babff-125">For more ideas about how to display the progress of the print job, see the information in the [Windows Application UI Development](/windows/desktop/windows-application-ui-development) guidelines.</span></span>

3.  <span data-ttu-id="babff-126">**Avviare il thread di stampa.**</span><span class="sxs-lookup"><span data-stu-id="babff-126">**Start the printing thread.**</span></span>

    <span data-ttu-id="babff-127">Dopo che il programma ha raccolto le informazioni sul processo di stampa dall'utente, può avviare il thread di stampa per eseguire l'elaborazione effettiva del documento per la stampa.</span><span class="sxs-lookup"><span data-stu-id="babff-127">After the program has collected the print job information from the user, it can start the printing thread to perform the actual processing of the document for printing.</span></span>

    <span data-ttu-id="babff-128">Per informazioni sul thread di stampa, vedere [procedura: avviare e arrestare un thread di stampa](how-to--start-and-stop-a-printing-thread.md).</span><span class="sxs-lookup"><span data-stu-id="babff-128">For information about the printing thread, see [How To: Start and Stop a Printing Thread](how-to--start-and-stop-a-printing-thread.md).</span></span>

4.  <span data-ttu-id="babff-129">**Rendering dei dati del processo di stampa.**</span><span class="sxs-lookup"><span data-stu-id="babff-129">**Render print job data.**</span></span>

    <span data-ttu-id="babff-130">Il thread di stampa esegue il rendering dei dati del documento per la stampa.</span><span class="sxs-lookup"><span data-stu-id="babff-130">The printing thread renders the document data for printing.</span></span> <span data-ttu-id="babff-131">È consigliabile suddividere questa elaborazione in passaggi di elaborazione discreti in modo che l'utente possa interrompere l'elaborazione e annullare il processo, oltre a non consentire al thread di elaborazione di bloccare altri thread e processi.</span><span class="sxs-lookup"><span data-stu-id="babff-131">You should break down this processing into discrete processing steps so that the user can interrupt the processing and cancel the job as well as to not allow the processing thread to block other threads and processes.</span></span>

    <span data-ttu-id="babff-132">Per informazioni sul rendering dei dati del processo di stampa, vedere [procedura: eseguire il rendering dei dati dei processi di stampa](how-to--render-the-print-job-data.md).</span><span class="sxs-lookup"><span data-stu-id="babff-132">For information about how the renders the print job data, see [How To: Render Print Job Data](how-to--render-the-print-job-data.md).</span></span>

5.  <span data-ttu-id="babff-133">**Monitorare lo stato del processo di stampa.**</span><span class="sxs-lookup"><span data-stu-id="babff-133">**Monitor print job progress.**</span></span>

    <span data-ttu-id="babff-134">Quando si esegue ogni passaggio di elaborazione, aggiornare l'indicatore di stato per informare l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="babff-134">As each processing step is performed, update the progress bar to inform the use.</span></span> <span data-ttu-id="babff-135">Calcolare i passaggi di elaborazione per completare il processo richiesto e quindi aggiornare l'indicatore di stato durante l'esecuzione di questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="babff-135">Compute the processing steps to complete the requested job and then updates the progress bar as those steps are performed.</span></span>

6.  <span data-ttu-id="babff-136">**Chiudere il processo di stampa e terminare il thread di stampa.**</span><span class="sxs-lookup"><span data-stu-id="babff-136">**Close print job and terminate printing thread.**</span></span>

    <span data-ttu-id="babff-137">Dopo che il programma ha inviato il processo di stampa alla stampante o se l'utente ha annullato il processo di stampa, è necessario chiudere il processo di stampa e rilasciare le risorse utilizzate dal processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="babff-137">After the program has sent the print job to the printer, or if the user has cancelled the print job, you must close the print job and release the resources used by the print job.</span></span>

## <a name="related-topics"></a><span data-ttu-id="babff-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="babff-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="babff-139">Procedura: raccogliere informazioni sui processi di stampa dall'utente</span><span class="sxs-lookup"><span data-stu-id="babff-139">How To: Collect Print Job Information from the User</span></span>](preparing-to-print.md)
</dt> </dl>

 

 
