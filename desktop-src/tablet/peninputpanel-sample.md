---
description: Questo esempio si basa sull'esempio di modulo delle attestazioni automatiche integrando l'oggetto PenInputPanel. L'esempio si trova nella \# directory C PIPanel nella cartella Autoclaims.
ms.assetid: 9a2c1565-fb24-4767-bfa5-0257129f4bd4
title: Esempio di PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d60f33ff3f61e1a2930841e5fd3d3ce3f9fc5b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317916"
---
# <a name="peninputpanel-sample"></a><span data-ttu-id="071f1-104">Esempio di PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="071f1-104">PenInputPanel Sample</span></span>

<span data-ttu-id="071f1-105">Questo esempio si basa sull'esempio di modulo delle attestazioni automatiche integrando l'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="071f1-105">This sample builds on the Auto Claims Form sample by integrating the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object.</span></span> <span data-ttu-id="071f1-106">L'esempio si trova nella \# directory C PIPanel nella cartella Autoclaims.</span><span class="sxs-lookup"><span data-stu-id="071f1-106">The sample is in the C\# PIPanel directory in the AutoClaims folder.</span></span>

> [!Note]  
> <span data-ttu-id="071f1-107">Per questo esempio è necessario che il sistema sia dotato di un dispositivo Pen.</span><span class="sxs-lookup"><span data-stu-id="071f1-107">This sample requires that your system is equipped with a pen device.</span></span> <span data-ttu-id="071f1-108">Se si usa solo un mouse (o un altro dispositivo di puntamento HID), l'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) non viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="071f1-108">If you are using just a mouse (or other non-human interface device (HID) pointing device) the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) does not appear.</span></span>

 

<span data-ttu-id="071f1-109">Per ulteriori informazioni sull'esempio relativo al modulo Auto Claims, vedere l'esempio relativo al [modulo Claims automatico](auto-claims-form-sample.md).</span><span class="sxs-lookup"><span data-stu-id="071f1-109">For more information about the Auto Claims Form sample, see [Auto Claims Form Sample](auto-claims-form-sample.md).</span></span> <span data-ttu-id="071f1-110">Per ulteriori informazioni sull'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) , vedere [Programming the input panel using the PenInputPanel class](programming-the-input-panel-using-the-peninputpanel-class.md).</span><span class="sxs-lookup"><span data-stu-id="071f1-110">For more information about the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object, see [Programming the Input Panel Using the PenInputPanel Class](programming-the-input-panel-using-the-peninputpanel-class.md).</span></span>

<span data-ttu-id="071f1-111">Nell'esempio, il form auto Claims contiene cinque campi in cui all'utente viene richiesto di inserire le informazioni relative all'attestazione: numero di criteri, nome assicurato, anno, marca e modello dell'automobile.</span><span class="sxs-lookup"><span data-stu-id="071f1-111">In the sample, the Auto Claims Form contains five fields into which the user is asked to put information relevant to the claim: policy number, insured name, the year, make, and model of the car.</span></span> <span data-ttu-id="071f1-112">Un oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) è associato a ogni campo di input per fornire un metodo semplice per l'immissione di valori con una penna.</span><span class="sxs-lookup"><span data-stu-id="071f1-112">A [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object is attached to each input field to provide an easy means for entering values with a pen.</span></span>

<span data-ttu-id="071f1-113">Esistono due tecniche per il fissaggio di un oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) ai campi di input nel form.</span><span class="sxs-lookup"><span data-stu-id="071f1-113">There are two techniques for attaching a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to the input fields on your form.</span></span> <span data-ttu-id="071f1-114">La prima tecnica consiste nell'assegnare un'istanza separata dell'oggetto a ogni campo di input in fase di progettazione.</span><span class="sxs-lookup"><span data-stu-id="071f1-114">The first technique is to assign a separate instance of the object to each input field at design time.</span></span> <span data-ttu-id="071f1-115">Il secondo consiste nel creare una singola istanza dell'oggetto e quindi collegarla in fase di esecuzione a un campo quando riceve lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="071f1-115">The second is to create a single instance of the object and then attach that object instance at run time to a field when it receives focus.</span></span> <span data-ttu-id="071f1-116">In questo esempio vengono illustrate entrambe le tecniche.</span><span class="sxs-lookup"><span data-stu-id="071f1-116">This sample demonstrates both techniques.</span></span>

