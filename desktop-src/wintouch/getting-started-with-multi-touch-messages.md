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
# <a name="getting-started-with-windows-touch-messages"></a>Introduzione con i messaggi di Windows Touch

In questa sezione vengono illustrate le attività associate all'acquisizione di un input di Windows Touch per il funzionamento dell'applicazione.

I passaggi seguenti vengono in genere eseguiti quando si utilizzano i messaggi di Windows Touch:

1.  Testare le funzionalità del digitalizzatore di input.
2.  Registrarsi per ricevere messaggi Windows Touch.
3.  Gestire i messaggi.

Il messaggio utilizzato per Windows Touch è [**WM \_ touch**](wm-touchdown.md). Questo messaggio indica i vari Stati del contatto con un digitalizzatore.

## <a name="testing-the-capabilities-of-the-input-digitizer"></a>Test delle funzionalità del digitalizzatore di input

La funzione [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) può essere usata per eseguire query sulle funzionalità del digitalizzatore di input passando il valore *nIndex* del **\_ digitalizzatore SM**. [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) restituisce un campo di bit che indica se il dispositivo è pronto, se il dispositivo supporta la penna o il tocco, se il dispositivo di input è integrato o esterno e se il dispositivo supporta più input (Windows Touch). La tabella seguente illustra i bit per i vari campi.



| bit   | 8           | 7           | 6        | 5        | 4            | 3              | 2              | 1                |
|-------|-------------|-------------|----------|----------|--------------|----------------|----------------|------------------|
| Valore | Pronto per lo stack | Multiinput | Riservato | Riservato | Penna esterna | Penna integrata | Tocco esterno | Tocco integrato |



 

Per testare il risultato del comando per una particolare funzionalità, è possibile usare l'operatore di & bit per bit e il bit particolare che si sta testando. Ad esempio, per testare Windows Touch, verificare che sia impostato il bit del settimo ordine (0x40 in hex). Nell'esempio di codice seguente viene illustrato come testare questi valori.


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



Nella tabella seguente sono elencate le costanti definite in Windows. h per il test delle funzionalità di tocco del digitalizzatore di input.



| Nome                   | Valore      | Descrizione                                                                                                                                                                                   |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| configurazione del TABLET \_ \_ None   | 0x00000000 | Il digitalizzatore di input non dispone di funzionalità di tocco.                                                                                                                                         |
| \_tocco integrato \_ NID | 0x00000001 | Un digitalizzatore Touch integrato viene usato per l'input.                                                                                                                                              |
| \_tocco esterno \_ NID   | 0x00000002 | Per l'input viene usato un digitalizzatore Touch esterno.                                                                                                                                                |
| \_penna integrata \_ NID   | 0x00000004 | Un digitalizzatore di penna integrato viene usato per l'input.                                                                                                                                                |
| \_penna esterna \_ NID     | 0x00000008 | Per l'input viene usato un digitalizzatore di penna esterno.                                                                                                                                                  |
| \_ \_ input MULTIinput NID      | 0x00000040 | Per l'input viene usato un digitalizzatore di input con supporto per più input.                                                                                                                        |
| pronto per NID \_             | 0x00000080 | Il digitalizzatore di input è pronto per l'input. Se questo valore non è impostato, potrebbe significare che il servizio tablet è stato arrestato, che il digitalizzatore non è supportato o che i driver del digitalizzatore non sono stati installati. |



 

Controllare i \_ \* valori NID è un modo utile per controllare le funzionalità del computer di un utente per configurare l'applicazione per il tocco, la penna o l'input non tablet. Se, ad esempio, si dispone di un'interfaccia utente dinamica e si desidera configurarne automaticamente una parte, è possibile controllare il valore di NID \_ Integrated \_ touch, NID \_ multitouch e ottenere il numero massimo di tocchi la prima volta che un utente esegue l'applicazione.

> [!Note]  
> Esistono alcune limitazioni intrinseche per \_ GetSystemMetrics SM. Non è ad esempio disponibile il supporto per plug and Play. Per questo motivo, prestare attenzione quando si usa questa funzione come mezzo per la configurazione permanente.

 

## <a name="registering-to-receive-windows-touch-input"></a>Registrazione per ricevere input Windows Touch

Prima di ricevere input Windows Touch, le applicazioni devono prima registrarsi per ricevere input Windows Touch. Registrando la finestra dell'applicazione, l'applicazione indica che è compatibile con il tocco. Dopo che l'applicazione ha registrato la finestra, le notifiche dal driver Windows Touch vengono inviate all'applicazione quando viene eseguito l'input nella finestra. Quando l'applicazione viene arrestata, Annulla la registrazione della finestra per disabilitare le notifiche.

> [!Note]  
> [**WM \_**](wm-touchdown.md) I messaggi touch sono attualmente "greedy". Dopo la ricezione del primo messaggio tocco in una finestra, tutti i messaggi di tocco vengono inviati a tale finestra finché un'altra finestra non riceve lo stato attivo.

 

> [!Note]  
> Per impostazione predefinita, si ricevono messaggi con [**\_ movimento WM**](wm-gesture.md) anziché messaggi [**WM \_ touch**](wm-touchdown.md) . Se si chiama [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), si smette di ricevere messaggi di **\_ movimento WM** .

 

Nel codice seguente viene illustrata la registrazione di un'applicazione per la ricezione di messaggi Windows Touch in un'applicazione Win32.


```C++
RegisterTouchWindow(hWnd, 0);
```



## <a name="handling-windows-touch-messages"></a>Gestione dei messaggi di Windows Touch

È possibile gestire i messaggi di Windows Touch dalle applicazioni nei sistemi operativi Windows in molti modi. Se si sta programmando un'applicazione GUI, è necessario aggiungere codice all'interno della `WndProc` funzione per gestire i messaggi di interesse. Se si sta programmando un'applicazione Microsoft Foundation Class (MFC) o gestita, è necessario aggiungere gestori per i messaggi di interesse. Nell'esempio di codice seguente viene illustrato il modo in cui i messaggi touch possono essere gestiti da WndProc in un'applicazione basata su Windows.


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





Nel codice seguente viene illustrato come è possibile implementare la mappa messaggi e un gestore di messaggi. Si noti che i messaggi devono essere dichiarati nella mappa messaggi, quindi il gestore per il messaggio deve essere implementato. Ad esempio, in un'applicazione MFC questo può essere dichiarato nel codice della finestra di dialogo. Si noti inoltre che la `OnInitDialog` funzione per la finestra di dialogo deve includere una chiamata a [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) , ad esempio `RegisterTouchWindow(m_hWnd, 0)` .


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



Se si tocca la finestra, si indicheranno i ritocchi da una finestra popup.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Input Windows Touch](guide-multi-touch-input.md)
</dt> </dl>

 

 