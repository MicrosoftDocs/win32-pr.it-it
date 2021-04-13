---
title: Introduzione con i messaggi di Windows Touch
description: In questa sezione vengono illustrate le attività associate all'acquisizione di un input di Windows Touch per il funzionamento dell'applicazione.
ms.assetid: cd4e140e-a0b8-494f-82d9-bc0bfba55ecd
keywords:
- Windows Touch, messaggi
- Windows Touch, registrazione per l'input tocco
- Windows Touch, test di digitalizzatori di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39048a4f9d643026396328093ae554c0eaa5d08
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399163"
---
# <a name="getting-started-with-windows-touch-messages"></a><span data-ttu-id="6d6dc-106">Introduzione con i messaggi di Windows Touch</span><span class="sxs-lookup"><span data-stu-id="6d6dc-106">Getting Started with Windows Touch Messages</span></span>

<span data-ttu-id="6d6dc-107">In questa sezione vengono illustrate le attività associate all'acquisizione di un input di Windows Touch per il funzionamento dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-107">This section explains the tasks associated with getting Windows Touch input to function in your application.</span></span>

<span data-ttu-id="6d6dc-108">I passaggi seguenti vengono in genere eseguiti quando si utilizzano i messaggi di Windows Touch:</span><span class="sxs-lookup"><span data-stu-id="6d6dc-108">The following steps are typically performed when working with Windows Touch messages:</span></span>

1.  <span data-ttu-id="6d6dc-109">Testare le funzionalità del digitalizzatore di input.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-109">Test the capabilities of the input digitizer.</span></span>
2.  <span data-ttu-id="6d6dc-110">Registrarsi per ricevere messaggi Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-110">Register to receive Windows Touch messages.</span></span>
3.  <span data-ttu-id="6d6dc-111">Gestire i messaggi.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-111">Handle the messages.</span></span>

<span data-ttu-id="6d6dc-112">Il messaggio utilizzato per Windows Touch è [**WM \_ touch**](wm-touchdown.md).</span><span class="sxs-lookup"><span data-stu-id="6d6dc-112">The message used for Windows Touch is [**WM\_TOUCH**](wm-touchdown.md).</span></span> <span data-ttu-id="6d6dc-113">Questo messaggio indica i vari Stati del contatto con un digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-113">This message indicates the various states of contact with a digitizer.</span></span>

## <a name="testing-the-capabilities-of-the-input-digitizer"></a><span data-ttu-id="6d6dc-114">Test delle funzionalità del digitalizzatore di input</span><span class="sxs-lookup"><span data-stu-id="6d6dc-114">Testing the Capabilities of the Input Digitizer</span></span>

<span data-ttu-id="6d6dc-115">La funzione [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) può essere usata per eseguire query sulle funzionalità del digitalizzatore di input passando il valore *nIndex* del **\_ digitalizzatore SM**.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-115">The [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function can be used to query the capabilities of the input digitizer by passing in the *nIndex* value of **SM\_DIGITIZER**.</span></span> <span data-ttu-id="6d6dc-116">[GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) restituisce un campo di bit che indica se il dispositivo è pronto, se il dispositivo supporta la penna o il tocco, se il dispositivo di input è integrato o esterno e se il dispositivo supporta più input (Windows Touch).</span><span class="sxs-lookup"><span data-stu-id="6d6dc-116">[GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) returns a bit field that indicates whether the device is ready, whether the device supports pen or touch, whether the input device is integrated or external, and whether the device supports multiple inputs (Windows Touch).</span></span> <span data-ttu-id="6d6dc-117">La tabella seguente illustra i bit per i vari campi.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-117">The following table shows the bits for the various fields.</span></span>



