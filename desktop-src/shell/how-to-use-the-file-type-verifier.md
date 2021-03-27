---
description: In questo argomento viene descritto come utilizzare il verificatore del tipo di file fornito in Windows 7 SDK.
ms.assetid: 96FCA74B-DEB2-49D1-B670-EBD8BE0783F1
title: Come utilizzare il tipo di file Verifier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f083897499f972f945867a0c02318df192e734d9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104234395"
---
# <a name="how-to-use-the-file-type-verifier"></a><span data-ttu-id="ace24-103">Come utilizzare il tipo di file Verifier</span><span class="sxs-lookup"><span data-stu-id="ace24-103">How to Use the File Type Verifier</span></span>

<span data-ttu-id="ace24-104">In questo argomento viene descritto come utilizzare il verificatore del tipo di file fornito in [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ace24-104">This topic describes how to use the File Type Verifier that is provided in the [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ace24-105">Se il programma crea tipi di file con cui gli utenti si aspettano di interagire dalla shell di Windows (in genere archiviati in una cartella nota dell'utente, ad esempio **documenti**), è molto importante testare l'applicazione e verificare che i file creati siano registrati correttamente e fornire un'esperienza utente di alta qualità durante l'esplorazione e la ricerca di file.</span><span class="sxs-lookup"><span data-stu-id="ace24-105">If your program creates file types that users are expected to interact with from the Windows Shell (typically stored in a user's known folder such as **My Documents**), it is very important to test your application and verify that the files it creates are properly registered and provide a high-quality user experience when browsing and searching files.</span></span> <span data-ttu-id="ace24-106">Questo è particolarmente importante se si prevede che gli utenti eseguano le applicazioni in Windows 7, che si basa su gestori di tipi di file di alta qualità per molte delle funzionalità della shell.</span><span class="sxs-lookup"><span data-stu-id="ace24-106">This is especially important if you expect users to run your applications on Windows 7, which relies on high-quality file type handlers for many of the Shell features.</span></span>

<span data-ttu-id="ace24-107">Per verificare il tipo di file utilizzando il tipo di file Verifier, attenersi alla seguente procedura.</span><span class="sxs-lookup"><span data-stu-id="ace24-107">To verify your file type using the File Type Verifier, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="ace24-108">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="ace24-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="ace24-109">Passaggio 1:</span><span class="sxs-lookup"><span data-stu-id="ace24-109">Step 1:</span></span>

<span data-ttu-id="ace24-110">Installare l'applicazione nell'ambiente di test e copiare il tipo di file Verifier in tale ambiente.</span><span class="sxs-lookup"><span data-stu-id="ace24-110">Install the application on your test environment, and copy the File Type Verifier to that environment.</span></span> <span data-ttu-id="ace24-111">Il verificatore del tipo di file è disponibile in [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ace24-111">The File Type Verifier is available in the [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

### <a name="step-2"></a><span data-ttu-id="ace24-112">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="ace24-112">Step 2:</span></span>

<span data-ttu-id="ace24-113">Usare l'applicazione per creare un file da testare.</span><span class="sxs-lookup"><span data-stu-id="ace24-113">Use your application to create a file to be tested.</span></span>

### <a name="step-3"></a><span data-ttu-id="ace24-114">Passaggio 3:</span><span class="sxs-lookup"><span data-stu-id="ace24-114">Step 3:</span></span>

<span data-ttu-id="ace24-115">Avviare il Verifier del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="ace24-115">Start the File Type Verifier.</span></span>

### <a name="step-4"></a><span data-ttu-id="ace24-116">Passaggio 4:</span><span class="sxs-lookup"><span data-stu-id="ace24-116">Step 4:</span></span>

<span data-ttu-id="ace24-117">Selezionare la categoria per il tipo di file, come illustrato nella schermata seguente.</span><span class="sxs-lookup"><span data-stu-id="ace24-117">Select the category for your file type, as shown in the following screen shot.</span></span>

![Screenshot che mostra la funzione di trascinamento della selezione.](images/file-assoc/filetypeverifier1.png)

<span data-ttu-id="ace24-119">La selezione della categoria determina il set di test che verranno eseguiti dallo strumento.</span><span class="sxs-lookup"><span data-stu-id="ace24-119">The category selection determines the set of tests that will be run by the tool.</span></span> <span data-ttu-id="ace24-120">Se il tipo può rientrare in più di una categoria, ad esempio un file TIF può essere un'immagine o un documento a seconda del contenuto, eseguire di nuovo lo strumento con ogni categoria appropriata.</span><span class="sxs-lookup"><span data-stu-id="ace24-120">If your type could fall under more than one category (for example, a TIF file might be a Picture or a Document depending on the content), run the tool again with each appropriate category.</span></span>

### <a name="step-5"></a><span data-ttu-id="ace24-121">Passaggio 5:</span><span class="sxs-lookup"><span data-stu-id="ace24-121">Step 5:</span></span>

<span data-ttu-id="ace24-122">Utilizzando Esplora risorse, individuare un file da testare e utilizzare il mouse per trascinarlo nella destinazione in tipo di file Verifier, come illustrato nella schermata seguente.</span><span class="sxs-lookup"><span data-stu-id="ace24-122">Using Windows Explorer, locate a file to be tested and use the mouse to drag it to the target in File Type Verifier, as shown in the following screen shot.</span></span>

![screenshot che mostra la funzione di trascinamento della selezione](images/file-assoc/filetypeverifier2.png)

### <a name="step-6"></a><span data-ttu-id="ace24-124">Passaggio 6:</span><span class="sxs-lookup"><span data-stu-id="ace24-124">Step 6:</span></span>

<span data-ttu-id="ace24-125">Attendere che lo strumento File Type Verifier continui a eseguire una serie di test.</span><span class="sxs-lookup"><span data-stu-id="ace24-125">Wait for the File Type Verifier tool to proceed through a series of tests.</span></span> <span data-ttu-id="ace24-126">Lo stato di avanzamento del test viene visualizzato dall'indicatore di stato, come nello screenshot seguente.</span><span class="sxs-lookup"><span data-stu-id="ace24-126">The progress of the testing is shown by the progress bar, as in the following screen shot.</span></span>

![screenshot che mostra l'indicatore di stato](images/file-assoc/filetypeverifier3.png)

### <a name="step-7"></a><span data-ttu-id="ace24-128">Passaggio 7:</span><span class="sxs-lookup"><span data-stu-id="ace24-128">Step 7:</span></span>

<span data-ttu-id="ace24-129">Esaminare il riepilogo dei risultati dei test del tipo di file di documento, come illustrato nella schermata seguente.</span><span class="sxs-lookup"><span data-stu-id="ace24-129">Review the results summary of your Document file type tests, as shown in the following screen shot.</span></span>

![screenshot che mostra il riepilogo dei risultati](images/file-assoc/filetypeverifier4.png)

### <a name="step-8"></a><span data-ttu-id="ace24-131">Passaggio 8:</span><span class="sxs-lookup"><span data-stu-id="ace24-131">Step 8:</span></span>

<span data-ttu-id="ace24-132">Fare clic su uno dei risultati nella pagina Riepilogo per visualizzare il log dettagliato.</span><span class="sxs-lookup"><span data-stu-id="ace24-132">Click any of the results on the summary page to view the detailed log.</span></span> <span data-ttu-id="ace24-133">Uno dei log di esempio per un gestore di anteprime è illustrato nella schermata seguente.</span><span class="sxs-lookup"><span data-stu-id="ace24-133">An example log for a preview handler is shown in the following screen shot.</span></span>

![screenshot che mostra il log del gestore di anteprime](images/file-assoc/filetypeverifier5.png)

### <a name="step-9"></a><span data-ttu-id="ace24-135">Passaggio 9:</span><span class="sxs-lookup"><span data-stu-id="ace24-135">Step 9:</span></span>

<span data-ttu-id="ace24-136">Per salvare una copia del file di log, fare clic su **Salva file di log** nella parte inferiore della visualizzazione del log e scegliere un percorso appropriato per archiviarlo nel computer.</span><span class="sxs-lookup"><span data-stu-id="ace24-136">To save a copy of the log file, click **Save Log File** at the bottom of the log display and choose an appropriate location for storing it on your computer.</span></span>

### <a name="step-10"></a><span data-ttu-id="ace24-137">Passaggio 10:</span><span class="sxs-lookup"><span data-stu-id="ace24-137">Step 10:</span></span>

<span data-ttu-id="ace24-138">Se vengono segnalati errori, apportare le modifiche appropriate all'applicazione ed eseguire di nuovo lo strumento per verificare che gli errori non vengano più visualizzati nei test.</span><span class="sxs-lookup"><span data-stu-id="ace24-138">If failures are reported, make the appropriate changes in your application and run the tool again to verify that the failures are no longer showing up in the tests.</span></span> <span data-ttu-id="ace24-139">Se vengono restituiti avvisi, valutarli e decidere se sono rilevanti per il tipo di file specifico e apportare le modifiche appropriate all'applicazione in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="ace24-139">If warnings are reported, evaluate them and decide whether they are relevant for your particular file type and make the appropriate changes to your application as necessary.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ace24-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ace24-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ace24-141">Windows 7 SDK</span><span class="sxs-lookup"><span data-stu-id="ace24-141">Windows 7 SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
</dt> </dl>

 

 



