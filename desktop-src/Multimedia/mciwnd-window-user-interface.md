---
title: Interfaccia utente della finestra MCIWnd
description: Interfaccia utente della finestra MCIWnd
ms.assetid: 422c5acb-bce5-4be2-96ba-5ab7f9dcc826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98c0b11b6868828625c6c6e605f005fe842d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044330"
---
# <a name="mciwnd-window-user-interface"></a><span data-ttu-id="825a2-103">Interfaccia utente della finestra MCIWnd</span><span class="sxs-lookup"><span data-stu-id="825a2-103">MCIWnd Window User Interface</span></span>

<span data-ttu-id="825a2-104">MCIWnd fornisce funzionalità aggiuntive per regolare l'aspetto della finestra MCIWnd, personalizzare il comportamento dell'applicazione e ottimizzare le prestazioni di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="825a2-104">MCIWnd provides additional features to adjust the look of the MCIWnd window, customize the behavior of your application, and tune playback performance.</span></span> <span data-ttu-id="825a2-105">Nella finestra MCIWnd sono incluse le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="825a2-105">The following features are included in the MCIWnd window:</span></span>

-   <span data-ttu-id="825a2-106">Barra degli strumenti con pulsanti di **riproduzione**, **arresto**, **record** e **menu**</span><span class="sxs-lookup"><span data-stu-id="825a2-106">A toolbar with **Play**, **Stop**, **Record** and **Menu** buttons</span></span>
-   <span data-ttu-id="825a2-107">TrackBar che controlla il posizionamento all'interno del contenuto di riproduzione</span><span class="sxs-lookup"><span data-stu-id="825a2-107">A trackbar that controls positioning within the playback content</span></span>
-   <span data-ttu-id="825a2-108">Menu di scelta rapida contenente i comandi comuni</span><span class="sxs-lookup"><span data-stu-id="825a2-108">A pop-up menu containing common commands</span></span>
-   <span data-ttu-id="825a2-109">Area di riproduzione per video e altri dispositivi che visualizzano immagini</span><span class="sxs-lookup"><span data-stu-id="825a2-109">A playback area for video and other devices that display images</span></span>

<span data-ttu-id="825a2-110">Nella figura seguente viene illustrato lo stato iniziale della riproduzione video controllata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="825a2-110">The following illustration shows the initial state of user-controlled video playback.</span></span> <span data-ttu-id="825a2-111">Il file di esempio usato è CLOCK.AVI.</span><span class="sxs-lookup"><span data-stu-id="825a2-111">The sample file used is CLOCK.AVI.</span></span>

![Immagine di clock.avi](images/mciwnd1.gif)

<span data-ttu-id="825a2-113">La finestra MCIWnd include un'area di riproduzione per video e altri dispositivi che visualizzano immagini durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="825a2-113">The MCIWnd window includes a playback area for video and other devices that display images during playback.</span></span> <span data-ttu-id="825a2-114">MCIWnd omette l'area di riproduzione dai dispositivi audio e della forma d'onda, i sequencer MIDI e altri dispositivi che non scrivono sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="825a2-114">MCIWnd omits the playback area from waveform-audio devices, MIDI sequencers, and other devices that do not write to the display.</span></span> <span data-ttu-id="825a2-115">Nell'illustrazione seguente viene mostrata l'area di riproduzione dell'audio e della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="825a2-115">The following illustration shows the waveform-audio playback area.</span></span>

![immagine della finestra MCIWnd](images/mciwnd4.gif)

<span data-ttu-id="825a2-117">Il pulsante **Play** si trova nell'angolo inferiore sinistro della finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="825a2-117">The **Play** button is located in the lower-left corner of the MCIWnd window.</span></span> <span data-ttu-id="825a2-118">Viene visualizzato quando il contenuto viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="825a2-118">It appears when the content is stopped.</span></span> <span data-ttu-id="825a2-119">L'utente può riprodurre il contenuto nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="825a2-119">The user can play the content in the following ways:</span></span>

-   <span data-ttu-id="825a2-120">Per riprodurre il contenuto dalla posizione di riproduzione corrente, selezionare il pulsante **Riproduci** .</span><span class="sxs-lookup"><span data-stu-id="825a2-120">To play the content from the current playback position, select the **Play** button.</span></span>
-   <span data-ttu-id="825a2-121">Per riprodurre il contenuto a schermo intero dalla posizione di riproduzione corrente, selezionare il pulsante **Play** tenendo premuto il tasto CTRL.</span><span class="sxs-lookup"><span data-stu-id="825a2-121">To play the content full-screen from the current playback position, select the **Play** button while holding down the CTRL key.</span></span>
-   <span data-ttu-id="825a2-122">Per riprodurre il contenuto indietro rispetto alla posizione di riproduzione corrente, selezionare il pulsante **Riproduci** tenendo premuto il tasto MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="825a2-122">To play the content backward from the current playback position, select the **Play** button while holding down the SHIFT key.</span></span>

