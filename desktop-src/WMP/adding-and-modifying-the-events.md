---
title: Aggiunta e modifica degli eventi
description: Aggiunta e modifica degli eventi
ms.assetid: 342b0592-67b7-4c13-bee8-48ac322d3d27
keywords:
- Plug-in di Windows Media Player, pagine delle proprietà di esempio Echo
- plug-in, pagine delle proprietà di esempio Echo
- plug-in di elaborazione dei segnali digitali, pagine delle proprietà di esempio Echo
- Plug-in DSP, pagine delle proprietà di esempio Echo
- Esempio di plug-in Echo DSP, pagine delle proprietà
- Esempio di plug-in Echo DSP, eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c8e069c20dc2c953998b9e5c2a47f509166ca3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331132"
---
# <a name="adding-and-modifying-the-events"></a><span data-ttu-id="eccc8-109">Aggiunta e modifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="eccc8-109">Adding and Modifying the Events</span></span>

<span data-ttu-id="eccc8-110">È necessario fornire gestori eventi per gli \_ eventi di modifica it che si verificano quando l'utente modifica il testo nelle caselle di modifica della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="eccc8-110">You need to supply event handlers for the EN\_CHANGE events that occur when the user changes the text in the property page edit boxes.</span></span> <span data-ttu-id="eccc8-111">Questi gestori di eventi hanno un'implementazione semplice che consente di **applicare** solo la finestra di dialogo della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="eccc8-111">These event handlers have a simple implementation that merely enables **Apply** in the property page dialog box.</span></span>

## <a name="modifying-the-scale-factor-event-handler"></a><span data-ttu-id="eccc8-112">Modifica del gestore eventi del fattore di scala</span><span class="sxs-lookup"><span data-stu-id="eccc8-112">Modifying the Scale Factor Event Handler</span></span>

<span data-ttu-id="eccc8-113">È necessario modificare il nome del gestore eventi esistente fornito dalla procedura guidata plug-in per la casella di modifica fattore di scala.</span><span class="sxs-lookup"><span data-stu-id="eccc8-113">You need to change the name of the existing event handler that the plug-in wizard provided for the scale factor edit box.</span></span> <span data-ttu-id="eccc8-114">È necessario modificare il nome da OnChangeScale a OnChangeDelay in tre posizioni:</span><span class="sxs-lookup"><span data-stu-id="eccc8-114">You should change the name from OnChangeScale to OnChangeDelay in three locations:</span></span>

1.  <span data-ttu-id="eccc8-115">In EchoPropPage. h, modificare il nome nella sezione della macro della mappa messaggi.</span><span class="sxs-lookup"><span data-stu-id="eccc8-115">In EchoPropPage.h, change the name in the message map macro section.</span></span> <span data-ttu-id="eccc8-116">Sostituire la riga che esegue il mapping dell'evento di modifica del fattore di scala al metodo OnChangeScale con il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="eccc8-116">Replace the line that maps the scale factor change event to the OnChangeScale method with the following code:</span></span>
    ```C++
    COMMAND_HANDLER(IDC_DELAYTIME, EN_CHANGE, OnChangeDelay)
    
    ```

    

2.  <span data-ttu-id="eccc8-117">In EchoPropPage. h modificare il nome nella riga che prototipa la funzione OnChangeScale:</span><span class="sxs-lookup"><span data-stu-id="eccc8-117">In EchoPropPage.h, change the name in the line that prototypes the OnChangeScale function:</span></span>
    ```C++
    LRESULT (OnChangeDelay)(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled);
    
    ```

    

3.  <span data-ttu-id="eccc8-118">In EchoPropPage. cpp modificare il nome nell'intestazione della funzione:</span><span class="sxs-lookup"><span data-stu-id="eccc8-118">In EchoPropPage.cpp, change the name in the function header:</span></span>
    ```C++
    LRESULT CEchoPropPage::OnChangeDelay(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled)
    
    ```

    

## <a name="adding-the-wet-mix-event-handler"></a><span data-ttu-id="eccc8-119">Aggiunta del gestore dell'evento Wet Mix</span><span class="sxs-lookup"><span data-stu-id="eccc8-119">Adding the Wet Mix Event Handler</span></span>

<span data-ttu-id="eccc8-120">È possibile aggiungere facilmente il gestore eventi per l' \_ evento di modifica en associato al \_ controllo della casella di modifica IDC WETMIX.</span><span class="sxs-lookup"><span data-stu-id="eccc8-120">You can easily add the event handler for the EN\_CHANGE event that is attached to the IDC\_WETMIX edit box control.</span></span> <span data-ttu-id="eccc8-121">Dall'editor di risorse della finestra di dialogo:</span><span class="sxs-lookup"><span data-stu-id="eccc8-121">From the dialog resource editor:</span></span>

