---
description: "I metodi che è necessario implementare per creare un riconoscimento input penna vengono chiamati dalle API della piattaforma Tablet PC e non direttamente da un'applicazione abilitata per l'input penna. I passaggi seguenti rappresentano una sequenza di chiamata tipica per l'implementazione di questi metodi: la DLL viene caricata. Un&\\# 160; Viene creato l'handle HRECOGNIZER. Un&\\# 160; Viene creato l'handle HRECOCONTEXT. Le opzioni e le modalità di riconoscimento sono impostate per questo contesto. I tratti vengono aggiunti ai dati dell'input penna. L'input è terminato. L'input penna è riconosciuto. Vengono restituiti i risultati del riconoscimento. L'handle HRECOCONTEXT viene eliminato definitivamente. L'handle HRECOGNIZER viene eliminato definitivamente. La sequenza chiamante viene inoltre illustrata nel seguente contorno di codice: C + + CreateRecognizer (CLSID, &hrec); while (altre parti di input penna da riconoscere...) {//Creare un contesto, una volta per ogni pezzo di input penna da riconoscere HRC = CreateContext (hrec, &HRC);//funzioni per configurare opzioni e modalità per questa guida di contesto (HRC, pGuide, 0); SetFactoid (HRC, 5, telefono); solo se nell'applicazione con i flag dei form (HRC, RECOFLAG \\_ WORDMODE);//rare, solo se si desidera la modalità Word, no out-of-Dictionary o single Segmentation WordList (HRC, HWL);//aggiungendo tutti i tratti in questa porzione di input penna (altri tratti...) {AddStroke (HRC, NULL, 800, pPacket, pXForm);//una chiamata per Stroke} EndInkInput (HRC); Questa operazione ottiene il processo di riconoscimento dell'input penna (HRC); Se si tratta di un'applicazione semplice, questa viene chiamata per una semplice risposta GetBestResultString (HRC, length, buffer); Se si tratta di un'applicazione complessa, questa viene chiamata per una risposta completa GetLatticePtr (HRC, &pLattice); Eliminare il contesto DestroyContext (HRC); }//Chiamato immediatamente prima della chiusura dell'applicazione DestroyRecognizer (hrec);"
ms.assetid: 484ba140-788f-4b71-9cc7-9baa919d9936
title: Sequenza di chiamata tipica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832ea396c1d73748c4636d2cad5e17529b8d54df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313909"
---
# <a name="typical-calling-sequence"></a><span data-ttu-id="80c1a-103">Sequenza di chiamata tipica</span><span class="sxs-lookup"><span data-stu-id="80c1a-103">Typical Calling Sequence</span></span>

<span data-ttu-id="80c1a-104">I metodi che è necessario implementare per creare un riconoscimento input penna vengono chiamati dalle API della piattaforma Tablet PC e non direttamente da un'applicazione abilitata per l'input penna.</span><span class="sxs-lookup"><span data-stu-id="80c1a-104">The methods you must implement to create an ink recognizer are called by the Tablet PC Platform APIs and not directly by an ink-enabled application.</span></span>

<span data-ttu-id="80c1a-105">I passaggi seguenti rappresentano una sequenza di chiamata tipica per l'implementazione di questi metodi:</span><span class="sxs-lookup"><span data-stu-id="80c1a-105">The following steps represent a typical calling sequence for the implementation of these methods:</span></span>

1.  <span data-ttu-id="80c1a-106">La DLL viene caricata.</span><span class="sxs-lookup"><span data-stu-id="80c1a-106">The DLL is loaded.</span></span>
2.  <span data-ttu-id="80c1a-107">Viene creato un handle [HRECOGNIZER](hrecognizer-handle.md) .</span><span class="sxs-lookup"><span data-stu-id="80c1a-107">An [HRECOGNIZER](hrecognizer-handle.md) handle is created.</span></span>
3.  <span data-ttu-id="80c1a-108">Viene creato un handle [HRECOCONTEXT](hrecocontext-handle.md) .</span><span class="sxs-lookup"><span data-stu-id="80c1a-108">An [HRECOCONTEXT](hrecocontext-handle.md) handle is created.</span></span>
4.  <span data-ttu-id="80c1a-109">Le opzioni e le modalità di riconoscimento sono impostate per questo contesto.</span><span class="sxs-lookup"><span data-stu-id="80c1a-109">Recognizer options and modes are set for this context.</span></span>
5.  <span data-ttu-id="80c1a-110">I tratti vengono aggiunti ai dati dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="80c1a-110">Strokes are added to the ink data.</span></span>
6.  <span data-ttu-id="80c1a-111">L'input è terminato.</span><span class="sxs-lookup"><span data-stu-id="80c1a-111">Input is ended.</span></span>
7.  <span data-ttu-id="80c1a-112">L'input penna è riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="80c1a-112">The ink is recognized.</span></span>
8.  <span data-ttu-id="80c1a-113">Vengono restituiti i risultati del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="80c1a-113">The recognition results are returned.</span></span>
9.  <span data-ttu-id="80c1a-114">L'handle [HRECOCONTEXT](hrecocontext-handle.md) viene eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="80c1a-114">The [HRECOCONTEXT](hrecocontext-handle.md) handle is destroyed.</span></span>
10. <span data-ttu-id="80c1a-115">L'handle [HRECOGNIZER](hrecognizer-handle.md) viene eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="80c1a-115">The [HRECOGNIZER](hrecognizer-handle.md) handle is destroyed.</span></span>

<span data-ttu-id="80c1a-116">La sequenza chiamante viene inoltre illustrata nel seguente contorno di codice:</span><span class="sxs-lookup"><span data-stu-id="80c1a-116">The calling sequence is also illustrated in the following code outline:</span></span>


```C++
CreateRecognizer(CLSID, &hrec);
while (more pieces of ink to recognize ... )
{
  // Create a context, once per piece of ink to be recognized
  hrc = CreateContext(hrec, &hrc);

  // Functions to set up options and modes for this context
  SetGuide(hrc, pGuide, 0);
  SetFactoid(hrc, 5, PHONE); // only if in application with forms
  SetFlags(hrc, RECOFLAG_WORDMODE); // rare, only if wanting word mode, no out-of-dictionary, or single segmentation
  SetWordList(hrc, hwl);

  // Adding all the strokes in this piece of ink
  while (more strokes ... )
  {
    AddStroke(hrc, NULL, 800, pPacket, pXForm);  // one call per stroke
  }
  EndInkInput(hrc);

  // This gets the ink recognized
  Process(hrc);

  // If this is a simple application, it calls this for a simple answer
  GetBestResultString(hrc, length, buffer);

  // If this is a complex application, it calls this for a complete answer
  GetLatticePtr(hrc, &pLattice);

  // Destroy the context
  DestroyContext(hrc);
}
// Called just before the application shuts down
DestroyRecognizer(hrec);
```



## <a name="related-topics"></a><span data-ttu-id="80c1a-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="80c1a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80c1a-118">API di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="80c1a-118">Recognizer APIs</span></span>](recognizer-apis.md)
</dt> <dt>

[<span data-ttu-id="80c1a-119">Architettura dell'API di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="80c1a-119">Recognition API Architecture</span></span>](recognition-api-architecture.md)
</dt> </dl>

 

 