<span data-ttu-id="071f1-117">La scelta della tecnica da utilizzare comporta compromessi.</span><span class="sxs-lookup"><span data-stu-id="071f1-117">There are tradeoffs involved in deciding which technique to use.</span></span> <span data-ttu-id="071f1-118">La creazione di un'istanza univoca dell'oggetto per ogni campo del modulo richiede una quantità di memoria leggermente maggiore quando il modulo viene caricato.</span><span class="sxs-lookup"><span data-stu-id="071f1-118">Creating a unique instance of the object for each form field requires slightly more memory when the form is loaded.</span></span> <span data-ttu-id="071f1-119">Tuttavia, salva la necessità di gestire gli eventi di attivazione per i campi per assegnare una singola istanza al campo corrente in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="071f1-119">However, it saves having to handle focus events for the fields to assign a single instance to the current field at run time.</span></span>

<span data-ttu-id="071f1-120">Poiché l'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) è supportato solo in un Tablet PC, l'esempio crea gli oggetti PenInputPanel all'interno di un blocco di gestione delle eccezioni.</span><span class="sxs-lookup"><span data-stu-id="071f1-120">Because the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object is supported only on a Tablet PC, the sample creates the PenInputPanel objects within an exception-handling block.</span></span>

## <a name="one-object-per-field"></a><span data-ttu-id="071f1-121">Un oggetto per ogni campo</span><span class="sxs-lookup"><span data-stu-id="071f1-121">One Object per Field</span></span>

<span data-ttu-id="071f1-122">Nell'esempio viene illustrata la prima tecnica (un oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) per ogni campo) assegnando i campi di input per il numero di criteri ( `inkEdPolicyNumber` ) e il nome assicurato ( `inkEdName` ) un'istanza univoca dell'oggetto PenInputPanel.</span><span class="sxs-lookup"><span data-stu-id="071f1-122">The sample demonstrates the first technique (one [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object per field) by assigning the input fields for policy number (`inkEdPolicyNumber`) and insured name (`inkEdName`) a unique instance of the PenInputPanel object.</span></span> <span data-ttu-id="071f1-123">Un costruttore di overload per l'oggetto PenInputPanel può assumere il nome del controllo di input come argomento, associando così i controlli.</span><span class="sxs-lookup"><span data-stu-id="071f1-123">An overloaded constructor for the PenInputPanel object can take the name of the input control as an argument, thus associating the controls.</span></span> <span data-ttu-id="071f1-124">Le righe seguenti del gestore dell'evento [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del form mostrano quanto segue:</span><span class="sxs-lookup"><span data-stu-id="071f1-124">The following lines from the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler shows this:</span></span>


```C++
pipPolicyNumber = new PenInputPanel(inkEdPolicyNumber);
pipName = new PenInputPanel(inkEdName);
```



## <a name="one-object-per-form"></a><span data-ttu-id="071f1-125">Un oggetto per ogni form</span><span class="sxs-lookup"><span data-stu-id="071f1-125">One Object per Form</span></span>

<span data-ttu-id="071f1-126">La seconda tecnica è illustrata nell'esempio: una singola istanza di un oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) , `pipShared` , viene condivisa tra i campi anno, marca e input modello.</span><span class="sxs-lookup"><span data-stu-id="071f1-126">The second technique is also shown in the sample: a single instance of a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object, `pipShared`, is shared between the Year, Make, and Model input fields.</span></span> <span data-ttu-id="071f1-127">L'oggetto condiviso viene creato utilizzando il costruttore predefinito.</span><span class="sxs-lookup"><span data-stu-id="071f1-127">The shared object is created by using the default constructor.</span></span>


```C++
pipShared = new PenInputPanel();
```



<span data-ttu-id="071f1-128">Per usare questa tecnica è necessario che il form disponga di una sola istanza dell'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="071f1-128">Using this technique requires that your form have only a single instance of the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object.</span></span> <span data-ttu-id="071f1-129">Questa operazione consente di risparmiare memoria, ma è necessario aggiungere il codice per gestire l'evento quando un campo di input riceve lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="071f1-129">This saves memory, but you must add code to handle the event when an input field receives focus.</span></span> <span data-ttu-id="071f1-130">Quando un controllo che usa un'istanza condivisa di un oggetto PenInputPanel ottiene lo stato attivo, impostare la proprietà [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) dell'oggetto PenInputPanel su tale controllo.</span><span class="sxs-lookup"><span data-stu-id="071f1-130">When a control that uses a shared instance of a PenInputPanel object gets focus, set the PenInputPanel object's [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) property to that control.</span></span> <span data-ttu-id="071f1-131">Il codice seguente illustra un gestore eventi per gli eventi year, make e Model Fields `Enter` .</span><span class="sxs-lookup"><span data-stu-id="071f1-131">The following code shows an event handler for the Year, Make, and Model fields' `Enter` events.</span></span>