| <span data-ttu-id="6d6dc-118">bit</span><span class="sxs-lookup"><span data-stu-id="6d6dc-118">Bit</span></span>   | <span data-ttu-id="6d6dc-119">8</span><span class="sxs-lookup"><span data-stu-id="6d6dc-119">8</span></span>           | <span data-ttu-id="6d6dc-120">7</span><span class="sxs-lookup"><span data-stu-id="6d6dc-120">7</span></span>           | <span data-ttu-id="6d6dc-121">6</span><span class="sxs-lookup"><span data-stu-id="6d6dc-121">6</span></span>        | <span data-ttu-id="6d6dc-122">5</span><span class="sxs-lookup"><span data-stu-id="6d6dc-122">5</span></span>        | <span data-ttu-id="6d6dc-123">4</span><span class="sxs-lookup"><span data-stu-id="6d6dc-123">4</span></span>            | <span data-ttu-id="6d6dc-124">3</span><span class="sxs-lookup"><span data-stu-id="6d6dc-124">3</span></span>              | <span data-ttu-id="6d6dc-125">2</span><span class="sxs-lookup"><span data-stu-id="6d6dc-125">2</span></span>              | <span data-ttu-id="6d6dc-126">1</span><span class="sxs-lookup"><span data-stu-id="6d6dc-126">1</span></span>                |
|-------|-------------|-------------|----------|----------|--------------|----------------|----------------|------------------|
| <span data-ttu-id="6d6dc-127">Valore</span><span class="sxs-lookup"><span data-stu-id="6d6dc-127">Value</span></span> | <span data-ttu-id="6d6dc-128">Pronto per lo stack</span><span class="sxs-lookup"><span data-stu-id="6d6dc-128">Stack Ready</span></span> | <span data-ttu-id="6d6dc-129">Multiinput</span><span class="sxs-lookup"><span data-stu-id="6d6dc-129">Multi-input</span></span> | <span data-ttu-id="6d6dc-130">Riservato</span><span class="sxs-lookup"><span data-stu-id="6d6dc-130">Reserved</span></span> | <span data-ttu-id="6d6dc-131">Riservato</span><span class="sxs-lookup"><span data-stu-id="6d6dc-131">Reserved</span></span> | <span data-ttu-id="6d6dc-132">Penna esterna</span><span class="sxs-lookup"><span data-stu-id="6d6dc-132">External Pen</span></span> | <span data-ttu-id="6d6dc-133">Penna integrata</span><span class="sxs-lookup"><span data-stu-id="6d6dc-133">Integrated Pen</span></span> | <span data-ttu-id="6d6dc-134">Tocco esterno</span><span class="sxs-lookup"><span data-stu-id="6d6dc-134">External Touch</span></span> | <span data-ttu-id="6d6dc-135">Tocco integrato</span><span class="sxs-lookup"><span data-stu-id="6d6dc-135">Integrated Touch</span></span> |



 

<span data-ttu-id="6d6dc-136">Per testare il risultato del comando per una particolare funzionalità, è possibile usare l'operatore di & bit per bit e il bit particolare che si sta testando.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-136">To test the result from the command for a particular feature, you can use the bitwise & operator and the particular bit you are testing.</span></span> <span data-ttu-id="6d6dc-137">Ad esempio, per testare Windows Touch, verificare che sia impostato il bit del settimo ordine (0x40 in hex).</span><span class="sxs-lookup"><span data-stu-id="6d6dc-137">For example, to test for Windows Touch, you would test that the seventh-order bit is set (0x40 in hex).</span></span> <span data-ttu-id="6d6dc-138">Nell'esempio di codice seguente viene illustrato come testare questi valori.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-138">The following code example shows how these values could be tested.</span></span>


```C++
#include <windows.h>
```




```C++
// test for touch
int value = GetSystemMetrics(SM_DIGITIZER);
if (value & NID_READY){ /* stack ready */}
if (value  & NID_MULTI_INPUT){
    /* digitizer is multitouch */ 
    MessageBoxW(hWnd, L"Multitouch found", L"IsMulti!", MB_OK);
}
if (value & NID_INTEGRATED_TOUCH){ /* Integrated touch */}
```



<span data-ttu-id="6d6dc-139">Nella tabella seguente sono elencate le costanti definite in Windows. h per il test delle funzionalità di tocco del digitalizzatore di input.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-139">The following table lists the constants defined in windows.h for testing touch capabilities of the input digitizer.</span></span>



