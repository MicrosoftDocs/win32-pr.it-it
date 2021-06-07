---
title: Risoluzione dei problemi relativi alle applicazioni
description: In questa sezione vengono fornite soluzioni ai problemi comuni.
ms.assetid: dfdc5a97-aa0a-4011-8f61-6e405e28b6f8
keywords:
- Windows Touch,risoluzione dei problemi delle applicazioni
- Windows Touch, rifiuto di palmo
- palm rejection
- Windows Touch, supporto legacy
- risoluzione dei problemi Windows Touch
- inerzia, risoluzione dei problemi delle applicazioni
- manipolazioni, risoluzione dei problemi delle applicazioni
- movimenti, risoluzione dei problemi delle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 389d200cedc57b7f128a535355b12a9288c6e9eb
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443148"
---
# <a name="troubleshooting-applications"></a><span data-ttu-id="82962-111">Risoluzione dei problemi relativi alle applicazioni</span><span class="sxs-lookup"><span data-stu-id="82962-111">Troubleshooting Applications</span></span>

<span data-ttu-id="82962-112">In questa sezione vengono fornite soluzioni ai problemi comuni.</span><span class="sxs-lookup"><span data-stu-id="82962-112">This section gives solutions to common problems.</span></span>

## <a name="general-troubleshooting"></a><span data-ttu-id="82962-113">Risoluzione di problemi generali</span><span class="sxs-lookup"><span data-stu-id="82962-113">General Troubleshooting</span></span>



| <span data-ttu-id="82962-114">Categoria</span><span class="sxs-lookup"><span data-stu-id="82962-114">Category</span></span> | <span data-ttu-id="82962-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82962-115">Description</span></span> |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82962-116">Problema</span><span class="sxs-lookup"><span data-stu-id="82962-116">Issue</span></span>    | <span data-ttu-id="82962-117">Si esegue Windows Server 2008 e Windows Touch funzionalità non funzionano.</span><span class="sxs-lookup"><span data-stu-id="82962-117">I am running Windows Server 2008 and Windows Touch features are not working.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="82962-118">Causa</span><span class="sxs-lookup"><span data-stu-id="82962-118">Cause</span></span>    | <span data-ttu-id="82962-119">Esperienza desktop non è stata abilitata.</span><span class="sxs-lookup"><span data-stu-id="82962-119">You haven't enabled the Desktop Experience.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="82962-120">Soluzione</span><span class="sxs-lookup"><span data-stu-id="82962-120">Solution</span></span> | <span data-ttu-id="82962-121">Aprire lo strumento Server Manager amministrativo: fare clic su **Start**, scegliere **Strumenti di** amministrazione , quindi fare clic **su Server Manager**.</span><span class="sxs-lookup"><span data-stu-id="82962-121">Open the Server Manager administrative tool: click **Start**, point to **Administrative Tools**, and then click **Server Manager**.</span></span> <span data-ttu-id="82962-122">Fare clic **sull'elemento** Funzionalità nella colonna a sinistra.</span><span class="sxs-lookup"><span data-stu-id="82962-122">Click the **Features** item in the left column.</span></span> <span data-ttu-id="82962-123">Fare **clic su Aggiungi** funzionalità nella **sezione** Funzionalità.</span><span class="sxs-lookup"><span data-stu-id="82962-123">Click **Add Features** in the **Features** section.</span></span> <span data-ttu-id="82962-124">Selezionare **Esperienza desktop,** fare clic **su Avanti** e quindi su **Installa.**</span><span class="sxs-lookup"><span data-stu-id="82962-124">Select **Desktop Experience**, click **Next**, and then click **Install**.</span></span> |



 