```C++
private void inkEdYear_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Year field
    pipShared.AttachedEditControl = inkEdYear;

    // set the NUMBER factoid to bias recognition for numbers
    pipShared.Factoid = "NUMBER";

    // Enable correction UI on the inkEdYear field
    pipShared.EnableTsf(true);
}

private void inkEdMake_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Make field
    pipShared.AttachedEditControl = inkEdMake;

    // reset the factoid to bias recognition for general text
    pipShared.Factoid = "DEFAULT";

    // Enable correction UI on the inkEdMake field
    pipShared.EnableTsf(true);
}
private void inkEdModel_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Model field
    pipShared.AttachedEditControl = inkEdModel;

    // reset the factoid to bias recognition for general text
    pipShared.Factoid = "DEFAULT";

    // Enable correction UI on the inkEdModel field
    pipShared.EnableTsf(true);
}
```



<span data-ttu-id="071f1-132">Assicurarsi di impostare le proprietà che devono essere impostate quando lo stato attivo viene modificato in un nuovo controllo.</span><span class="sxs-lookup"><span data-stu-id="071f1-132">Be sure to set any properties that need to be set when focus changes to a new control.</span></span> <span data-ttu-id="071f1-133">Nei gestori eventi precedenti, ad esempio, la proprietà del controllo del controllo è impostata in [base alle esigenze](/previous-versions/ms571978(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="071f1-133">In the previous event handlers, for example, the [Factoid](/previous-versions/ms571978(v=vs.100)) property is set as appropriate.</span></span>

## <a name="usability-considerations"></a><span data-ttu-id="071f1-134">Considerazioni sull'usabilità</span><span class="sxs-lookup"><span data-stu-id="071f1-134">Usability Considerations</span></span>

<span data-ttu-id="071f1-135">Quando si usa l'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) nell'applicazione, tenere presenti le seguenti considerazioni sull'usabilità.</span><span class="sxs-lookup"><span data-stu-id="071f1-135">Keep the following usability considerations in mind when using the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object in your application.</span></span>

### <a name="positioning-the-peninputpanel"></a><span data-ttu-id="071f1-136">Posizionamento di PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="071f1-136">Positioning the PenInputPanel</span></span>

<span data-ttu-id="071f1-137">Poiché i campi sono disposti verticalmente sul form in questo esempio, l'interfaccia utente [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) per ogni controllo di input è leggermente posizionata a destra del controllo di input per facilitarne l'uso.</span><span class="sxs-lookup"><span data-stu-id="071f1-137">Because the fields are laid out vertically on the form in this sample, the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) user interface for each input control is positioned slightly to the right of the input control to make it easier to use.</span></span> <span data-ttu-id="071f1-138">In questo modo si impedisce a PenInputPanel di coprire la successiva casella di modifica, rendendo più semplice la destinazione della successiva casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="071f1-138">This prevents the PenInputPanel from covering up the next edit box, making it easier to target the next edit box.</span></span>


```C++
pipShared.HorizontalOffset = 32;
pipPolicyNumber.HorizontalOffset = 32;
pipName.HorizontalOffset = 32;
```



### <a name="selecting-input-panel-to-display"></a><span data-ttu-id="071f1-139">Selezione del pannello di input da visualizzare</span><span class="sxs-lookup"><span data-stu-id="071f1-139">Selecting Input Panel to Display</span></span>

<span data-ttu-id="071f1-140">Poiché i numeri di criteri sono spesso combinazioni di numeri, lettere e altri caratteri, possono essere soggetti a errori di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="071f1-140">Because policy numbers are often combinations of numbers, letters, and other characters, they can be prone to recognition errors.</span></span> <span data-ttu-id="071f1-141">Pertanto, l'esempio imposta il pannello predefinito visualizzato dall'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) come tastiera quando viene collegato al campo numero di criteri.</span><span class="sxs-lookup"><span data-stu-id="071f1-141">Therefore, the sample sets the default panel displayed by the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to be the keyboard when it is attached to the policy number field.</span></span>


```C++
pipPolicyNumber.DefaultPanel = PanelType.Keyboard;
```



<span data-ttu-id="071f1-142">Il comportamento predefinito dell'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) consiste nell'usare il pannello selezionato per ultimo dall'utente.</span><span class="sxs-lookup"><span data-stu-id="071f1-142">The default behavior of the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object is to use the panel the user selected last.</span></span>

### <a name="text-services-framework-correction-user-interface"></a><span data-ttu-id="071f1-143">Interfaccia utente di correzione del Framework di servizi di testo</span><span class="sxs-lookup"><span data-stu-id="071f1-143">Text Services Framework Correction User Interface</span></span>