| <span data-ttu-id="6d6dc-140">Nome</span><span class="sxs-lookup"><span data-stu-id="6d6dc-140">Name</span></span>                   | <span data-ttu-id="6d6dc-141">Valore</span><span class="sxs-lookup"><span data-stu-id="6d6dc-141">Value</span></span>      | <span data-ttu-id="6d6dc-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d6dc-142">Description</span></span>                                                                                                                                                                                   |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d6dc-143">configurazione del TABLET \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="6d6dc-143">TABLET\_CONFIG\_NONE</span></span>   | <span data-ttu-id="6d6dc-144">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d6dc-144">0x00000000</span></span> | <span data-ttu-id="6d6dc-145">Il digitalizzatore di input non dispone di funzionalità di tocco.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-145">The input digitizer does not have touch capabilities.</span></span>                                                                                                                                         |
| <span data-ttu-id="6d6dc-146">\_tocco integrato \_ NID</span><span class="sxs-lookup"><span data-stu-id="6d6dc-146">NID\_INTEGRATED\_TOUCH</span></span> | <span data-ttu-id="6d6dc-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6d6dc-147">0x00000001</span></span> | <span data-ttu-id="6d6dc-148">Un digitalizzatore Touch integrato viene usato per l'input.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-148">An integrated touch digitizer is used for input.</span></span>                                                                                                                                              |
| <span data-ttu-id="6d6dc-149">\_tocco esterno \_ NID</span><span class="sxs-lookup"><span data-stu-id="6d6dc-149">NID\_EXTERNAL\_TOUCH</span></span>   | <span data-ttu-id="6d6dc-150">0x00000002</span><span class="sxs-lookup"><span data-stu-id="6d6dc-150">0x00000002</span></span> | <span data-ttu-id="6d6dc-151">Per l'input viene usato un digitalizzatore Touch esterno.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-151">An external touch digitizer is used for input.</span></span>                                                                                                                                                |
| <span data-ttu-id="6d6dc-152">\_penna integrata \_ NID</span><span class="sxs-lookup"><span data-stu-id="6d6dc-152">NID\_INTEGRATED\_PEN</span></span>   | <span data-ttu-id="6d6dc-153">0x00000004</span><span class="sxs-lookup"><span data-stu-id="6d6dc-153">0x00000004</span></span> | <span data-ttu-id="6d6dc-154">Un digitalizzatore di penna integrato viene usato per l'input.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-154">An integrated pen digitizer is used for input.</span></span>                                                                                                                                                |
| <span data-ttu-id="6d6dc-155">\_penna esterna \_ NID</span><span class="sxs-lookup"><span data-stu-id="6d6dc-155">NID\_EXTERNAL\_PEN</span></span>     | <span data-ttu-id="6d6dc-156">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6d6dc-156">0x00000008</span></span> | <span data-ttu-id="6d6dc-157">Per l'input viene usato un digitalizzatore di penna esterno.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-157">An external pen digitizer is used for input.</span></span>                                                                                                                                                  |
| <span data-ttu-id="6d6dc-158">\_ \_ input MULTIinput NID</span><span class="sxs-lookup"><span data-stu-id="6d6dc-158">NID\_MULTI\_INPUT</span></span>      | <span data-ttu-id="6d6dc-159">0x00000040</span><span class="sxs-lookup"><span data-stu-id="6d6dc-159">0x00000040</span></span> | <span data-ttu-id="6d6dc-160">Per l'input viene usato un digitalizzatore di input con supporto per più input.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-160">An input digitizer with support for multiple inputs is used for input.</span></span>                                                                                                                        |
| <span data-ttu-id="6d6dc-161">pronto per NID \_</span><span class="sxs-lookup"><span data-stu-id="6d6dc-161">NID\_READY</span></span>             | <span data-ttu-id="6d6dc-162">0x00000080</span><span class="sxs-lookup"><span data-stu-id="6d6dc-162">0x00000080</span></span> | <span data-ttu-id="6d6dc-163">Il digitalizzatore di input è pronto per l'input.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-163">The input digitizer is ready for input.</span></span> <span data-ttu-id="6d6dc-164">Se questo valore non è impostato, potrebbe significare che il servizio tablet è stato arrestato, che il digitalizzatore non è supportato o che i driver del digitalizzatore non sono stati installati.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-164">If this value is unset, it may mean that the tablet service is stopped, the digitizer is not supported, or digitizer drivers have not been installed.</span></span> |



 

<span data-ttu-id="6d6dc-165">Controllare i \_ \* valori NID è un modo utile per controllare le funzionalità del computer di un utente per configurare l'applicazione per il tocco, la penna o l'input non tablet.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-165">Checking the NID\_\* values is a useful way of checking the capabilities of a user's computer to configure your application for touch, pen, or non-tablet input.</span></span> <span data-ttu-id="6d6dc-166">Se, ad esempio, si dispone di un'interfaccia utente dinamica e si desidera configurarne automaticamente una parte, è possibile controllare il valore di NID \_ Integrated \_ touch, NID \_ multitouch e ottenere il numero massimo di tocchi la prima volta che un utente esegue l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-166">For example, if you have a dynamic user interface (UI) and want to automatically configure some of it, you could check for NID\_INTEGRATED\_TOUCH, NID\_MULTITOUCH, and could get the maximum number of touches the first time that a user runs your application.</span></span>

