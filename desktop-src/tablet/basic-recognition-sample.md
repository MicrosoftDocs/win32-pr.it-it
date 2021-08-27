---
description: Questa applicazione illustra come creare una semplice applicazione di riconoscimento della grafia. Questo programma crea un oggetto InkCollector per abilitare l'input penna della finestra e un oggetto contesto del riconoscimento predefinito.
ms.assetid: 6dc94293-cdf7-4b90-a5e8-559f376add26
title: Esempio di riconoscimento di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf45aa7695866e1cf413ea42b7c377b07ea84984ecf2cc3f44da93ff868072d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111141"
---
# <a name="basic-recognition-sample"></a>Esempio di riconoscimento di base

Questa applicazione illustra come creare una semplice applicazione *di riconoscimento della grafia.*

Questo programma crea un [**oggetto InkCollector**](inkcollector-class.md) per abilitare *l'input penna* e un oggetto contesto *del riconoscimento* predefinito. Alla ricezione del messaggio "Recognize!" il comando , attivato dal menu dell'applicazione, i tratti input penna raccolti vengono passati al contesto del riconoscimento. La stringa di risultato migliore viene visualizzata in una finestra di messaggio.

## <a name="creating-the-recognizercontext-object"></a>Creazione dell'oggetto RecognizerContext

Nella procedura WndProc per l'applicazione, quando viene ricevuto il messaggio WM CREATE all'avvio, viene creato un nuovo contesto di riconoscimento che usa il sistema \_ di riconoscimento predefinito. Questo contesto viene usato per tutto il riconoscimento nell'applicazione.


```C++
case WM_CREATE:
{
    HRESULT hr;
    hr = CoCreateInstance(CLSID_InkRecognizerContext,
             NULL, CLSCTX_INPROC_SERVER, IID_IInkRecognizerContext,
             (void **) &g_pIInkRecoContext);
    if (FAILED(hr))
    {
        ::MessageBox(NULL, TEXT("There are no handwriting recognizers installed.\n"
            "You need to have at least one in order to run this sample.\nExiting."),
            gc_szAppName, MB_ICONERROR);
        return -1;
    }
  //...
```



## <a name="recognizing-the-strokes"></a>Riconoscimento dei tratti

Il comando recognize viene ricevuto quando l'utente fa clic su Recognize! . Il codice ottiene un puntatore a [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) (pIInkStrokes) dall'oggetto [**InkDisp**](inkdisp-class.md) e quindi passa **InkStrokes** al contesto del riconoscimento usando una chiamata a putref \_ Strokes.


```C++
 case WM_COMMAND:
  //...
  else if (wParam == ID_RECOGNIZE)
  {
      // change cursor to the system's Hourglass
      HCURSOR hCursor = ::SetCursor(::LoadCursor(NULL, IDC_WAIT));
      // Get a pointer to the ink stroke collection
      // This collection is a snapshot of the entire ink object
      IInkStrokes* pIInkStrokes = NULL;
      HRESULT hr = g_pIInkDisp->get_Strokes(&pIInkStrokes);
      if (SUCCEEDED(hr)) 
      {
          // Pass the stroke collection to the recognizer context
          hr = g_pIInkRecoContext->putref_Strokes(pIInkStrokes);
          if (SUCCEEDED(hr)) 
          {
```



Il codice chiama quindi il [**metodo Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) dell'oggetto [**InkRecognizerContext,**](inkrecognizercontext-class.md) passando un puntatore a [**un oggetto IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) per contenere i risultati.


```C++
              // Recognize
              IInkRecognitionResult* pIInkRecoResult = NULL;
              hr = g_pIInkRecoContext->Recognize(&pIInkRecoResult);
              if (SUCCEEDED(hr)) 
              {
```



Infine, il codice usa la proprietà [**TopString**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) dell'oggetto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) per recuperare il primo risultato del riconoscimento in una variabile stringa, rilascia l'oggetto **IInkRecognitionResult** e visualizza la stringa in una finestra di messaggio.


```C++
                  // Get the best result of the recognition 
                  BSTR bstrBestResult = NULL;
                  hr = pIInkRecoResult->get_TopString(&bstrBestResult);
                  pIInkRecoResult->Release();
                  pIInkRecoResult = NULL;

                  // Show the result string
                  if (SUCCEEDED(hr) && bstrBestResult)
                  {
                      MessageBoxW(hwnd, bstrBestResult, 
                                  L"Recognition Results", MB_OK);
                      SysFreeString(bstrBestResult);
                  }  }
        
```



Assicurarsi di reimpostare il contesto del riconoscimento tra gli utilizzi.


```
              // Reset the recognizer context
              g_pIInkRecoContext->putref_Strokes(NULL);
          }
          pIInkStrokes->Release();
      }
      // restore the cursor
      ::SetCursor(hCursor);
  }
```



 

 