| <span data-ttu-id="82962-125">Categoria</span><span class="sxs-lookup"><span data-stu-id="82962-125">Category</span></span> | <span data-ttu-id="82962-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82962-126">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82962-127">Problema</span><span class="sxs-lookup"><span data-stu-id="82962-127">Issue</span></span>    | <span data-ttu-id="82962-128">Ogni volta che si sposta rapidamente il dito nell'applicazione, viene visualizzata una freccia e il movimento o la manipolazione non viene registrato correttamente.</span><span class="sxs-lookup"><span data-stu-id="82962-128">Whenever I move my finger quickly across my application, an arrow appears and my gesture or manipulation is not registering correctly.</span></span>                                                             |
| <span data-ttu-id="82962-129">Causa</span><span class="sxs-lookup"><span data-stu-id="82962-129">Cause</span></span>    | <span data-ttu-id="82962-130">Quando non è necessario, sono abilitati i gesti rapidi.</span><span class="sxs-lookup"><span data-stu-id="82962-130">Having flicks enabled when you don't need it.</span></span>                                                                                                                                                      |
| <span data-ttu-id="82962-131">Soluzione</span><span class="sxs-lookup"><span data-stu-id="82962-131">Solution</span></span> | <span data-ttu-id="82962-132">I gesti rapidi sono abilitati quando si vuole che sia disabilitato.</span><span class="sxs-lookup"><span data-stu-id="82962-132">You have flicks enabled when you want it to be disabled.</span></span> <span data-ttu-id="82962-133">Per [informazioni sulla disabilitazione dei gesti rapidi](legacy-support-for-panning-with-scrollbars.md) della penna, vedere Supporto legacy per la panoramica con le barre di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="82962-133">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling pen flicks.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="82962-134">Problema</span><span class="sxs-lookup"><span data-stu-id="82962-134">Issue</span></span></td>
<td><span data-ttu-id="82962-135">Non è possibile distinguere tra input del mouse e input Windows Touch mouse.</span><span class="sxs-lookup"><span data-stu-id="82962-135">I can't discern between mouse input and Windows Touch input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82962-136">Causa</span><span class="sxs-lookup"><span data-stu-id="82962-136">Cause</span></span></td>
<td><span data-ttu-id="82962-137">Windows genera messaggi del mouse per il supporto legacy quando un utente fa clic sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="82962-137">Windows generates mouse messages for legacy support when a user clicks on the screen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82962-138">Soluzione</span><span class="sxs-lookup"><span data-stu-id="82962-138">Solution</span></span></td>
<td><span data-ttu-id="82962-139">È possibile chiamare <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> per i messaggi <strong>WM_LBUTTONDOWN</strong> e <strong>WM_LBUTTONUP</strong> per determinare l'origine.</span><span class="sxs-lookup"><span data-stu-id="82962-139">You can call <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> for the <strong>WM_LBUTTONDOWN</strong> and <strong>WM_LBUTTONUP</strong> messages to determine the source.</span></span> <span data-ttu-id="82962-140">Nel codice seguente viene illustrato come eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="82962-140">The following code shows how this could be done.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="82962-141">C++</span><span class="sxs-lookup"><span data-stu-id="82962-141">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#define MOUSEEVENTF_FROMTOUCH 0xFF515700

if ((GetMessageExtraInfo() & MOUSEEVENTF_FROMTOUCH) == MOUSEEVENTF_FROMTOUCH) { 
    // Click was generated by wisptis / Windows Touch
}else{ 
    // Click was generated by the mouse.
}
</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 



| <span data-ttu-id="82962-142">Categoria</span><span class="sxs-lookup"><span data-stu-id="82962-142">Category</span></span> | <span data-ttu-id="82962-143">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82962-143">Description</span></span> |
|----------|------------------------------------------------------------------------------------|
| <span data-ttu-id="82962-144">Problema</span><span class="sxs-lookup"><span data-stu-id="82962-144">Issue</span></span>    | <span data-ttu-id="82962-145">Ricerca per categorie eseguire applicazioni Microsoft PixelSense in Windows 7?</span><span class="sxs-lookup"><span data-stu-id="82962-145">How do I run Microsoft PixelSense applications on Windows 7?</span></span>                       |
| <span data-ttu-id="82962-146">Causa</span><span class="sxs-lookup"><span data-stu-id="82962-146">Cause</span></span>    | <span data-ttu-id="82962-147">Windows Touch e Microsoft PixelSense non sono compatibili.</span><span class="sxs-lookup"><span data-stu-id="82962-147">Windows Touch and Microsoft PixelSense are incompatible.</span></span>                           |
| <span data-ttu-id="82962-148">Soluzione</span><span class="sxs-lookup"><span data-stu-id="82962-148">Solution</span></span> | <span data-ttu-id="82962-149">È necessario scegliere come destinazione la piattaforma Windows 7 o la piattaforma Microsoft PixelSense.</span><span class="sxs-lookup"><span data-stu-id="82962-149">You either need to target the Windows 7 platform or Microsoft PixelSense platform.</span></span> |



 

