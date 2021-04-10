---
description: Questa applicazione illustra come creare una semplice applicazione di riconoscimento della grafia. Questo programma crea un oggetto InkCollector per abilitare l'input penna per la finestra e un oggetto contesto di riconoscimento predefinito.
ms.assetid: 6dc94293-cdf7-4b90-a5e8-559f376add26
title: Esempio di riconoscimento di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19679a6d1642a94ed813ba0428654b6e03009ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884382"
---
# <a name="basic-recognition-sample"></a>Esempio di riconoscimento di base

Questa applicazione illustra come creare una semplice applicazione di riconoscimento della *grafia* .

Questo programma crea un oggetto [**InkCollector**](inkcollector-class.md) per abilitare l' *input penna* per la finestra e un oggetto *contesto di riconoscimento* predefinito. Alla ricezione di "Recognize!" , generato dal menu dell'applicazione, i tratti di input penna raccolti vengono passati al contesto del riconoscimento. La stringa di risultato migliore viene visualizzata in una finestra di messaggio.

## <a name="creating-the-recognizercontext-object"></a>Creazione dell'oggetto RecognizerContext

Nella procedura WndProc per l'applicazione, quando viene ricevuto il \_ messaggio WM create all'avvio, viene creato un nuovo contesto di riconoscimento che usa il riconoscimento predefinito. Questo contesto viene utilizzato per tutti i riconoscimenti nell'applicazione.


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

Il comando Recognize viene ricevuto quando l'utente fa clic su Recognize! . Il codice ottiene un puntatore al [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) input penna (pIInkStrokes) dall'oggetto [**InkDisp**](inkdisp-class.md) e quindi passa il **InkStrokes** al contesto del riconoscimento utilizzando una chiamata a putref \_ Strokes.


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



Il codice chiama quindi il metodo [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) dell'oggetto [**InkRecognizerContext**](inkrecognizercontext-class.md) , passando un puntatore a un oggetto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) per conservare i risultati.


```C++
              // Recognize
              IInkRecognitionResult* pIInkRecoResult = NULL;
              hr = g_pIInkRecoContext->Recognize(&pIInkRecoResult);
              if (SUCCEEDED(hr)) 
              {
```



Infine, il codice utilizza la proprietà [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) dell'oggetto IInkRecognitionResult per recuperare il risultato del riconoscimento principale in una [**variabile di stringa**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) , rilascia l'oggetto  e visualizza la stringa in una finestra di messaggio.


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



Assicurarsi di reimpostare il contesto di riconoscimento tra gli utilizzi.


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



 

 
