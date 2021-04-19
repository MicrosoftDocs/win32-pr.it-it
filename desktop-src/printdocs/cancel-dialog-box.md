---
description: In questo argomento viene descritto come visualizzare l'avanzamento del processo di stampa per l'utente e assegnare loro l'opzione per annullare un processo di stampa attualmente in corso.
ms.assetid: 2b7a0ab7-bf7e-473d-ab43-8b79478d4453
title: 'Procedura: visualizzare lo stato di avanzamento del processo di stampa'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9effc778f6affaba5b53cbd96a7a428ea5554d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311834"
---
# <a name="how-to-display-the-print-job-progress"></a><span data-ttu-id="6a54e-103">Procedura: visualizzare lo stato di avanzamento del processo di stampa</span><span class="sxs-lookup"><span data-stu-id="6a54e-103">How To: Display the Print Job Progress</span></span>

<span data-ttu-id="6a54e-104">In questo argomento viene descritto come visualizzare l'avanzamento del processo di stampa per l'utente e assegnare loro l'opzione per annullare un processo di stampa attualmente in corso.</span><span class="sxs-lookup"><span data-stu-id="6a54e-104">This topic describes how to display the print job progress to the user and give them the option to cancel a print job that is currently in progress.</span></span>

## <a name="overview"></a><span data-ttu-id="6a54e-105">Panoramica</span><span class="sxs-lookup"><span data-stu-id="6a54e-105">Overview</span></span>

<span data-ttu-id="6a54e-106">Una routine della finestra di dialogo stato di stampa esegue in genere le funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="6a54e-106">A print progress dialog procedure typically performs the following functions.</span></span>

-   <span data-ttu-id="6a54e-107">Visualizza lo stato del processo di stampa per l'utente.</span><span class="sxs-lookup"><span data-stu-id="6a54e-107">Display print job progress to the user.</span></span>
-   <span data-ttu-id="6a54e-108">Avviare il thread di elaborazione stampa.</span><span class="sxs-lookup"><span data-stu-id="6a54e-108">Start the print processing thread.</span></span>
-   <span data-ttu-id="6a54e-109">Consente di visualizzare un pulsante **Annulla** per consentire all'utente di arrestare un processo di stampa prima del completamento.</span><span class="sxs-lookup"><span data-stu-id="6a54e-109">Display a **Cancel** button so the user can stop a print job before it finishes.</span></span>

<span data-ttu-id="6a54e-110">In modo rigoroso, l'unica cosa che la routine della finestra di dialogo stato di stampa deve eseguire è visualizzare l'avanzamento del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="6a54e-110">Strictly speaking, the only thing that the print progress dialog box procedure must do is display the print job progress to the user.</span></span> <span data-ttu-id="6a54e-111">Tuttavia, poiché le altre due funzioni nell'elenco precedente sono strettamente correlate, sono state incluse anche in questo modulo.</span><span class="sxs-lookup"><span data-stu-id="6a54e-111">However, because the other two functions in the preceding list are closely related, they have also been included in this module.</span></span>

## <a name="displaying-print-job-progress"></a><span data-ttu-id="6a54e-112">Visualizzazione dello stato del processo di stampa</span><span class="sxs-lookup"><span data-stu-id="6a54e-112">Displaying Print Job Progress</span></span>

<span data-ttu-id="6a54e-113">Una procedura di stampa dello stato di avanzamento della finestra di dialogo gestisce i messaggi della finestra seguenti.</span><span class="sxs-lookup"><span data-stu-id="6a54e-113">A print progress dialog box procedure handles the following window messages.</span></span>

-   <span data-ttu-id="6a54e-114">**\_INITDIALOG WM**</span><span class="sxs-lookup"><span data-stu-id="6a54e-114">**WM\_INITDIALOG**</span></span>

    <span data-ttu-id="6a54e-115">Inizializza i controlli utilizzati dalla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="6a54e-115">Initializes the controls that the dialog box uses.</span></span>

