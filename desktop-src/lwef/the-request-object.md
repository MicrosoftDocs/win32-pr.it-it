---
title: Oggetto Request
description: Oggetto Request
ms.assetid: d8b37164-6855-48c0-bcf8-a86c0f8b3a59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2bc9ecf65403ca6dbb471c81a65b105bcc5b69701760a73f8fbc8a5684a9b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117882394"
---
# <a name="the-request-object"></a>Oggetto Request

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il server elabora alcuni metodi in modo asincrono. In questo modo il codice dell'applicazione può continuare mentre il metodo è in corso di completamento. Quando un'applicazione client chiama uno di questi metodi, il controllo crea e restituisce un [**oggetto Request**](/windows/desktop/lwef/the-request-object) per la richiesta. È possibile usare **l'oggetto Request** per tenere traccia dello stato del metodo assegnando una variabile oggetto al metodo . In Visual Basic dichiarare prima una variabile oggetto:


```
   Dim MyRequest as Object
```



In VBScript non si include il tipo di variabile nella dichiarazione:


```
   Dim MyRequest
```



Usare quindi Visual Basic'istruzione Set di per assegnare la variabile alla chiamata al metodo:


```
   Set MyRequest = <i>agent</i>.Characters("<i>CharacterID</i>").<i>method</i> (<i>parameter</i>[s])
```



Verrà aggiunto un riferimento [**all'oggetto**](/windows/desktop/lwef/the-request-object) Request. **L'oggetto** Request verrà eliminato quando non vi sono altri riferimenti. La posizione in cui si **dichiara l'oggetto Request** e il modo in cui lo si usa ne determina la durata. Se l'oggetto viene dichiarato locale in una subroutine o funzione, verrà eliminato quando esce dall'ambito; ad esempio quando termina la subroutine o la funzione. Se l'oggetto viene dichiarato a livello globale, non verrà eliminato fino a quando il programma non termina o non viene assegnato un nuovo valore (o un valore impostato su "vuoto") all'oggetto.

[**L'oggetto Request**](/windows/desktop/lwef/the-request-object) fornisce diverse proprietà su cui è possibile eseguire query. Ad esempio, la [**proprietà Status**](status-property.md) restituisce lo stato corrente della richiesta. È possibile usare questa proprietà per controllare lo stato della richiesta:


```
   Dim MyRequest
   
   Set MyRequest = Agent1.Characters.Load ("Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf")

   If (MyRequest.Status = 2) then
      'do something

   Else If (MyRequest.Status = 0) then
      'do something right away

   End If
```



La [**proprietà Status**](status-property.md) restituisce lo stato di un oggetto [**Request**](/windows/desktop/lwef/the-request-object) come valore Long Integer.



| Stato | Definizione                                        |
|--------|---------------------------------------------------|
| 0      | Richiesta completata.                   |
| 1      | Richiesta non riuscita.                                   |
| 2      | Richiesta in sospeso (nella coda, ma non completata). |
| 3      | Richiesta interrotta.                              |
| 4      | Richiesta in corso.                              |



 

[**L'oggetto Request**](/windows/desktop/lwef/the-request-object) include anche un valore Long Integer nella [**proprietà Number**](https://www.bing.com/search?q=**Number**) che restituisce l'errore o la causa del [**codice di**](status-property.md) stato. Se none, questo valore è zero (0). La [**proprietà Description**](description-property.md) contiene un valore stringa che corrisponde al numero di errore. Se la stringa non esiste, **Description** contiene "Errore definito dall'applicazione o definito dall'oggetto".

Per i valori e il significato restituiti dalla [**proprietà Number,**](https://www.bing.com/search?q=**Number**) vedere [Codici di errore.](microsoft-agent-error-codes.md)

Il server inserisce le richieste di animazione nella coda del carattere specificato. In questo modo il server può riprodurre l'animazione in un thread separato e il codice dell'applicazione può continuare mentre le animazioni vengono riprodotte. Se si crea un riferimento all'oggetto [**Request,**](/windows/desktop/lwef/the-request-object) il server invia automaticamente una notifica all'utente quando una richiesta di animazione è stata avviata o completata tramite gli [**eventi RequestStart**](https://www.bing.com/search?q=**RequestStart**) e [**RequestComplete.**](https://www.bing.com/search?q=**RequestComplete**) Poiché i metodi che **restituiscono oggetti Request** sono asincroni e potrebbero non essere completati durante l'ambito della funzione chiamante, dichiarare il riferimento all'oggetto **Request** a livello globale.

Per restituire un oggetto Request, è possibile usare i metodi seguenti: [**GestureAt**](gestureat-method.md), [**Get**](get-method.md), [**Hide**](hide-method.md), [**Interrupt**](interrupt-method.md), [**Load**](load-method.md), [**MoveTo**](moveto-method.md) [](/windows/desktop/lwef/the-request-object) , [**Play**](play-method.md), [**Show**](show-method.md), [**Speak**](speak-method.md)e [**Wait**](https://www.bing.com/search?q=**Wait**).

 

 