<span data-ttu-id="825a2-123">Il pulsante di **menu** , situato accanto al pulsante **Riproduci** , attiva un menu che consente all'utente di aprire e chiudere i file audio-video con interfoliazione (AVI) e di regolare le dimensioni dell'immagine, la velocità di riproduzione e il volume.</span><span class="sxs-lookup"><span data-stu-id="825a2-123">The **Menu** button, located next to the **Play** button, activates a menu that allows the user to open and close audio-video interleaved (AVI) files, and to adjust the image size, playback speed, and volume.</span></span> <span data-ttu-id="825a2-124">L'utente può anche attivare il menu facendo clic con il pulsante destro del mouse quando il cursore si trova nell'area client della finestra. Il menu include anche i comandi per modificare la configurazione del dispositivo corrente, per copiare il contenuto della riproduzione negli Appunti e per emettere i comandi MCI.</span><span class="sxs-lookup"><span data-stu-id="825a2-124">(The user can also activate the menu by clicking the right mouse button whenever the cursor is in the client area of the window.) The menu also includes commands to change the configuration of the current device, to copy the playback content to the clipboard, and to issue MCI commands.</span></span>

<span data-ttu-id="825a2-125">Il TrackBar a destra del pulsante di **menu** rappresenta la durata del contenuto di riproduzione (o registrato).</span><span class="sxs-lookup"><span data-stu-id="825a2-125">The trackbar to the right of the **Menu** button represents the duration of the playback (or recorded) content.</span></span> <span data-ttu-id="825a2-126">Il dispositivo di scorrimento nel TrackBar rappresenta la posizione di riproduzione corrente all'interno del contenuto.</span><span class="sxs-lookup"><span data-stu-id="825a2-126">The slider on the trackbar represents the current playback position within the content.</span></span> <span data-ttu-id="825a2-127">Quando il dispositivo di scorrimento è posizionato all'estremità sinistra del TrackBar, la posizione di riproduzione corrente è l'inizio del contenuto.</span><span class="sxs-lookup"><span data-stu-id="825a2-127">When the slider is positioned at the left end of the trackbar, the current playback position is the beginning of the content.</span></span> <span data-ttu-id="825a2-128">L'utente può spostarsi in posizioni diverse nel contenuto trascinando il dispositivo di scorrimento lungo il TrackBar.</span><span class="sxs-lookup"><span data-stu-id="825a2-128">The user can move to different locations in the content by dragging the slider along the trackbar.</span></span> <span data-ttu-id="825a2-129">Il pulsante **Arresta** si trova nell'angolo inferiore sinistro della finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="825a2-129">The **Stop** button is located in the lower-left corner of the MCIWnd window.</span></span> <span data-ttu-id="825a2-130">Viene visualizzato quando viene riprodotto il contenuto.</span><span class="sxs-lookup"><span data-stu-id="825a2-130">It appears when the content is played.</span></span> <span data-ttu-id="825a2-131">La figura seguente mostra la riproduzione video in corso.</span><span class="sxs-lookup"><span data-stu-id="825a2-131">The following illustration shows video playback in progress.</span></span>

![immagine di riproduzione video](images/mciwnd2.gif)

<span data-ttu-id="825a2-133">I controlli MCIWnd possono includere anche un pulsante di **registrazione** per i dispositivi che possono registrare.</span><span class="sxs-lookup"><span data-stu-id="825a2-133">The MCIWnd controls can also include a **Record** button for devices that can record.</span></span> <span data-ttu-id="825a2-134">Il pulsante **record** è contrassegnato da un cerchio rosso e viene visualizzato solo quando il dispositivo è in grado di registrare.</span><span class="sxs-lookup"><span data-stu-id="825a2-134">The **Record** button is marked with a red circle and appears only when the device is capable of recording.</span></span>

> [!Note]  
> <span data-ttu-id="825a2-135">La finestra di riproduzione deve essere allineata su un limite di quattro pixel per ottenere prestazioni migliori per la riproduzione video.</span><span class="sxs-lookup"><span data-stu-id="825a2-135">The playback window must be aligned on a four-pixel boundary for the best video playback performance.</span></span> <span data-ttu-id="825a2-136">In genere, Windows allinea automaticamente la finestra al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="825a2-136">Typically, Windows aligns the window automatically when it is created.</span></span> <span data-ttu-id="825a2-137">Se un utente sposta o estende la finestra dalla posizione iniziale, la velocità di riproduzione del video potrebbe essere ridotta di metà.</span><span class="sxs-lookup"><span data-stu-id="825a2-137">If a user moves or stretches the window from its initial position, video playback speed might be reduced by half.</span></span>

 

 

 




