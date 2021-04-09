---
title: Risoluzione dei problemi relativi alle applicazioni
description: Questa sezione fornisce soluzioni ai problemi comuni.
ms.assetid: dfdc5a97-aa0a-4011-8f61-6e405e28b6f8
keywords:
- Windows Touch, risoluzione dei problemi delle applicazioni
- Windows Touch, rifiuto di Palm
- rifiuto Palm
- Windows Touch, supporto legacy
- risoluzione dei problemi di Windows Touch
- inerzia, risoluzione dei problemi delle applicazioni
- manipolazioni, risoluzione dei problemi delle applicazioni
- movimenti, risoluzione dei problemi delle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1aeb37f139ea9063c07dd7d629ac5579229863
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969026"
---
# <a name="troubleshooting-applications"></a><span data-ttu-id="51acf-111">Risoluzione dei problemi relativi alle applicazioni</span><span class="sxs-lookup"><span data-stu-id="51acf-111">Troubleshooting Applications</span></span>

<span data-ttu-id="51acf-112">Questa sezione fornisce soluzioni ai problemi comuni.</span><span class="sxs-lookup"><span data-stu-id="51acf-112">This section gives solutions to common problems.</span></span>

## <a name="general-troubleshooting"></a><span data-ttu-id="51acf-113">Risoluzione di problemi generali</span><span class="sxs-lookup"><span data-stu-id="51acf-113">General Troubleshooting</span></span>



|          |                                                                                                                                                                                                                                                                                                                    |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51acf-114">Problema</span><span class="sxs-lookup"><span data-stu-id="51acf-114">Issue</span></span>    | <span data-ttu-id="51acf-115">Sono in esecuzione Windows Server 2008 e le funzionalità di Windows Touch non funzionano.</span><span class="sxs-lookup"><span data-stu-id="51acf-115">I am running Windows Server 2008 and Windows Touch features are not working.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="51acf-116">Causa</span><span class="sxs-lookup"><span data-stu-id="51acf-116">Cause</span></span>    | <span data-ttu-id="51acf-117">L'esperienza desktop non è stata abilitata.</span><span class="sxs-lookup"><span data-stu-id="51acf-117">You haven't enabled the Desktop Experience.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="51acf-118">Soluzione</span><span class="sxs-lookup"><span data-stu-id="51acf-118">Solution</span></span> | <span data-ttu-id="51acf-119">Aprire lo strumento di amministrazione Server Manager: fare clic sul pulsante **Start**, scegliere **strumenti di amministrazione** e quindi fare clic su **Server Manager**.</span><span class="sxs-lookup"><span data-stu-id="51acf-119">Open the Server Manager administrative tool: click **Start**, point to **Administrative Tools**, and then click **Server Manager**.</span></span> <span data-ttu-id="51acf-120">Fare clic sull'elemento **funzionalità** nella colonna a sinistra.</span><span class="sxs-lookup"><span data-stu-id="51acf-120">Click the **Features** item in the left column.</span></span> <span data-ttu-id="51acf-121">Fare clic su **Aggiungi funzionalità** nella sezione **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="51acf-121">Click **Add Features** in the **Features** section.</span></span> <span data-ttu-id="51acf-122">Selezionare **esperienza desktop**, fare clic su **Avanti** e quindi su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="51acf-122">Select **Desktop Experience**, click **Next**, and then click **Install**.</span></span> |



 



