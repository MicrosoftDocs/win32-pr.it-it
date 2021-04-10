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
# <a name="basic-recognition-sample"></a><span data-ttu-id="61e2c-103">Esempio di riconoscimento di base</span><span class="sxs-lookup"><span data-stu-id="61e2c-103">Basic Recognition Sample</span></span>

<span data-ttu-id="61e2c-104">Questa applicazione illustra come creare una semplice applicazione di riconoscimento della *grafia* .</span><span class="sxs-lookup"><span data-stu-id="61e2c-104">This application demonstrates how you can build a simple *handwriting* recognition application.</span></span>

<span data-ttu-id="61e2c-105">Questo programma crea un oggetto [**InkCollector**](inkcollector-class.md) per abilitare l' *input penna* per la finestra e un oggetto *contesto di riconoscimento* predefinito.</span><span class="sxs-lookup"><span data-stu-id="61e2c-105">This program creates an [**InkCollector**](inkcollector-class.md) object to *ink*-enable the window and a default *recognizer context* object.</span></span> <span data-ttu-id="61e2c-106">Alla ricezione di "Recognize!"</span><span class="sxs-lookup"><span data-stu-id="61e2c-106">Upon receiving the "Recognize!"</span></span> <span data-ttu-id="61e2c-107">, generato dal menu dell'applicazione, i tratti di input penna raccolti vengono passati al contesto del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="61e2c-107">command, fired from the application's menu, the collected ink strokes are passed to the recognizer context.</span></span> <span data-ttu-id="61e2c-108">La stringa di risultato migliore viene visualizzata in una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="61e2c-108">The best result string is presented in a message box.</span></span>

## <a name="creating-the-recognizercontext-object"></a><span data-ttu-id="61e2c-109">Creazione dell'oggetto RecognizerContext</span><span class="sxs-lookup"><span data-stu-id="61e2c-109">Creating the RecognizerContext Object</span></span>

<span data-ttu-id="61e2c-110">Nella procedura WndProc per l'applicazione, quando viene ricevuto il \_ messaggio WM create all'avvio, viene creato un nuovo contesto di riconoscimento che usa il riconoscimento predefinito.</span><span class="sxs-lookup"><span data-stu-id="61e2c-110">In the WndProc procedure for the application, when the WM\_CREATE message is received on startup, a new recognizer context that uses the default recognizer is created.</span></span> <span data-ttu-id="61e2c-111">Questo contesto viene utilizzato per tutti i riconoscimenti nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="61e2c-111">This context is used for all recognition in the application.</span></span>


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



## <a name="recognizing-the-strokes"></a><span data-ttu-id="61e2c-112">Riconoscimento dei tratti</span><span class="sxs-lookup"><span data-stu-id="61e2c-112">Recognizing the Strokes</span></span>

<span data-ttu-id="61e2c-113">Il comando Recognize viene ricevuto quando l'utente fa clic su Recognize!</span><span class="sxs-lookup"><span data-stu-id="61e2c-113">The recognize command is received when the user clicks the Recognize!</span></span> <span data-ttu-id="61e2c-114">.</span><span class="sxs-lookup"><span data-stu-id="61e2c-114">menu item.</span></span> <span data-ttu-id="61e2c-115">Il codice ottiene un puntatore al [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) input penna (pIInkStrokes) dall'oggetto [**InkDisp**](inkdisp-class.md) e quindi passa il **InkStrokes** al contesto del riconoscimento utilizzando una chiamata a putref \_ Strokes.</span><span class="sxs-lookup"><span data-stu-id="61e2c-115">The code gets a pointer to the ink [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) (pIInkStrokes) off of the [**InkDisp**](inkdisp-class.md) object, and then passes the **InkStrokes** to the recognizer context using a call to putref\_Strokes.</span></span>


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



<span data-ttu-id="61e2c-116">Il codice chiama quindi il metodo [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) dell'oggetto [**InkRecognizerContext**](inkrecognizercontext-class.md) , passando un puntatore a un oggetto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) per conservare i risultati.</span><span class="sxs-lookup"><span data-stu-id="61e2c-116">The code then calls the [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) method of the [**InkRecognizerContext**](inkrecognizercontext-class.md) object, passing in a pointer to an [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object to hold the results.</span></span>


```C++
              // Recognize
              IInkRecognitionResult* pIInkRecoResult = NULL;
              hr = g_pIInkRecoContext->Recognize(&pIInkRecoResult);
              if (SUCCEEDED(hr)) 
              {
```



<span data-ttu-id="61e2c-117">Infine, il codice utilizza la proprietà [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) dell'oggetto IInkRecognitionResult per recuperare il risultato del riconoscimento principale in una [**variabile di stringa**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) , rilascia l'oggetto  e visualizza la stringa in una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="61e2c-117">Finally, the code uses the [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object's [**TopString**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) property retrieve the top recognition result into a string variable, releases the **IInkRecognitionResult** object, and displays the string in a message box.</span></span>


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



<span data-ttu-id="61e2c-118">Assicurarsi di reimpostare il contesto di riconoscimento tra gli utilizzi.</span><span class="sxs-lookup"><span data-stu-id="61e2c-118">Be sure to reset the recognizer context between usages.</span></span>


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



 

 
