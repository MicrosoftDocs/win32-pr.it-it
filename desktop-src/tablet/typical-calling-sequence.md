---
description: "I metodi che è necessario implementare per creare un riconoscimento input penna vengono chiamati dalle API della piattaforma Tablet PC e non direttamente da un'applicazione abilitata per l'input penna. I passaggi seguenti rappresentano una sequenza di chiamata tipica per l'implementazione di questi metodi: viene caricata la DLL. Un&\\# 160; Viene creato l'handle HRECOGNIZER. Un&\\# 160; Viene creato l'handle HRECOCONTEXT. Le opzioni e le modalità del riconoscitore sono impostate per questo contesto. I tratti vengono aggiunti ai dati dell'input penna. L'input è terminato. L'input penna viene riconosciuto. Vengono restituiti i risultati del riconoscimento. L'handle HRECOCONTEXT viene eliminato. L'handle HRECOGNIZER viene eliminato. La sequenza di chiamata è illustrata anche nella struttura di codice seguente: C++CreateRecognizer(CLSID, &hrec); while (più parti dell'input penna da riconoscere ... ) { // Creare un contesto, una volta per ogni input penna da riconoscere hrc = CreateContext(hrec, &hrc); // Funzioni per configurare opzioni e modalità per questo contesto SetGuide(hrc, pGuide, 0); SetFactoid(hrc, 5, PHONE); solo se nell'applicazione con form SetFlags(hrc, RECOFLAG WORDMODE); // rare, solo se si vuole la modalità parola, senza dizionario o setWordList a segmentazione \\_ singola(hrc, hwl); // Aggiunta di tutti i tratti in questa parte dell'input penna mentre (altri tratti ... ) { AddStroke(hrc, NULL, 800, pPacket, pXForm); // una chiamata per tratto } EndInkInput(hrc); Ottiene l'oggetto Process(hrc) riconosciuto dall'input penna. Se si tratta di un'applicazione semplice, viene chiamata per una risposta semplice GetBestResultString(hrc, length, buffer); Se si tratta di un'applicazione complessa, chiama per ottenere una risposta completa GetLatticePtr(hrc, &pLattice); Eliminare il contesto DestroyContext(hrc); } // Chiamato subito prima dell'arresto dell'applicazione DestroyRecognizer(hrec);"
ms.assetid: 484ba140-788f-4b71-9cc7-9baa919d9936
title: Sequenza di chiamata tipica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94506d320d2ac0dca31fcc44714d0fd9ed089a2dda479020d860b0fbe5bfae5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708221"
---
# <a name="typical-calling-sequence"></a>Sequenza di chiamata tipica

I metodi che è necessario implementare per creare un riconoscimento input penna vengono chiamati dalle API della piattaforma Tablet PC e non direttamente da un'applicazione abilitata per l'input penna.

I passaggi seguenti rappresentano una sequenza di chiamata tipica per l'implementazione di questi metodi:

1.  La DLL viene caricata.
2.  Viene creato un handle [HRECOGNIZER.](hrecognizer-handle.md)
3.  Viene creato un handle [HRECOCONTEXT.](hrecocontext-handle.md)
4.  Le opzioni e le modalità del riconoscitore sono impostate per questo contesto.
5.  I tratti vengono aggiunti ai dati dell'input penna.
6.  L'input è terminato.
7.  L'input penna viene riconosciuto.
8.  Vengono restituiti i risultati del riconoscimento.
9.  [L'handle HRECOCONTEXT](hrecocontext-handle.md) viene eliminato.
10. [L'handle HRECOGNIZER](hrecognizer-handle.md) viene eliminato.

La sequenza di chiamata è illustrata anche nella struttura del codice seguente:


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

 

 



