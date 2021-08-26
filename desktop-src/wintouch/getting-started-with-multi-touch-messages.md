---
title: Attività iniziali con Windows touch
description: Questa sezione illustra le attività associate al recupero Windows'input tocco per il funzionamento nell'applicazione.
ms.assetid: cd4e140e-a0b8-494f-82d9-bc0bfba55ecd
keywords:
- Windows Tocco, messaggi
- Windows Tocco, registrazione per l'input tocco
- Windows Tocco, test dei digitalizzatori di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d3f1daac2aacf8ac4c34ccbf9b1ab8be63058c45096e181c8b2eecf4f5d2de6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055901"
---
# <a name="getting-started-with-windows-touch-messages"></a>Attività iniziali con Windows touch

Questa sezione illustra le attività associate al recupero Windows'input tocco per il funzionamento nell'applicazione.

I passaggi seguenti vengono in genere eseguiti quando si lavora con Windows touch:

1.  Testare le funzionalità del digitalizzatore di input.
2.  Registrarsi per ricevere Windows Touch.
3.  Gestire i messaggi.

Il messaggio usato per l Windows Touch è [**WM \_ TOUCH.**](wm-touchdown.md) Questo messaggio indica i vari stati di contatto con un digitalizzatore.

## <a name="testing-the-capabilities-of-the-input-digitizer"></a>Test delle funzionalità del digitalizzatore di input

La [funzione GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) può essere usata per eseguire query sulle funzionalità del digitalizzatore di input passando il *valore nIndex* di SM **\_ DIGITIZER.** [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) restituisce un campo di bit che indica se il dispositivo è pronto, se il dispositivo supporta la penna o il tocco, se il dispositivo di input è integrato o esterno e se il dispositivo supporta più input (Windows Touch). La tabella seguente illustra i bit per i vari campi.



| bit   | 8           | 7           | 6        | 5        | 4            | 3              | 2              | 1                |
|-------|-------------|-------------|----------|----------|--------------|----------------|----------------|------------------|
| Valore | Pronto per lo stack | Multi-input | Riservato | Riservato | Penna esterna | Penna integrata | Tocco esterno | Tocco integrato |



 

Per testare il risultato del comando per una particolare funzionalità, è possibile usare l'operatore & bit per bit e il bit specifico che si sta testando. Ad esempio, per testare la Windows Touch, è necessario verificare che il bit del settimo ordine sia impostato (0x40 in formato esadecimale). Nell'esempio di codice seguente viene illustrato come testare questi valori.


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



La tabella seguente elenca le costanti definite in windows.h per testare le funzionalità di tocco del digitalizzatore di input.



| Nome                   | Valore      | Descrizione                                                                                                                                                                                   |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONFIGURAZIONE \_ TABLET \_ NONE   | 0x00000000 | Il digitalizzatore di input non ha funzionalità di tocco.                                                                                                                                         |
| NID \_ INTEGRATED \_ TOUCH | 0x00000001 | Per l'input viene usato un digitalizzatore tocco integrato.                                                                                                                                              |
| NID \_ EXTERNAL \_ TOUCH   | 0x00000002 | Per l'input viene usato un digitalizzatore tocco esterno.                                                                                                                                                |
| PENNA INTEGRATA \_ NID \_   | 0x00000004 | Per l'input viene usato un digitalizzatore di penna integrato.                                                                                                                                                |
| NID \_ EXTERNAL \_ PEN     | 0x00000008 | Per l'input viene usato un digitalizzatore di penna esterno.                                                                                                                                                  |
| NID \_ MULTI \_ INPUT      | 0x00000040 | Per l'input viene usato un digitalizzatore di input con supporto per più input.                                                                                                                        |
| NID \_ READY             | 0x00000080 | Il digitalizzatore di input è pronto per l'input. Se questo valore non è impostato, può significare che il servizio tablet è stato arrestato, che il digitalizzatore non è supportato o che i driver del digitalizzatore non sono stati installati. |



 

Il controllo dei valori NID è un modo utile per controllare le funzionalità del computer di un utente per configurare \_ \* l'applicazione per l'input tocco, penna o non tablet. Ad esempio, se si ha un'interfaccia utente dinamica e si vuole configurarla automaticamente, è possibile cercare NID \_ INTEGRATED \_ TOUCH, NID MULTITOUCH e ottenere il numero massimo di tocchi la prima volta che un utente esegue \_ l'applicazione.

> [!Note]  
> Esistono alcune limitazioni intrinseche per SM \_ GETSYSTEMMETRICS. Ad esempio, non è disponibile alcun supporto per Plug and Play. Per questo motivo, prestare attenzione quando si usa questa funzione come mezzo per la configurazione permanente.

 

## <a name="registering-to-receive-windows-touch-input"></a>Registrazione a Receive Windows Touch Input

Prima di ricevere Windows'input tocco, le applicazioni devono prima registrarsi per ricevere Windows input tocco. Registrando la finestra dell'applicazione, l'applicazione indica che è compatibile con il tocco. Dopo che l'applicazione ha registrato la finestra, le notifiche dal driver Windows Touch vengono inoltrate all'applicazione quando viene effettuato l'input nella finestra. Quando l'applicazione viene arrestata, annulla la registrazione della finestra per disabilitare le notifiche.

> [!Note]  
> [**WM \_ I**](wm-touchdown.md) messaggi TOUCH sono attualmente "greedy". Dopo la ricezione del primo messaggio di tocco in una finestra, tutti i messaggi di tocco vengono inviati a tale finestra fino a quando un'altra finestra non riceve lo stato attivo.

 

> [!Note]  
> Per impostazione predefinita, si ricevono [**messaggi WM \_ GESTURE**](wm-gesture.md) anziché [**messaggi WM \_ TOUCH.**](wm-touchdown.md) Se chiami [**RegisterTouchWindow,**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)interrompi la ricezione **di messaggi WM \_ GESTURE.**

 

Il codice seguente illustra come un'applicazione può registrarsi per ricevere Windows touch in un'applicazione Win32.


```C++
RegisterTouchWindow(hWnd, 0);
```



## <a name="handling-windows-touch-messages"></a>Gestione dei Windows touch

È possibile gestire i Windows Touch dalle applicazioni in Windows sistemi operativi in molti modi. Se si programma un'applicazione GUI, si aggiunge codice all'interno della `WndProc` funzione per gestire i messaggi di interesse. Se si programma un'applicazione gestita o Microsoft Foundation Class (MFC), si aggiungono gestori per i messaggi di interesse. Nell'esempio di codice seguente viene illustrato come gestire i messaggi di tocco da WndProc in un Windows basata su dispositivi.


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





Nel codice seguente viene illustrato come implementare la mappa messaggi e un gestore di messaggi. Si noti che i messaggi devono essere dichiarati nella mappa messaggi e quindi deve essere implementato il gestore per il messaggio. In un'applicazione MFC, ad esempio, questa operazione può essere dichiarata nel codice della finestra di dialogo. Si noti anche che la funzione per la finestra di dialogo deve `OnInitDialog` includere una chiamata a [**RegisterTouchWindow,**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) ad esempio `RegisterTouchWindow(m_hWnd, 0)` .


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



Toccare la finestra indicherà i tocchi da una finestra popup.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Input tocco](guide-multi-touch-input.md)
</dt> </dl>

 

 