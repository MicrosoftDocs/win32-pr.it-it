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
# <a name="typical-calling-sequence"></a>Sequenza di chiamata tipica

I metodi che è necessario implementare per creare un riconoscimento input penna vengono chiamati dalle API della piattaforma Tablet PC e non direttamente da un'applicazione abilitata per l'input penna.

I passaggi seguenti rappresentano una sequenza di chiamata tipica per l'implementazione di questi metodi:

1.  La DLL viene caricata.
2.  Viene creato un handle [HRECOGNIZER](hrecognizer-handle.md) .
3.  Viene creato un handle [HRECOCONTEXT](hrecocontext-handle.md) .
4.  Le opzioni e le modalità di riconoscimento sono impostate per questo contesto.
5.  I tratti vengono aggiunti ai dati dell'input penna.
6.  L'input è terminato.
7.  L'input penna è riconosciuto.
8.  Vengono restituiti i risultati del riconoscimento.
9.  L'handle [HRECOCONTEXT](hrecocontext-handle.md) viene eliminato definitivamente.
10. L'handle [HRECOGNIZER](hrecognizer-handle.md) viene eliminato definitivamente.

La sequenza chiamante viene inoltre illustrata nel seguente contorno di codice:


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API di riconoscimento](recognizer-apis.md)
</dt> <dt>

[Architettura dell'API di riconoscimento](recognition-api-architecture.md)
</dt> </dl>

 

 