1.  <span data-ttu-id="eccc8-122">Fare clic con il pulsante destro del mouse sulla \_ casella di modifica IDC WETMIX e scegliere **eventi**.</span><span class="sxs-lookup"><span data-stu-id="eccc8-122">Right-click the IDC\_WETMIX edit box and choose **Events**.</span></span> <span data-ttu-id="eccc8-123">Verrà visualizzata la finestra di dialogo nuovo messaggio e gestori eventi di Windows.</span><span class="sxs-lookup"><span data-stu-id="eccc8-123">The New Windows Message and Event Handlers dialog box appears.</span></span>
2.  <span data-ttu-id="eccc8-124">Nella casella **classe o oggetto da gestire** , fare clic sul nome della risorsa casella di modifica, IDC \_ WETMIX.</span><span class="sxs-lookup"><span data-stu-id="eccc8-124">In the **Class or object to handle** box, click the name of the edit box resource, IDC\_WETMIX.</span></span>
3.  <span data-ttu-id="eccc8-125">Nella casella **New Windows Messages/Events** fare clic su en \_ Change per selezionarlo.</span><span class="sxs-lookup"><span data-stu-id="eccc8-125">In the **New Windows messages/events** box, click EN\_CHANGE to select it.</span></span>
4.  <span data-ttu-id="eccc8-126">Fare clic su **Aggiungi gestore**.</span><span class="sxs-lookup"><span data-stu-id="eccc8-126">Click **Add Handler**.</span></span> <span data-ttu-id="eccc8-127">Verrà visualizzata la finestra di dialogo Aggiungi funzione membro.</span><span class="sxs-lookup"><span data-stu-id="eccc8-127">The Add Member Function dialog box appears.</span></span>
5.  <span data-ttu-id="eccc8-128">Nella casella **nome funzione membro** Digitare il nome OnChangeWetmix.</span><span class="sxs-lookup"><span data-stu-id="eccc8-128">In the **Member function name** box, type the name OnChangeWetmix.</span></span>
6.  <span data-ttu-id="eccc8-129">Fare clic su **OK** per chiudere la finestra di dialogo Aggiungi funzione membro.</span><span class="sxs-lookup"><span data-stu-id="eccc8-129">Click **OK** to close the Add Member Function dialog box.</span></span>
7.  <span data-ttu-id="eccc8-130">Fare clic su **OK** per tornare all'editor risorse della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="eccc8-130">Click **OK** to return to the dialog box resource editor.</span></span>

<span data-ttu-id="eccc8-131">Visual C++ aggiunge automaticamente il codice per la mappa messaggi e la funzione del gestore eventi a EchoPropPage. h.</span><span class="sxs-lookup"><span data-stu-id="eccc8-131">Visual C++ automatically adds the code for the message map and for the event handler function to EchoPropPage.h.</span></span> <span data-ttu-id="eccc8-132">Il codice inserito fornisce un commento TODO in cui è possibile aggiungere l'implementazione nell'intestazione per la funzione.</span><span class="sxs-lookup"><span data-stu-id="eccc8-132">The code it inserts provides a TODO comment where you can add the implementation in the header for the function.</span></span> <span data-ttu-id="eccc8-133">Si tratta di uno stile leggermente diverso rispetto a quello usato dal codice di esempio della procedura guidata per il plug-in di Windows Media Player, ma è accettabile.</span><span class="sxs-lookup"><span data-stu-id="eccc8-133">This is a slightly different style than the Windows Media Player Plug-in Wizard sample code uses, but is acceptable.</span></span>

<span data-ttu-id="eccc8-134">Se si desidera scrivere l'implementazione nel file di intestazione o spostarla in EchoPropPage. cpp, è possibile.</span><span class="sxs-lookup"><span data-stu-id="eccc8-134">Whether you want to write your implementation in the header file or move it to EchoPropPage.cpp is up to you.</span></span> <span data-ttu-id="eccc8-135">In entrambi i casi, l'implementazione richiede solo una singola riga di codice aggiuntiva per abilitare **applica** nella finestra di dialogo della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="eccc8-135">In either case, the implementation needs only a single additional line of code to enable **Apply** in the property page dialog.</span></span> <span data-ttu-id="eccc8-136">Inserire questa riga di codice prima della riga restituita dalla funzione:</span><span class="sxs-lookup"><span data-stu-id="eccc8-136">Insert this line of code before the line that returns from the function:</span></span>


```C++
SetDirty(TRUE);  // Enable Apply.

```



## <a name="related-topics"></a><span data-ttu-id="eccc8-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eccc8-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eccc8-138">**Modifica della pagina delle proprietà di esempio Echo**</span><span class="sxs-lookup"><span data-stu-id="eccc8-138">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