|          |                                                                                                                                                                                                    |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51acf-123">Problema</span><span class="sxs-lookup"><span data-stu-id="51acf-123">Issue</span></span>    | <span data-ttu-id="51acf-124">Quando sposto il dito rapidamente nell'applicazione, viene visualizzata una freccia e il gesto o la manipolazione non vengono registrati correttamente.</span><span class="sxs-lookup"><span data-stu-id="51acf-124">Whenever I move my finger quickly across my application, an arrow appears and my gesture or manipulation is not registering correctly.</span></span>                                                             |
| <span data-ttu-id="51acf-125">Causa</span><span class="sxs-lookup"><span data-stu-id="51acf-125">Cause</span></span>    | <span data-ttu-id="51acf-126">Con i gesti rapidi abilitati quando non è necessario.</span><span class="sxs-lookup"><span data-stu-id="51acf-126">Having flicks enabled when you don't need it.</span></span>                                                                                                                                                      |
| <span data-ttu-id="51acf-127">Soluzione</span><span class="sxs-lookup"><span data-stu-id="51acf-127">Solution</span></span> | <span data-ttu-id="51acf-128">Sono abilitati i gesti rapidi quando si desidera che vengano disabilitati.</span><span class="sxs-lookup"><span data-stu-id="51acf-128">You have flicks enabled when you want it to be disabled.</span></span> <span data-ttu-id="51acf-129">Per informazioni sulla disabilitazione di gesti rapidi penna, vedere [supporto legacy per la panoramica con le barre di scorrimento](legacy-support-for-panning-with-scrollbars.md) .</span><span class="sxs-lookup"><span data-stu-id="51acf-129">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling pen flicks.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="51acf-130">Problema</span><span class="sxs-lookup"><span data-stu-id="51acf-130">Issue</span></span></td>
<td><span data-ttu-id="51acf-131">Non è possibile distinguere tra input del mouse e input di Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="51acf-131">I can't discern between mouse input and Windows Touch input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51acf-132">Causa</span><span class="sxs-lookup"><span data-stu-id="51acf-132">Cause</span></span></td>
<td><span data-ttu-id="51acf-133">Windows genera messaggi del mouse per il supporto legacy quando un utente fa clic sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="51acf-133">Windows generates mouse messages for legacy support when a user clicks on the screen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51acf-134">Soluzione</span><span class="sxs-lookup"><span data-stu-id="51acf-134">Solution</span></span></td>
<td><span data-ttu-id="51acf-135">Per determinare l'origine, è possibile chiamare <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> per la <strong>WM_LBUTTONDOWN</strong> e <strong>WM_LBUTTONUP</strong> i messaggi.</span><span class="sxs-lookup"><span data-stu-id="51acf-135">You can call <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> for the <strong>WM_LBUTTONDOWN</strong> and <strong>WM_LBUTTONUP</strong> messages to determine the source.</span></span> <span data-ttu-id="51acf-136">Il codice seguente illustra come eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="51acf-136">The following code shows how this could be done.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="51acf-137">C++</span><span class="sxs-lookup"><span data-stu-id="51acf-137">C++</span></span></th>
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



 



|          |                                                                                    |
|----------|------------------------------------------------------------------------------------|
| <span data-ttu-id="51acf-138">Problema</span><span class="sxs-lookup"><span data-stu-id="51acf-138">Issue</span></span>    | <span data-ttu-id="51acf-139">Ricerca per categorie eseguire applicazioni Microsoft PixelSense in Windows 7?</span><span class="sxs-lookup"><span data-stu-id="51acf-139">How do I run Microsoft PixelSense applications on Windows 7?</span></span>                       |
| <span data-ttu-id="51acf-140">Causa</span><span class="sxs-lookup"><span data-stu-id="51acf-140">Cause</span></span>    | <span data-ttu-id="51acf-141">Windows Touch e Microsoft PixelSense sono incompatibili.</span><span class="sxs-lookup"><span data-stu-id="51acf-141">Windows Touch and Microsoft PixelSense are incompatible.</span></span>                           |
| <span data-ttu-id="51acf-142">Soluzione</span><span class="sxs-lookup"><span data-stu-id="51acf-142">Solution</span></span> | <span data-ttu-id="51acf-143">È necessario avere come destinazione la piattaforma Windows 7 o la piattaforma Microsoft PixelSense.</span><span class="sxs-lookup"><span data-stu-id="51acf-143">You either need to target the Windows 7 platform or Microsoft PixelSense platform.</span></span> |



 

## <a name="troubleshooting-manipulations-and-inertia"></a><span data-ttu-id="51acf-144">Risoluzione dei problemi di manipolazione e inerzia</span><span class="sxs-lookup"><span data-stu-id="51acf-144">Troubleshooting Manipulations and Inertia</span></span>