> [!Note]  
> <span data-ttu-id="6d6dc-167">Esistono alcune limitazioni intrinseche per \_ GetSystemMetrics SM.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-167">There are some inherent limitations for SM\_GETSYSTEMMETRICS.</span></span> <span data-ttu-id="6d6dc-168">Non è ad esempio disponibile il supporto per plug and Play.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-168">For example, there is no support for plug and play.</span></span> <span data-ttu-id="6d6dc-169">Per questo motivo, prestare attenzione quando si usa questa funzione come mezzo per la configurazione permanente.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-169">For this reason, use caution when using this function as a means for permanent configuration.</span></span>

 

## <a name="registering-to-receive-windows-touch-input"></a><span data-ttu-id="6d6dc-170">Registrazione per ricevere input Windows Touch</span><span class="sxs-lookup"><span data-stu-id="6d6dc-170">Registering to Receive Windows Touch Input</span></span>

<span data-ttu-id="6d6dc-171">Prima di ricevere input Windows Touch, le applicazioni devono prima registrarsi per ricevere input Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-171">Before receiving Windows Touch input, applications must first register to receive Windows Touch input.</span></span> <span data-ttu-id="6d6dc-172">Registrando la finestra dell'applicazione, l'applicazione indica che è compatibile con il tocco.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-172">By registering the application window, the application indicates that it is touch compatible.</span></span> <span data-ttu-id="6d6dc-173">Dopo che l'applicazione ha registrato la finestra, le notifiche dal driver Windows Touch vengono inviate all'applicazione quando viene eseguito l'input nella finestra.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-173">After the application registers its window, notifications from the Windows Touch driver are forwarded to the application when input is made on the window.</span></span> <span data-ttu-id="6d6dc-174">Quando l'applicazione viene arrestata, Annulla la registrazione della finestra per disabilitare le notifiche.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-174">When the application shuts down, it unregisters its window to disable notifications.</span></span>

> [!Note]  
> <span data-ttu-id="6d6dc-175">[**WM \_**](wm-touchdown.md) I messaggi touch sono attualmente "greedy".</span><span class="sxs-lookup"><span data-stu-id="6d6dc-175">[**WM\_TOUCH**](wm-touchdown.md) messages are currently "greedy."</span></span> <span data-ttu-id="6d6dc-176">Dopo la ricezione del primo messaggio tocco in una finestra, tutti i messaggi di tocco vengono inviati a tale finestra finché un'altra finestra non riceve lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-176">After the first touch message is received on a window, all touch messages are sent to that window until another window receives focus.</span></span>

 