## <a name="troubleshooting-manipulations-and-inertia"></a><span data-ttu-id="82962-150">Risoluzione dei problemi relativi a modifiche e inerzia</span><span class="sxs-lookup"><span data-stu-id="82962-150">Troubleshooting Manipulations and Inertia</span></span>



| <span data-ttu-id="82962-151">Categoria</span><span class="sxs-lookup"><span data-stu-id="82962-151">Category</span></span> | <span data-ttu-id="82962-152">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82962-152">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82962-153">Problema</span><span class="sxs-lookup"><span data-stu-id="82962-153">Issue</span></span>    | <span data-ttu-id="82962-154">L'applicazione si blocca senza motivo.</span><span class="sxs-lookup"><span data-stu-id="82962-154">My application is freezing for no reason.</span></span> <span data-ttu-id="82962-155">Si verificano violazioni di accesso quando si inizializzano le interfacce degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="82962-155">I'm getting access violations when I initialize my object interfaces.</span></span>                                                                                                                                          |
| <span data-ttu-id="82962-156">Causa</span><span class="sxs-lookup"><span data-stu-id="82962-156">Cause</span></span>    | <span data-ttu-id="82962-157">Manca una chiamata a **CoInitialize** quando si usano [**le interfacce IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) [**o IInertiaProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)</span><span class="sxs-lookup"><span data-stu-id="82962-157">Missing a call to **CoInitialize** when using the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) or [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interfaces.</span></span>                                                                                 |
| <span data-ttu-id="82962-158">Soluzione</span><span class="sxs-lookup"><span data-stu-id="82962-158">Solution</span></span> | <span data-ttu-id="82962-159">Questo problema può essere causato dalla creazione di un'istanza degli oggetti Windows Touch Component Object Model (COM) senza chiamare CoInitialize.</span><span class="sxs-lookup"><span data-stu-id="82962-159">This could be caused by instantiating the Windows Touch Component Object Model (COM) objects without calling CoInitialize.</span></span> <span data-ttu-id="82962-160">Ciò si verifica a volte quando si convertono progetti dall'uso di movimenti all'uso delle manipolazioni o delle interfacce di inerzia.</span><span class="sxs-lookup"><span data-stu-id="82962-160">This happens sometimes when you are converting projects from using gestures to using the manipulations or inertia interfaces.</span></span> |



 



| <span data-ttu-id="82962-161">Categoria</span><span class="sxs-lookup"><span data-stu-id="82962-161">Category</span></span> | <span data-ttu-id="82962-162">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82962-162">Description</span></span> |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82962-163">Problema</span><span class="sxs-lookup"><span data-stu-id="82962-163">Issue</span></span>    | <span data-ttu-id="82962-164">L'oggetto ruota in modo non corretto durante la traduzione.</span><span class="sxs-lookup"><span data-stu-id="82962-164">My object is rotating improperly when it's being translated.</span></span> <span data-ttu-id="82962-165">La rotazione con un solo dito non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="82962-165">Single-finger rotation is not working correctly.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="82962-166">Causa</span><span class="sxs-lookup"><span data-stu-id="82962-166">Cause</span></span>    | <span data-ttu-id="82962-167">Impostazione non corretta dei pivot in un oggetto.</span><span class="sxs-lookup"><span data-stu-id="82962-167">Improperly setting pivots on an object.</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="82962-168">Soluzione</span><span class="sxs-lookup"><span data-stu-id="82962-168">Solution</span></span> | <span data-ttu-id="82962-169">I punti pivot di manipolazione non vengono configurati correttamente.</span><span class="sxs-lookup"><span data-stu-id="82962-169">You are not setting up the manipulation pivot points correctly.</span></span> <span data-ttu-id="82962-170">Impostare le [**proprietà PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) e [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) al centro dell'oggetto o del punto in cui si vuole ruotare e la proprietà [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) sul raggio dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="82962-170">Set the [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) and [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) properties to the center of the object or point you want to rotate around, and set the [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) property to the radius of your object.</span></span> |



 

## <a name="troubleshooting-windows-touch-input"></a><span data-ttu-id="82962-171">Risoluzione dei Windows Touch input</span><span class="sxs-lookup"><span data-stu-id="82962-171">Troubleshooting Windows Touch Input</span></span>



| <span data-ttu-id="82962-172">Categoria</span><span class="sxs-lookup"><span data-stu-id="82962-172">Category</span></span> | <span data-ttu-id="82962-173">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82962-173">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82962-174">Problema</span><span class="sxs-lookup"><span data-stu-id="82962-174">Issue</span></span>    | <span data-ttu-id="82962-175">Dopo aver gestito il [**messaggio WM \_ TOUCH,**](wm-touchdown.md) non si riceve più il feedback sui limiti.</span><span class="sxs-lookup"><span data-stu-id="82962-175">After I handle the [**WM\_TOUCH**](wm-touchdown.md) message, I stop getting boundary feedback.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="82962-176">Causa</span><span class="sxs-lookup"><span data-stu-id="82962-176">Cause</span></span>    | <span data-ttu-id="82962-177">Utilizzo del [**messaggio WM \_ TOUCH**](wm-touchdown.md) senza gestirlo.</span><span class="sxs-lookup"><span data-stu-id="82962-177">Consuming the [**WM\_TOUCH**](wm-touchdown.md) message without handling it.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="82962-178">Soluzione</span><span class="sxs-lookup"><span data-stu-id="82962-178">Solution</span></span> | <span data-ttu-id="82962-179">È probabile che si sta utilizzando Windows Touch un messaggio senza inoltrarlo a **DefWindowProc,** il che comporta un comportamento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="82962-179">You are probably consuming a Windows Touch message without forwarding it to **DefWindowProc**, which will result in unexpected behavior.</span></span> <span data-ttu-id="82962-180">Per [altre Attività iniziali su come gestire correttamente i messaggi](getting-started-with-multi-touch-messages.md) [**WM \_ TOUCH,**](wm-touchdown.md) vedere Windows Touch con i messaggi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="82962-180">Check [Getting Started with Windows Touch Messages](getting-started-with-multi-touch-messages.md) for more information on how to properly handle [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="82962-181">Problema</span><span class="sxs-lookup"><span data-stu-id="82962-181">Issue</span></span></td>
<td><span data-ttu-id="82962-182">Sto includendo windows.h, ma continua a dire che <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> non è definito.</span><span class="sxs-lookup"><span data-stu-id="82962-182">I am including windows.h, but it still says that <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> is not defined.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82962-183">Causa</span><span class="sxs-lookup"><span data-stu-id="82962-183">Cause</span></span></td>
<td><span data-ttu-id="82962-184">La versione di Windows in Targetver.h non è corretta.</span><span class="sxs-lookup"><span data-stu-id="82962-184">The Windows version in Targetver.h is incorrect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82962-185">Soluzione</span><span class="sxs-lookup"><span data-stu-id="82962-185">Solution</span></span></td>
<td><span data-ttu-id="82962-186">Non è stata impostata la versione di Windows corretta nel progetto.</span><span class="sxs-lookup"><span data-stu-id="82962-186">You haven't set the correct Windows version in your project.</span></span> <span data-ttu-id="82962-187">Il codice seguente illustra le versioni di Windows impostate correttamente per Windows Touch in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="82962-187">The following code illustrates the properly set Windows versions for Windows Touch in Windows 7.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="82962-188">C++</span><span class="sxs-lookup"><span data-stu-id="82962-188">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifndef WINVER                  // Specify that the minimum required platform is Windows 7.
#define WINVER 0x0601           
#endif</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="82962-189">Problema</span><span class="sxs-lookup"><span data-stu-id="82962-189">Issue</span></span></td>
<td><span data-ttu-id="82962-190">Le coordinate x e y dell'input tocco sembrano non valide.</span><span class="sxs-lookup"><span data-stu-id="82962-190">My touch input x-coordinates and y-coordinates seem invalid.</span></span> <span data-ttu-id="82962-191">Si tratta di valori più grandi del previsto o di valori negativi.</span><span class="sxs-lookup"><span data-stu-id="82962-191">They are either larger values than I expect or they are negative values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82962-192">Causa</span><span class="sxs-lookup"><span data-stu-id="82962-192">Cause</span></span></td>
<td><span data-ttu-id="82962-193">Potrebbe essere necessario convertire i punti di tocco in pixel o convertire le coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="82962-193">You may need to convert your touch points to pixels, or you may need to convert the screen coordinates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82962-194">Soluzione</span><span class="sxs-lookup"><span data-stu-id="82962-194">Solution</span></span></td>
<td><span data-ttu-id="82962-195">Assicurarsi di chiamare <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong></strong></a> TOUCH_COORD_TO_PIXEL <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>e ScreenToClient.</strong></a></span><span class="sxs-lookup"><span data-stu-id="82962-195">Make sure that you are calling <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> and <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a>.</span></span> <span data-ttu-id="82962-196">A tal fine, osservare il codice indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="82962-196">The following code shows how to do this.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="82962-197">C++</span><span class="sxs-lookup"><span data-stu-id="82962-197">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>      POINT ptInput;
      if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
        for (int i=0; i < static_cast<INT>(cInputs); i++){
          TOUCHINPUT ti = pInputs[i];                       
          if (ti.dwID != 0){                
            // Do something with your touch input handle.
            ptInput.x = TOUCH_COORD_TO_PIXEL(ti.x);
            ptInput.y = TOUCH_COORD_TO_PIXEL(ti.y);
            ScreenToClient(hWnd, &ptInput);
            points[ti.dwID][0] = ptInput.x;
            points[ti.dwID][1] = ptInput.y;
          }
        }
      }</code></pre></td>
</tr>
</tbody>
</table>

<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="82962-198">Per usare la funzione <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient,</strong></a> è necessario avere un supporto DPI elevato nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="82962-198">In order to use the <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a> function, you must have high DPI support in your application.</span></span> <span data-ttu-id="82962-199">Per altre informazioni sul supporto di valori DPI alti, visitare la <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">sezione Relativa ai valori DPI</a> alti di MSDN.</span><span class="sxs-lookup"><span data-stu-id="82962-199">For more information on supporting high DPI, visit the <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">High DPI</a> section of MSDN.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>



 



| <span data-ttu-id="82962-200">Categoria</span><span class="sxs-lookup"><span data-stu-id="82962-200">Category</span></span> | <span data-ttu-id="82962-201">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82962-201">Description</span></span> |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82962-202">Problema</span><span class="sxs-lookup"><span data-stu-id="82962-202">Issue</span></span>    | <span data-ttu-id="82962-203">I messaggi [**WM \_ TOUCH**](wm-touchdown.md) non vengono visualizzati, ma è Windows Touch perché vengono visualizzati [**messaggi WM \_ GESTURE.**](wm-gesture.md)</span><span class="sxs-lookup"><span data-stu-id="82962-203">I'm not seeing [**WM\_TOUCH**](wm-touchdown.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_GESTURE**](wm-gesture.md) messages.</span></span>                                                             |
| <span data-ttu-id="82962-204">Causa</span><span class="sxs-lookup"><span data-stu-id="82962-204">Cause</span></span>    | <span data-ttu-id="82962-205">Manca una chiamata a [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span><span class="sxs-lookup"><span data-stu-id="82962-205">Missing a call to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                          |
| <span data-ttu-id="82962-206">Soluzione</span><span class="sxs-lookup"><span data-stu-id="82962-206">Solution</span></span> | <span data-ttu-id="82962-207">[**WM \_ I messaggi TOUCH**](wm-touchdown.md) [**e WM \_ GESTURE**](wm-gesture.md) si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="82962-207">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="82962-208">Se non si chiama [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), si riceveranno solo messaggi **WM \_ GESTURE.**</span><span class="sxs-lookup"><span data-stu-id="82962-208">If you don't call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will receive only **WM\_GESTURE** messages.</span></span> |



 



| <span data-ttu-id="82962-209">Categoria</span><span class="sxs-lookup"><span data-stu-id="82962-209">Category</span></span> | <span data-ttu-id="82962-210">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82962-210">Description</span></span> |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82962-211">Problema</span><span class="sxs-lookup"><span data-stu-id="82962-211">Issue</span></span>    | <span data-ttu-id="82962-212">Si notno piccoli ritardi dal momento in cui si tocca il dito verso il basso fino a quando si riceve l'input nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="82962-212">I am noticing small delays from the time I touch my finger down to when I am getting input in my application.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="82962-213">Causa</span><span class="sxs-lookup"><span data-stu-id="82962-213">Cause</span></span>    | <span data-ttu-id="82962-214">Il rifiuto del palmo causa ritardi nell'input.</span><span class="sxs-lookup"><span data-stu-id="82962-214">Palm rejection is causing delays in input.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="82962-215">Soluzione</span><span class="sxs-lookup"><span data-stu-id="82962-215">Solution</span></span> | <span data-ttu-id="82962-216">Se **TWF \_ WANTPALM** è impostato nelle chiamate a [**RegisterTouchWindow,**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)il rifiuto tramite palmo è abilitato.</span><span class="sxs-lookup"><span data-stu-id="82962-216">If **TWF\_WANTPALM** is set in calls to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), palm rejection is enabled.</span></span> <span data-ttu-id="82962-217">Ciò causa un piccolo ritardo (100 ms) mentre il software verifica se l'input proviene da un dito, una penna o il palmo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="82962-217">This causes a small (100 ms) delay while the software tests whether input is coming from a finger, pen, or the user's palm.</span></span> <span data-ttu-id="82962-218">Disabilitare il rifiuto del palmo **chiamando RegisterTouchWindow** con il flag **\_ TWF WANTPALM** deselezionato.</span><span class="sxs-lookup"><span data-stu-id="82962-218">Disable palm rejection by calling **RegisterTouchWindow** with the **TWF\_WANTPALM** flag cleared.</span></span> |



 

## <a name="troubleshooting-windows-touch-gestures"></a><span data-ttu-id="82962-219">Risoluzione dei Windows Touch movimenti</span><span class="sxs-lookup"><span data-stu-id="82962-219">Troubleshooting Windows Touch Gestures</span></span>



| <span data-ttu-id="82962-220">Categoria</span><span class="sxs-lookup"><span data-stu-id="82962-220">Category</span></span> | <span data-ttu-id="82962-221">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82962-221">Description</span></span> |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82962-222">Problema</span><span class="sxs-lookup"><span data-stu-id="82962-222">Issue</span></span>    | <span data-ttu-id="82962-223">Dopo la gestione del [**messaggio WM \_ GESTURE,**](wm-gesture.md) non si riceve più il feedback sui limiti.</span><span class="sxs-lookup"><span data-stu-id="82962-223">After handling the [**WM\_GESTURE**](wm-gesture.md) message, I stop getting boundary feedback.</span></span> <span data-ttu-id="82962-224">In caso contrario, un movimento che funzionava in precedenza non funziona ora.</span><span class="sxs-lookup"><span data-stu-id="82962-224">Or, a gesture that worked previously does not work now.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="82962-225">Causa</span><span class="sxs-lookup"><span data-stu-id="82962-225">Cause</span></span>    | <span data-ttu-id="82962-226">Utilizzo del [**messaggio WM \_ GESTURE**](wm-gesture.md) senza gestirlo.</span><span class="sxs-lookup"><span data-stu-id="82962-226">Consuming the [**WM\_GESTURE**](wm-gesture.md) message without handling it.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="82962-227">Soluzione</span><span class="sxs-lookup"><span data-stu-id="82962-227">Solution</span></span> | <span data-ttu-id="82962-228">È probabile che si sta utilizzando Windows Touch messaggio senza inoltrarlo a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), che avrà un comportamento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="82962-228">You are probably consuming a Windows Touch message without forwarding it to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), which will result in unexpected behavior.</span></span> <span data-ttu-id="82962-229">Per altre informazioni su come gestire correttamente i messaggi [**WM \_ GESTURE,**](wm-gesture.md) vedere Attività iniziali con i movimenti di [Windows.](getting-started-with-multi-touch-gestures.md)</span><span class="sxs-lookup"><span data-stu-id="82962-229">Check [Getting Started with Windows Gestures](getting-started-with-multi-touch-gestures.md) for more information on how to properly handle [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> |



 



| <span data-ttu-id="82962-230">Categoria</span><span class="sxs-lookup"><span data-stu-id="82962-230">Category</span></span> | <span data-ttu-id="82962-231">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82962-231">Description</span></span> |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82962-232">Problema</span><span class="sxs-lookup"><span data-stu-id="82962-232">Issue</span></span>    | <span data-ttu-id="82962-233">I messaggi [**WM \_ GESTURE**](wm-gesture.md) non vengono visualizzati, ma è Windows Touch perché vengono visualizzati [**messaggi WM \_ TOUCH.**](wm-touchdown.md)</span><span class="sxs-lookup"><span data-stu-id="82962-233">I'm not seeing [**WM\_GESTURE**](wm-gesture.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span>                                                      |
| <span data-ttu-id="82962-234">Causa</span><span class="sxs-lookup"><span data-stu-id="82962-234">Cause</span></span>    | <span data-ttu-id="82962-235">Chiamata [**di RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span><span class="sxs-lookup"><span data-stu-id="82962-235">Calling [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                             |
| <span data-ttu-id="82962-236">Soluzione</span><span class="sxs-lookup"><span data-stu-id="82962-236">Solution</span></span> | <span data-ttu-id="82962-237">[**WM \_ I messaggi TOUCH**](wm-touchdown.md) [**e WM \_ GESTURE**](wm-gesture.md) si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="82962-237">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="82962-238">Se si chiama [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), non si riceveranno **messaggi WM \_ GESTURE.**</span><span class="sxs-lookup"><span data-stu-id="82962-238">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will not receive **WM\_GESTURE** messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="82962-239">Problema</span><span class="sxs-lookup"><span data-stu-id="82962-239">Issue</span></span></td>
<td><span data-ttu-id="82962-240">Non vengono visualizzati tutti i movimenti previsti.</span><span class="sxs-lookup"><span data-stu-id="82962-240">I'm not seeing all of the gestures that I expect to see.</span></span> <span data-ttu-id="82962-241">Ad esempio, i movimenti vengono visualizzati con l'identificatore <strong>GID_PAN</strong> ma non <strong>GID_ROTATE</strong>.</span><span class="sxs-lookup"><span data-stu-id="82962-241">For example, I'm seeing gestures with the identifier <strong>GID_PAN</strong> but not <strong>GID_ROTATE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82962-242">Causa</span><span class="sxs-lookup"><span data-stu-id="82962-242">Cause</span></span></td>
<td><span data-ttu-id="82962-243">Alcuni movimenti, ad esempio il movimento di rotazione, non sono abilitati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="82962-243">Some gestures, such as the rotate gesture, are not enabled by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82962-244">Soluzione</span><span class="sxs-lookup"><span data-stu-id="82962-244">Solution</span></span></td>
<td><span data-ttu-id="82962-245">È necessario chiamare <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>SetGestureConfig</strong></a> quando si riceve un messaggio <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> come descritto nel riferimento <strong>WM_GESTURENOTIFY</strong> oppure aggiungere un gestore per il messaggio <strong>WM_GESTURENOTIFY.</strong></span><span class="sxs-lookup"><span data-stu-id="82962-245">You need to call <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>SetGestureConfig</strong></a> when you receive a <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> message as described in the <strong>WM_GESTURENOTIFY</strong> reference, or you need to add a handler for the <strong>WM_GESTURENOTIFY</strong> message.</span></span> <span data-ttu-id="82962-246">Il codice seguente illustra come può essere implementato un gestore per abilitare il supporto per la rotazione.</span><span class="sxs-lookup"><span data-stu-id="82962-246">The following code shows how a handler could be implemented to enable support for rotation.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="82962-247">C++</span><span class="sxs-lookup"><span data-stu-id="82962-247">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>// The message map.
BEGIN_MESSAGE_MAP()
    ON_WM_CREATE()
     ... ... ...
    ON_MESSAGE(WM_GESTURENOTIFY, OnWindowsGestureNotify)
END_MESSAGE_MAP()  

LRESULT CTestWndApp::OnWindowsGestureNotify(
    UINT    uMsg,
    WPARAM  wParam,
    LPARAM  lParam,
    BOOL&   bHandled
    ){
    GESTURECONFIG gc;
    gc.dwID    = GID_ROTATE; // The gesture identifier.
    gc.dwWant  = GC_ROTATE;  // The gesture command you are enabling for GID_ROTATE.
    gc.dwBlock = 0;          // Don&#39;t block anything.
    UINT uiGcs = 1;          // The number of gestures being set.

  BOOL bResult = SetGestureConfig(g_hMainWnd, 0, uiGcs, &gc, sizeof(GESTURECONFIG));
    if(!bResult) {
        // Something went wrong, report the error using your preferred logging.
    }

  return 0;
}  </code></pre></td>
</tr>
</tbody>
</table>

<span data-ttu-id="82962-248">Per altri esempi di configurazioni tipiche dei movimenti, <strong>vedere SetGestureConfig</strong>.</span><span class="sxs-lookup"><span data-stu-id="82962-248">For more examples of typical gesture configurations, see <strong>SetGestureConfig</strong>.</span></span></td>
</tr>
</tbody>
</table>



 



| <span data-ttu-id="82962-249">Categoria</span><span class="sxs-lookup"><span data-stu-id="82962-249">Category</span></span> | <span data-ttu-id="82962-250">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82962-250">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82962-251">Problema</span><span class="sxs-lookup"><span data-stu-id="82962-251">Issue</span></span>    | <span data-ttu-id="82962-252">Le barre di scorrimento personalizzate nell'applicazione non scorrono quando si esegue il movimento di panoramica.</span><span class="sxs-lookup"><span data-stu-id="82962-252">The custom scroll bars in my application are not scrolling when I perform the pan gesture.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="82962-253">Causa</span><span class="sxs-lookup"><span data-stu-id="82962-253">Cause</span></span>    | <span data-ttu-id="82962-254">Gestori mancanti per i messaggi WM \_ \* SCROLL corretti.</span><span class="sxs-lookup"><span data-stu-id="82962-254">Missing handlers for the correct WM\_\*SCROLL messages.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="82962-255">Soluzione</span><span class="sxs-lookup"><span data-stu-id="82962-255">Solution</span></span> | <span data-ttu-id="82962-256">Non si stanno gestendo tutti i messaggi WM \_ \* SCROLL nelle barre di scorrimento personalizzate.</span><span class="sxs-lookup"><span data-stu-id="82962-256">You are not handling all of the WM\_\*SCROLL messages in your custom scroll bars.</span></span> <span data-ttu-id="82962-257">È consigliabile gestire il messaggio [**WM \_ GESTURE**](wm-gesture.md) anziché mantenere la funzionalità personalizzata della barra di scorrimento tramite il supporto legacy.</span><span class="sxs-lookup"><span data-stu-id="82962-257">It is recommended that you handle the [**WM\_GESTURE**](wm-gesture.md) message rather than retain custom scrollbar functionality through legacy support.</span></span> <span data-ttu-id="82962-258">È necessario supportare i messaggi come descritto in dettaglio nella sezione [Supporto legacy per la panoramica con barre di scorrimento](legacy-support-for-panning-with-scrollbars.md).</span><span class="sxs-lookup"><span data-stu-id="82962-258">You need to support messages as detailed in the section [Legacy Support for Panning with Scroll bars](legacy-support-for-panning-with-scrollbars.md).</span></span> |



 



| <span data-ttu-id="82962-259">Categoria</span><span class="sxs-lookup"><span data-stu-id="82962-259">Category</span></span> | <span data-ttu-id="82962-260">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82962-260">Description</span></span> |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82962-261">Problema</span><span class="sxs-lookup"><span data-stu-id="82962-261">Issue</span></span>    | <span data-ttu-id="82962-262">Si verificano ritardi per i movimenti.</span><span class="sxs-lookup"><span data-stu-id="82962-262">I am getting delays for gestures.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="82962-263">Causa</span><span class="sxs-lookup"><span data-stu-id="82962-263">Cause</span></span>    | <span data-ttu-id="82962-264">I gesti rapidi possono causare ritardi per i movimenti.</span><span class="sxs-lookup"><span data-stu-id="82962-264">Flicks may be causing delays for gestures.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="82962-265">Soluzione</span><span class="sxs-lookup"><span data-stu-id="82962-265">Solution</span></span> | <span data-ttu-id="82962-266">I movimenti rapidi possono causare ritardi per il tempo necessario all'applicazione per ricevere [**messaggi WM \_ GESTURE.**](wm-gesture.md)</span><span class="sxs-lookup"><span data-stu-id="82962-266">Flicks can cause delays for how long it takes for your application to receive [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> <span data-ttu-id="82962-267">Per [informazioni sulla disabilitazione dei gesti rapidi,](legacy-support-for-panning-with-scrollbars.md) vedere Supporto legacy per la panoramica con le barre di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="82962-267">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling flicks.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="82962-268">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="82962-268">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82962-269">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="82962-269">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 