|          |                                                                                                                                                                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51acf-145">Problema</span><span class="sxs-lookup"><span data-stu-id="51acf-145">Issue</span></span>    | <span data-ttu-id="51acf-146">L'applicazione è in blocco per nessun motivo.</span><span class="sxs-lookup"><span data-stu-id="51acf-146">My application is freezing for no reason.</span></span> <span data-ttu-id="51acf-147">Si ricevono violazioni di accesso quando si inizializzano le interfacce oggetto.</span><span class="sxs-lookup"><span data-stu-id="51acf-147">I'm getting access violations when I initialize my object interfaces.</span></span>                                                                                                                                          |
| <span data-ttu-id="51acf-148">Causa</span><span class="sxs-lookup"><span data-stu-id="51acf-148">Cause</span></span>    | <span data-ttu-id="51acf-149">Chiamata a **CoInitialize** mancante quando si utilizzano le interfacce [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) o [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .</span><span class="sxs-lookup"><span data-stu-id="51acf-149">Missing a call to **CoInitialize** when using the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) or [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interfaces.</span></span>                                                                                 |
| <span data-ttu-id="51acf-150">Soluzione</span><span class="sxs-lookup"><span data-stu-id="51acf-150">Solution</span></span> | <span data-ttu-id="51acf-151">Questo problema può essere causato dalla creazione di un'istanza degli oggetti di Windows Touch Component Object Model (COM) senza chiamare CoInitialize.</span><span class="sxs-lookup"><span data-stu-id="51acf-151">This could be caused by instantiating the Windows Touch Component Object Model (COM) objects without calling CoInitialize.</span></span> <span data-ttu-id="51acf-152">Questo problema si verifica a volte quando si convertono progetti dall'uso di movimenti all'uso di modifiche o interfacce di inerzia.</span><span class="sxs-lookup"><span data-stu-id="51acf-152">This happens sometimes when you are converting projects from using gestures to using the manipulations or inertia interfaces.</span></span> |



 



|          |                                                                                                                                                                                                                                                                                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51acf-153">Problema</span><span class="sxs-lookup"><span data-stu-id="51acf-153">Issue</span></span>    | <span data-ttu-id="51acf-154">L'oggetto viene ruotato in modo errato durante la traduzione.</span><span class="sxs-lookup"><span data-stu-id="51acf-154">My object is rotating improperly when it's being translated.</span></span> <span data-ttu-id="51acf-155">La rotazione di un singolo dito non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="51acf-155">Single-finger rotation is not working correctly.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="51acf-156">Causa</span><span class="sxs-lookup"><span data-stu-id="51acf-156">Cause</span></span>    | <span data-ttu-id="51acf-157">Impostazione errata di pivot in un oggetto.</span><span class="sxs-lookup"><span data-stu-id="51acf-157">Improperly setting pivots on an object.</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="51acf-158">Soluzione</span><span class="sxs-lookup"><span data-stu-id="51acf-158">Solution</span></span> | <span data-ttu-id="51acf-159">I punti pivot di manipolazione non vengono configurati correttamente.</span><span class="sxs-lookup"><span data-stu-id="51acf-159">You are not setting up the manipulation pivot points correctly.</span></span> <span data-ttu-id="51acf-160">Impostare le proprietà [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) e [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) sul centro dell'oggetto o del punto che si desidera ruotare e impostare la proprietà [**pivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) sul raggio dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="51acf-160">Set the [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) and [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) properties to the center of the object or point you want to rotate around, and set the [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) property to the radius of your object.</span></span> |



 

## <a name="troubleshooting-windows-touch-input"></a><span data-ttu-id="51acf-161">Risoluzione dei problemi relativi a Windows Touch Input</span><span class="sxs-lookup"><span data-stu-id="51acf-161">Troubleshooting Windows Touch Input</span></span>



|          |                                                                                                                                                                                                                                                                                                                                        |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51acf-162">Problema</span><span class="sxs-lookup"><span data-stu-id="51acf-162">Issue</span></span>    | <span data-ttu-id="51acf-163">Dopo aver gestito il messaggio [**WM \_ touch**](wm-touchdown.md) , si interrompe il feedback del limite.</span><span class="sxs-lookup"><span data-stu-id="51acf-163">After I handle the [**WM\_TOUCH**](wm-touchdown.md) message, I stop getting boundary feedback.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="51acf-164">Causa</span><span class="sxs-lookup"><span data-stu-id="51acf-164">Cause</span></span>    | <span data-ttu-id="51acf-165">Utilizzo del messaggio [**WM \_ touch**](wm-touchdown.md) senza gestirlo.</span><span class="sxs-lookup"><span data-stu-id="51acf-165">Consuming the [**WM\_TOUCH**](wm-touchdown.md) message without handling it.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="51acf-166">Soluzione</span><span class="sxs-lookup"><span data-stu-id="51acf-166">Solution</span></span> | <span data-ttu-id="51acf-167">È probabile che si usi un messaggio Windows Touch senza inoltrarlo a **DefWindowProc**, causando un comportamento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="51acf-167">You are probably consuming a Windows Touch message without forwarding it to **DefWindowProc**, which will result in unexpected behavior.</span></span> <span data-ttu-id="51acf-168">Per ulteriori informazioni su come gestire correttamente i messaggi [**WM \_ touch**](wm-touchdown.md) , controllare [Introduzione con i messaggi di Windows Touch](getting-started-with-multi-touch-messages.md) .</span><span class="sxs-lookup"><span data-stu-id="51acf-168">Check [Getting Started with Windows Touch Messages](getting-started-with-multi-touch-messages.md) for more information on how to properly handle [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="51acf-169">Problema</span><span class="sxs-lookup"><span data-stu-id="51acf-169">Issue</span></span></td>
<td><span data-ttu-id="51acf-170">Sto includendo Windows. h, ma continua a affermare che <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> non è definito.</span><span class="sxs-lookup"><span data-stu-id="51acf-170">I am including windows.h, but it still says that <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> is not defined.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51acf-171">Causa</span><span class="sxs-lookup"><span data-stu-id="51acf-171">Cause</span></span></td>
<td><span data-ttu-id="51acf-172">La versione di Windows in targetver. h non è corretta.</span><span class="sxs-lookup"><span data-stu-id="51acf-172">The Windows version in Targetver.h is incorrect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51acf-173">Soluzione</span><span class="sxs-lookup"><span data-stu-id="51acf-173">Solution</span></span></td>
<td><span data-ttu-id="51acf-174">Non è stata impostata la versione corretta di Windows nel progetto.</span><span class="sxs-lookup"><span data-stu-id="51acf-174">You haven't set the correct Windows version in your project.</span></span> <span data-ttu-id="51acf-175">Nel codice seguente viene illustrata la corretta impostazione delle versioni di Windows per Windows Touch in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="51acf-175">The following code illustrates the properly set Windows versions for Windows Touch in Windows 7.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="51acf-176">C++</span><span class="sxs-lookup"><span data-stu-id="51acf-176">C++</span></span></th>
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
<td><span data-ttu-id="51acf-177">Problema</span><span class="sxs-lookup"><span data-stu-id="51acf-177">Issue</span></span></td>
<td><span data-ttu-id="51acf-178">Le coordinate x di input tocco e le coordinate y sembrano non valide.</span><span class="sxs-lookup"><span data-stu-id="51acf-178">My touch input x-coordinates and y-coordinates seem invalid.</span></span> <span data-ttu-id="51acf-179">Sono valori più grandi di quelli previsti o sono valori negativi.</span><span class="sxs-lookup"><span data-stu-id="51acf-179">They are either larger values than I expect or they are negative values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51acf-180">Causa</span><span class="sxs-lookup"><span data-stu-id="51acf-180">Cause</span></span></td>
<td><span data-ttu-id="51acf-181">Potrebbe essere necessario convertire i punti di tocco in pixel o potrebbe essere necessario convertire le coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="51acf-181">You may need to convert your touch points to pixels, or you may need to convert the screen coordinates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51acf-182">Soluzione</span><span class="sxs-lookup"><span data-stu-id="51acf-182">Solution</span></span></td>
<td><span data-ttu-id="51acf-183">Assicurarsi di chiamare <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> e <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="51acf-183">Make sure that you are calling <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> and <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a>.</span></span> <span data-ttu-id="51acf-184">A tal fine, osservare il codice indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="51acf-184">The following code shows how to do this.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="51acf-185">C++</span><span class="sxs-lookup"><span data-stu-id="51acf-185">C++</span></span></th>
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
<span data-ttu-id="51acf-186">Per usare la funzione <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a> , è necessario disporre di un supporto DPI elevato nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="51acf-186">In order to use the <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a> function, you must have high DPI support in your application.</span></span> <span data-ttu-id="51acf-187">Per ulteriori informazioni sul supporto di valori DPI alti, vedere la sezione relativa a <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">DPI elevata</a> di MSDN.</span><span class="sxs-lookup"><span data-stu-id="51acf-187">For more information on supporting high DPI, visit the <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">High DPI</a> section of MSDN.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>



 



|          |                                                                                                                                                                                                                                |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51acf-188">Problema</span><span class="sxs-lookup"><span data-stu-id="51acf-188">Issue</span></span>    | <span data-ttu-id="51acf-189">Non vengono visualizzati i messaggi [**WM \_ touch**](wm-touchdown.md) , ma so che Windows Touch funziona perché i messaggi di [**\_ movimento WM**](wm-gesture.md) sono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="51acf-189">I'm not seeing [**WM\_TOUCH**](wm-touchdown.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_GESTURE**](wm-gesture.md) messages.</span></span>                                                             |
| <span data-ttu-id="51acf-190">Causa</span><span class="sxs-lookup"><span data-stu-id="51acf-190">Cause</span></span>    | <span data-ttu-id="51acf-191">Manca una chiamata a [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span><span class="sxs-lookup"><span data-stu-id="51acf-191">Missing a call to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                          |
| <span data-ttu-id="51acf-192">Soluzione</span><span class="sxs-lookup"><span data-stu-id="51acf-192">Solution</span></span> | <span data-ttu-id="51acf-193">[**WM \_**](wm-touchdown.md) I messaggi [**con \_ movimento**](wm-gesture.md) tocco e WM si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="51acf-193">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="51acf-194">Se non si chiama [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), si riceveranno solo messaggi di **\_ movimento WM** .</span><span class="sxs-lookup"><span data-stu-id="51acf-194">If you don't call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will receive only **WM\_GESTURE** messages.</span></span> |



 



|          |                                                                                                                                                                                                                                                                                                                                                       |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51acf-195">Problema</span><span class="sxs-lookup"><span data-stu-id="51acf-195">Issue</span></span>    | <span data-ttu-id="51acf-196">Ho notato piccoli ritardi dal momento in cui tocco il dito fino a quando ricevo input nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="51acf-196">I am noticing small delays from the time I touch my finger down to when I am getting input in my application.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="51acf-197">Causa</span><span class="sxs-lookup"><span data-stu-id="51acf-197">Cause</span></span>    | <span data-ttu-id="51acf-198">Il rifiuto della palma sta causando ritardi nell'input.</span><span class="sxs-lookup"><span data-stu-id="51acf-198">Palm rejection is causing delays in input.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="51acf-199">Soluzione</span><span class="sxs-lookup"><span data-stu-id="51acf-199">Solution</span></span> | <span data-ttu-id="51acf-200">Se **TWF \_ WANTPALM** è impostato in chiamate a [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), il rifiuto della Palma è abilitato.</span><span class="sxs-lookup"><span data-stu-id="51acf-200">If **TWF\_WANTPALM** is set in calls to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), palm rejection is enabled.</span></span> <span data-ttu-id="51acf-201">Ciò provoca un ritardo (100 ms) ridotto mentre il software verifica se l'input viene provenendo da un dito, da una penna o dalla palma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="51acf-201">This causes a small (100 ms) delay while the software tests whether input is coming from a finger, pen, or the user's palm.</span></span> <span data-ttu-id="51acf-202">Disabilitare il rifiuto Palm chiamando **RegisterTouchWindow** con il flag **TWF \_ WANTPALM** cancellato.</span><span class="sxs-lookup"><span data-stu-id="51acf-202">Disable palm rejection by calling **RegisterTouchWindow** with the **TWF\_WANTPALM** flag cleared.</span></span> |



 

## <a name="troubleshooting-windows-touch-gestures"></a><span data-ttu-id="51acf-203">Risoluzione dei problemi relativi ai movimenti tocco di Windows</span><span class="sxs-lookup"><span data-stu-id="51acf-203">Troubleshooting Windows Touch Gestures</span></span>



|          |                                                                                                                                                                                                                                                                                                                                                                                 |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51acf-204">Problema</span><span class="sxs-lookup"><span data-stu-id="51acf-204">Issue</span></span>    | <span data-ttu-id="51acf-205">Dopo aver gestito il messaggio di [**\_ movimento WM**](wm-gesture.md) , si interrompe il feedback del limite.</span><span class="sxs-lookup"><span data-stu-id="51acf-205">After handling the [**WM\_GESTURE**](wm-gesture.md) message, I stop getting boundary feedback.</span></span> <span data-ttu-id="51acf-206">In alternativa, un gesto che funzionava in precedenza non funziona ora.</span><span class="sxs-lookup"><span data-stu-id="51acf-206">Or, a gesture that worked previously does not work now.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="51acf-207">Causa</span><span class="sxs-lookup"><span data-stu-id="51acf-207">Cause</span></span>    | <span data-ttu-id="51acf-208">Utilizzo del messaggio [**di \_ movimento WM**](wm-gesture.md) senza gestirlo.</span><span class="sxs-lookup"><span data-stu-id="51acf-208">Consuming the [**WM\_GESTURE**](wm-gesture.md) message without handling it.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="51acf-209">Soluzione</span><span class="sxs-lookup"><span data-stu-id="51acf-209">Solution</span></span> | <span data-ttu-id="51acf-210">È probabile che si usi un messaggio Windows Touch senza inoltrarlo a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), causando un comportamento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="51acf-210">You are probably consuming a Windows Touch message without forwarding it to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), which will result in unexpected behavior.</span></span> <span data-ttu-id="51acf-211">Per ulteriori informazioni su come gestire correttamente i messaggi di [**\_ movimento WM**](wm-gesture.md) , controllare [Introduzione con i movimenti di Windows](getting-started-with-multi-touch-gestures.md) .</span><span class="sxs-lookup"><span data-stu-id="51acf-211">Check [Getting Started with Windows Gestures](getting-started-with-multi-touch-gestures.md) for more information on how to properly handle [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> |



 



|          |                                                                                                                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51acf-212">Problema</span><span class="sxs-lookup"><span data-stu-id="51acf-212">Issue</span></span>    | <span data-ttu-id="51acf-213">Non vengono visualizzati i messaggi con [**\_ movimento WM**](wm-gesture.md) , ma si sa che Windows Touch funziona perché vengono visualizzati i messaggi [**WM \_ touch**](wm-touchdown.md) .</span><span class="sxs-lookup"><span data-stu-id="51acf-213">I'm not seeing [**WM\_GESTURE**](wm-gesture.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span>                                                      |
| <span data-ttu-id="51acf-214">Causa</span><span class="sxs-lookup"><span data-stu-id="51acf-214">Cause</span></span>    | <span data-ttu-id="51acf-215">Chiamata a [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span><span class="sxs-lookup"><span data-stu-id="51acf-215">Calling [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                             |
| <span data-ttu-id="51acf-216">Soluzione</span><span class="sxs-lookup"><span data-stu-id="51acf-216">Solution</span></span> | <span data-ttu-id="51acf-217">[**WM \_**](wm-touchdown.md) I messaggi [**con \_ movimento**](wm-gesture.md) tocco e WM si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="51acf-217">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="51acf-218">Se si chiama [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), non si riceveranno messaggi di **\_ movimento WM** .</span><span class="sxs-lookup"><span data-stu-id="51acf-218">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will not receive **WM\_GESTURE** messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="51acf-219">Problema</span><span class="sxs-lookup"><span data-stu-id="51acf-219">Issue</span></span></td>
<td><span data-ttu-id="51acf-220">Non vengono visualizzati tutti i movimenti che si prevede di visualizzare.</span><span class="sxs-lookup"><span data-stu-id="51acf-220">I'm not seeing all of the gestures that I expect to see.</span></span> <span data-ttu-id="51acf-221">Ad esempio, vengono visualizzati i movimenti con l'identificatore <strong>GID_PAN</strong> ma non <strong>GID_ROTATE</strong>.</span><span class="sxs-lookup"><span data-stu-id="51acf-221">For example, I'm seeing gestures with the identifier <strong>GID_PAN</strong> but not <strong>GID_ROTATE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51acf-222">Causa</span><span class="sxs-lookup"><span data-stu-id="51acf-222">Cause</span></span></td>
<td><span data-ttu-id="51acf-223">Alcuni movimenti, ad esempio il movimento di rotazione, non sono abilitati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="51acf-223">Some gestures, such as the rotate gesture, are not enabled by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51acf-224">Soluzione</span><span class="sxs-lookup"><span data-stu-id="51acf-224">Solution</span></span></td>
<td><span data-ttu-id="51acf-225">È necessario chiamare <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>SetGestureConfig</strong></a> quando si riceve un messaggio di <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> come descritto nel riferimento <strong>WM_GESTURENOTIFY</strong> oppure è necessario aggiungere un gestore per il messaggio di <strong>WM_GESTURENOTIFY</strong> .</span><span class="sxs-lookup"><span data-stu-id="51acf-225">You need to call <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>SetGestureConfig</strong></a> when you receive a <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> message as described in the <strong>WM_GESTURENOTIFY</strong> reference, or you need to add a handler for the <strong>WM_GESTURENOTIFY</strong> message.</span></span> <span data-ttu-id="51acf-226">Il codice seguente illustra come implementare un gestore per abilitare il supporto per la rotazione.</span><span class="sxs-lookup"><span data-stu-id="51acf-226">The following code shows how a handler could be implemented to enable support for rotation.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="51acf-227">C++</span><span class="sxs-lookup"><span data-stu-id="51acf-227">C++</span></span></th>
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

<span data-ttu-id="51acf-228">Per altri esempi di configurazioni di movimento tipiche, vedere <strong>SetGestureConfig</strong>.</span><span class="sxs-lookup"><span data-stu-id="51acf-228">For more examples of typical gesture configurations, see <strong>SetGestureConfig</strong>.</span></span></td>
</tr>
</tbody>
</table>



 



|          |                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51acf-229">Problema</span><span class="sxs-lookup"><span data-stu-id="51acf-229">Issue</span></span>    | <span data-ttu-id="51acf-230">Le barre di scorrimento personalizzate nell'applicazione non vengono spostate quando si esegue il movimento di panoramica.</span><span class="sxs-lookup"><span data-stu-id="51acf-230">The custom scroll bars in my application are not scrolling when I perform the pan gesture.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="51acf-231">Causa</span><span class="sxs-lookup"><span data-stu-id="51acf-231">Cause</span></span>    | <span data-ttu-id="51acf-232">Gestori mancanti per i messaggi di scorrimento WM corretti \_ \* .</span><span class="sxs-lookup"><span data-stu-id="51acf-232">Missing handlers for the correct WM\_\*SCROLL messages.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="51acf-233">Soluzione</span><span class="sxs-lookup"><span data-stu-id="51acf-233">Solution</span></span> | <span data-ttu-id="51acf-234">Non si gestiscono tutti i messaggi di \_ \* scorrimento WM nelle barre di scorrimento personalizzate.</span><span class="sxs-lookup"><span data-stu-id="51acf-234">You are not handling all of the WM\_\*SCROLL messages in your custom scroll bars.</span></span> <span data-ttu-id="51acf-235">Si consiglia di gestire il messaggio di [**\_ movimento WM**](wm-gesture.md) anziché mantenere la funzionalità di barra di scorrimento personalizzata tramite il supporto legacy.</span><span class="sxs-lookup"><span data-stu-id="51acf-235">It is recommended that you handle the [**WM\_GESTURE**](wm-gesture.md) message rather than retain custom scrollbar functionality through legacy support.</span></span> <span data-ttu-id="51acf-236">È necessario supportare i messaggi come descritto in dettaglio nella sezione [supporto legacy per la panoramica con le barre di scorrimento](legacy-support-for-panning-with-scrollbars.md).</span><span class="sxs-lookup"><span data-stu-id="51acf-236">You need to support messages as detailed in the section [Legacy Support for Panning with Scroll bars](legacy-support-for-panning-with-scrollbars.md).</span></span> |



 



|          |                                                                                                                                                                                                                                                                 |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51acf-237">Problema</span><span class="sxs-lookup"><span data-stu-id="51acf-237">Issue</span></span>    | <span data-ttu-id="51acf-238">Ricevo ritardi per i movimenti.</span><span class="sxs-lookup"><span data-stu-id="51acf-238">I am getting delays for gestures.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="51acf-239">Causa</span><span class="sxs-lookup"><span data-stu-id="51acf-239">Cause</span></span>    | <span data-ttu-id="51acf-240">I gesti rapidi possono causare ritardi per i movimenti.</span><span class="sxs-lookup"><span data-stu-id="51acf-240">Flicks may be causing delays for gestures.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="51acf-241">Soluzione</span><span class="sxs-lookup"><span data-stu-id="51acf-241">Solution</span></span> | <span data-ttu-id="51acf-242">I gesti rapidi possono causare ritardi sul tempo impiegato dall'applicazione per la ricezione di messaggi con [**\_ movimento WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="51acf-242">Flicks can cause delays for how long it takes for your application to receive [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> <span data-ttu-id="51acf-243">Per informazioni sulla disabilitazione di gesti rapidi, vedere [supporto legacy per la panoramica con le barre di scorrimento](legacy-support-for-panning-with-scrollbars.md) .</span><span class="sxs-lookup"><span data-stu-id="51acf-243">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling flicks.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="51acf-244">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="51acf-244">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51acf-245">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="51acf-245">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 