> [!Note]  
> <span data-ttu-id="6d6dc-177">Per impostazione predefinita, si ricevono messaggi con [**\_ movimento WM**](wm-gesture.md) anziché messaggi [**WM \_ touch**](wm-touchdown.md) .</span><span class="sxs-lookup"><span data-stu-id="6d6dc-177">By default, you receive [**WM\_GESTURE**](wm-gesture.md) messages instead of [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span> <span data-ttu-id="6d6dc-178">Se si chiama [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), si smette di ricevere messaggi di **\_ movimento WM** .</span><span class="sxs-lookup"><span data-stu-id="6d6dc-178">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will stop receiving **WM\_GESTURE** messages.</span></span>

 

<span data-ttu-id="6d6dc-179">Nel codice seguente viene illustrata la registrazione di un'applicazione per la ricezione di messaggi Windows Touch in un'applicazione Win32.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-179">The following code demonstrates how an application could register to receive Windows Touch messages in a Win32 application.</span></span>


```C++
RegisterTouchWindow(hWnd, 0);
```



## <a name="handling-windows-touch-messages"></a><span data-ttu-id="6d6dc-180">Gestione dei messaggi di Windows Touch</span><span class="sxs-lookup"><span data-stu-id="6d6dc-180">Handling Windows Touch Messages</span></span>

<span data-ttu-id="6d6dc-181">È possibile gestire i messaggi di Windows Touch dalle applicazioni nei sistemi operativi Windows in molti modi.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-181">You can handle the Windows Touch messages from applications in Windows operating systems in many ways.</span></span> <span data-ttu-id="6d6dc-182">Se si sta programmando un'applicazione GUI, è necessario aggiungere codice all'interno della `WndProc` funzione per gestire i messaggi di interesse.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-182">If you are programming a GUI application, you add code within the `WndProc` function to handle the messages of interest.</span></span> <span data-ttu-id="6d6dc-183">Se si sta programmando un'applicazione Microsoft Foundation Class (MFC) o gestita, è necessario aggiungere gestori per i messaggi di interesse.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-183">If you are programming a Microsoft Foundation Class (MFC) or managed application, you add handlers for the messages of interest.</span></span> <span data-ttu-id="6d6dc-184">Nell'esempio di codice seguente viene illustrato il modo in cui i messaggi touch possono essere gestiti da WndProc in un'applicazione basata su Windows.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-184">The following code example shows how touch messages could be handled from WndProc in a Windows-based application.</span></span>


```C++
  LRESULT OnTouch(HWND hWnd, WPARAM wParam, LPARAM lParam ){
    BOOL bHandled = FALSE;
    UINT cInputs = LOWORD(wParam);
    PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
    if (pInputs){
        if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
            for (UINT i=0; i < cInputs; i++){
                TOUCHINPUT ti = pInputs[i];
                //do something with each touch input entry
            }            
            bHandled = TRUE;
        }else{
             /* handle the error here */
        }
        delete [] pInputs;
    }else{
        /* handle the error here, probably out of memory */
    }
    if (bHandled){
        // if you handled the message, close the touch input handle and return
        CloseTouchInputHandle((HTOUCHINPUT)lParam);
        return 0;
    }else{
        // if you didn't handle the message, let DefWindowProc handle it
        return DefWindowProc(hWnd, WM_TOUCH, wParam, lParam);
    }
  }


LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
      // pass touch messages to the touch handler 
      case WM_TOUCH:
        OnTouch(hWnd, wParam, lParam);
        break;
```





<span data-ttu-id="6d6dc-185">Nel codice seguente viene illustrato come è possibile implementare la mappa messaggi e un gestore di messaggi.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-185">The following code shows how you can implement the message map and a message handler.</span></span> <span data-ttu-id="6d6dc-186">Si noti che i messaggi devono essere dichiarati nella mappa messaggi, quindi il gestore per il messaggio deve essere implementato.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-186">Note that the messages must be declared in the message map and then the handler for the message should be implemented.</span></span> <span data-ttu-id="6d6dc-187">Ad esempio, in un'applicazione MFC questo può essere dichiarato nel codice della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-187">For example, in an MFC application, this could be declared in the dialog code.</span></span> <span data-ttu-id="6d6dc-188">Si noti inoltre che la `OnInitDialog` funzione per la finestra di dialogo deve includere una chiamata a [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) , ad esempio `RegisterTouchWindow(m_hWnd, 0)` .</span><span class="sxs-lookup"><span data-stu-id="6d6dc-188">Note also, that the `OnInitDialog` function for your dialog window would have to include a call to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) such as `RegisterTouchWindow(m_hWnd, 0)`.</span></span>


```C++
  // Class implementations within a dialog
  LRESULT TestDlg::OnTouch( WPARAM wParam, LPARAM lParam ){
    //Insert handler code here to do something with the message or uncomment the following line to test
    //MessageBox(L"touch!", L"touch!", MB_OK);
    return 0;
  }
  // The message map
  BEGIN_MESSAGE_MAP()
    ON_WM_CREATE()
    ... ... ...
    ON_MESSAGE(WM_TOUCH, OnTouch)
  END_MESSAGE_MAP()  
 
  BOOL TestDlg::OnInitDialog()
  {
    CDialog::OnInitDialog();    

    RegisterTouchWindow(m_hWnd, 0);
     ... ... ...
  }  
  
```



<span data-ttu-id="6d6dc-189">Se si tocca la finestra, si indicheranno i ritocchi da una finestra popup.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-189">Touching the window will indicate touches from a pop-up window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d6dc-190">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6d6dc-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d6dc-191">Input Windows Touch</span><span class="sxs-lookup"><span data-stu-id="6d6dc-191">Windows Touch Input</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

 