<span data-ttu-id="071f1-144">In questo esempio tutti i campi di input sono controlli [InkEdit](/previous-versions/ms552265(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="071f1-144">In this sample all of the input fields are [InkEdit](/previous-versions/ms552265(v=vs.100)) controls.</span></span> <span data-ttu-id="071f1-145">Questa operazione è significativa perché il controllo InkEdit dispone del supporto incorporato per il [Framework di servizi di testo](../tsf/text-services-framework.md) (TSF) ed è quindi in grado di supportare l'interfaccia utente di correzione sul posto per l'input ricevuto dall'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="071f1-145">This is significant because the InkEdit control has built-in support for the [Text Services Framework](../tsf/text-services-framework.md) (TSF) and is thus capable of supporting the in-place correction user interface for input received from the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object.</span></span>

<span data-ttu-id="071f1-146">Il valore predefinito per [EnableTsf](/previous-versions/ms569656(v=vs.100)) è **true**.</span><span class="sxs-lookup"><span data-stu-id="071f1-146">The default value for [EnableTsf](/previous-versions/ms569656(v=vs.100)) is **TRUE**.</span></span> <span data-ttu-id="071f1-147">In questo modo, l'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) tenta di avviare il Framework dei servizi di testo (TSF) sul controllo associato.</span><span class="sxs-lookup"><span data-stu-id="071f1-147">This causes the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to attempt to start the Text Services Framework (TSF) on the attached control.</span></span> <span data-ttu-id="071f1-148">In caso di esito positivo, l'interfaccia utente di correzione viene visualizzata nel controllo e consente l'accesso alle alternative di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="071f1-148">If successful, the correction user interface shows in the control, and it allows access to recognition alternates.</span></span> <span data-ttu-id="071f1-149">La chiamata di questo metodo con un parametro **false** tenta di arrestare TSF sul controllo associato.</span><span class="sxs-lookup"><span data-stu-id="071f1-149">Calling this method with a **FALSE** parameter attempts to shut down TSF on the attached control.</span></span>

<span data-ttu-id="071f1-150">Il controllo [InkEdit](/previous-versions/ms552265(v=vs.100)) fornisce già un'interfaccia utente di correzione, ma nell'esempio [EnableTsf](/previous-versions/ms569656(v=vs.100)) viene usato per consentire a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) di usare il contesto del riconoscimento di inserimento di TSF anziché la funzione [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) per inviare i risultati del riconoscimento della grafia nel controllo.</span><span class="sxs-lookup"><span data-stu-id="071f1-150">The [InkEdit](/previous-versions/ms552265(v=vs.100)) control already provides a correction user interface, but in the sample [EnableTsf](/previous-versions/ms569656(v=vs.100)) is used to enable the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) to use the TSF insertion recognizer context rather than the [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) function to send the handwriting recognition results into the control.</span></span> <span data-ttu-id="071f1-151">Il risultato è che il testo può essere inserito anche se il campo non ha più lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="071f1-151">The result is that text can be inserted even if the field no longer has focus.</span></span>


```C++
  pipName.EnableTsf(true);
  pipPolicyNumber.EnableTsf(true);
```



## <a name="closing-the-form"></a><span data-ttu-id="071f1-152">Chiusura del modulo</span><span class="sxs-lookup"><span data-stu-id="071f1-152">Closing the Form</span></span>

<span data-ttu-id="071f1-153">Nel codice generato da Progettazione Windows Form, i controlli [InkEdit](/previous-versions/ms552265(v=vs.100)) e [InkPicture](/previous-versions/aa514604(v=msdn.10)) vengono aggiunti all'elenco dei componenti del form quando il modulo viene inizializzato.</span><span class="sxs-lookup"><span data-stu-id="071f1-153">In the Windows Form Designer generated code, the [InkEdit](/previous-versions/ms552265(v=vs.100)) and [InkPicture](/previous-versions/aa514604(v=msdn.10)) controls are added to the form's component list when the form is initialized.</span></span> <span data-ttu-id="071f1-154">Quando il form viene chiuso, i controlli InkEdit e InkPicture vengono eliminati, così come gli altri componenti del form, dal metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del modulo.</span><span class="sxs-lookup"><span data-stu-id="071f1-154">When the form closes, the InkEdit and InkPicture controls are disposed, as well as the other components of the form, by the form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method.</span></span> <span data-ttu-id="071f1-155">Il metodo Dispose del modulo Elimina inoltre gli oggetti [Ink](/previous-versions/aa515768(v=msdn.10)) creati per il form.</span><span class="sxs-lookup"><span data-stu-id="071f1-155">The form's Dispose method also disposes the [Ink](/previous-versions/aa515768(v=msdn.10)) objects that are created for the form.</span></span>

 

 