-   <span data-ttu-id="6a54e-116">**\_cursore WM**</span><span class="sxs-lookup"><span data-stu-id="6a54e-116">**WM\_SETCURSOR**</span></span>

    <span data-ttu-id="6a54e-117">Imposta il cursore su un puntatore quando l'utente è in grado di annullare un processo di stampa e al cursore di attesa quando il processo di stampa si trova in un punto in cui non può essere annullato.</span><span class="sxs-lookup"><span data-stu-id="6a54e-117">Sets the cursor to a pointer when the user is able to cancel a print job, and to the wait cursor when the print job is at a point where it cannot be cancelled.</span></span>

-   <span data-ttu-id="6a54e-118">**stampa \_ \_ inizio stampa \_ utente**</span><span class="sxs-lookup"><span data-stu-id="6a54e-118">**USER\_PRINT\_START\_PRINTING**</span></span>

    <span data-ttu-id="6a54e-119">Imposta i parametri dell'indicatore di stato per il processo di stampa e crea il thread di stampa per avviare l'elaborazione del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="6a54e-119">Sets the progress bar parameters for the print job, and creates the printing thread to start processing the print job.</span></span>

    <span data-ttu-id="6a54e-120">Si tratta di un messaggio di finestra specifico dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6a54e-120">This is an application-specific window message.</span></span>

-   <span data-ttu-id="6a54e-121">**\_comando WM-IDCANCEL**</span><span class="sxs-lookup"><span data-stu-id="6a54e-121">**WM\_COMMAND - IDCANCEL**</span></span>

    <span data-ttu-id="6a54e-122">Imposta l'evento Cancel per indicare al thread di elaborazione della stampa di annullare il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="6a54e-122">Sets the cancel event to tell the print processing thread to cancel the print job.</span></span>

-   <span data-ttu-id="6a54e-123">**\_ \_ aggiornamento dello stato di stampa dell'utente \_**</span><span class="sxs-lookup"><span data-stu-id="6a54e-123">**USER\_PRINT\_STATUS\_UPDATE**</span></span>

    <span data-ttu-id="6a54e-124">Aggiorna l'indicatore di stato e il testo dello stato per visualizzare lo stato corrente del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="6a54e-124">Updates the progress bar and status text to show the current state of the print job.</span></span>

    <span data-ttu-id="6a54e-125">Si tratta di un messaggio di finestra specifico dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6a54e-125">This is an application-specific window message.</span></span>

-   <span data-ttu-id="6a54e-126">**\_chiusura stampa \_ utente**</span><span class="sxs-lookup"><span data-stu-id="6a54e-126">**USER\_PRINT\_CLOSING**</span></span>

    <span data-ttu-id="6a54e-127">Imposta il testo dello stato di chiusura nella finestra di dialogo stato per indicare che il processo di stampa è in fase di chiusura.</span><span class="sxs-lookup"><span data-stu-id="6a54e-127">Sets the closing status text in the progress dialog box to indicate that the print job is closing.</span></span>

    <span data-ttu-id="6a54e-128">Si tratta di un messaggio di finestra specifico dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6a54e-128">This is an application-specific window message.</span></span>

-   <span data-ttu-id="6a54e-129">**\_stampa utente \_ completata**</span><span class="sxs-lookup"><span data-stu-id="6a54e-129">**USER\_PRINT\_COMPLETE**</span></span>

    <span data-ttu-id="6a54e-130">Visualizza il messaggio "stampa processo completato" per l'utente e rilascia handle ed eventi utilizzati in questo processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="6a54e-130">Displays the "Print job complete" message to the user, and releases handles and events that were used in this print job.</span></span>

    <span data-ttu-id="6a54e-131">Si tratta di un messaggio di finestra specifico dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6a54e-131">This is an application-specific window message.</span></span>

 

 



