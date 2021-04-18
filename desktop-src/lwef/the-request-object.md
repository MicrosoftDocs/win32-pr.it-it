---
title: Oggetto Request
description: Oggetto Request
ms.assetid: d8b37164-6855-48c0-bcf8-a86c0f8b3a59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a50d554a5799af9a434b456113d7c826d2a0aa2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299648"
---
# <a name="the-request-object"></a>Oggetto Request

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il server elabora alcuni metodi in modo asincrono. Ciò consente al codice dell'applicazione di continuare mentre è in corso il completamento del metodo. Quando un'applicazione client chiama uno di questi metodi, il controllo Crea e restituisce un oggetto [**Request**](/windows/desktop/lwef/the-request-object) per la richiesta. È possibile usare l'oggetto **Request** per tenere traccia dello stato del metodo assegnando una variabile oggetto al metodo. In Visual Basic dichiarare prima una variabile oggetto:


```
   Dim MyRequest as Object
```



In VBScript non è incluso il tipo di variabile nella dichiarazione:


```
   Dim MyRequest
```



Usare l'istruzione set di Visual Basic per assegnare la variabile alla chiamata al metodo:


```
   Set MyRequest = <i>agent</i>.Characters("<i>CharacterID</i>").<i>method</i> (<i>parameter</i>[s])
```



Viene aggiunto un riferimento all'oggetto [**Request**](/windows/desktop/lwef/the-request-object) . L'oggetto **richiesta** verrà eliminato definitivamente quando non vi sono altri riferimenti. La posizione in cui si dichiara l'oggetto **richiesta** e la relativa modalità di utilizzo determina la relativa durata. Se l'oggetto è dichiarato localmente a una subroutine o a una funzione, viene eliminato definitivamente quando esce dall'ambito. ovvero, al termine della subroutine o della funzione. Se l'oggetto viene dichiarato a livello globale, non verrà eliminato definitivamente fino a quando il programma non termina o un nuovo valore (o un valore impostato su "Empty") viene assegnato all'oggetto.

L'oggetto [**Request**](/windows/desktop/lwef/the-request-object) fornisce diverse proprietà su cui è possibile eseguire una query. Ad esempio, la proprietà [**status**](status-property.md) restituisce lo stato corrente della richiesta. È possibile usare questa proprietà per verificare lo stato della richiesta:


```
   Dim MyRequest
   
   Set MyRequest = Agent1.Characters.Load ("Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf")

   If (MyRequest.Status = 2) then
      'do something

   Else If (MyRequest.Status = 0) then
      'do something right away

   End If
```



La proprietà [**status**](status-property.md) restituisce lo stato di un oggetto [**Request**](/windows/desktop/lwef/the-request-object) come valore long integer.



| Stato | Definizione                                        |
|--------|---------------------------------------------------|
| 0      | La richiesta è stata completata.                   |
| 1      | Richiesta non riuscita.                                   |
| 2      | Richiesta in sospeso (nella coda, ma non completata). |
| 3      | Richiesta interrotta.                              |
| 4      | Richiesta in corso.                              |



 

L'oggetto [**Request**](/windows/desktop/lwef/the-request-object) include anche un valore long integer nella proprietà [**Number**](https://www.bing.com/search?q=**Number**) che restituisce l'errore [**o la sua**](status-property.md) origine. Se None, questo valore è zero (0). La proprietà [**Description**](description-property.md) contiene un valore stringa corrispondente al numero di errore. Se la stringa non esiste, la **Descrizione** contiene "errore definito dall'applicazione o definito dall'oggetto".

Per i valori e il significato restituiti dalla proprietà [**Number**](https://www.bing.com/search?q=**Number**) , vedere [codici di errore](microsoft-agent-error-codes.md).

Il server inserisce le richieste di animazione nella coda del carattere specificato. Ciò consente al server di riprodurre l'animazione in un thread separato e il codice dell'applicazione può continuare mentre le animazioni vengono riprodotte. Se si crea un riferimento a un oggetto [**richiesta**](/windows/desktop/lwef/the-request-object) , il server invia automaticamente una notifica quando una richiesta di animazione viene avviata o completata tramite gli eventi [**RequestStart**](https://www.bing.com/search?q=**RequestStart**) e [**RequestComplete**](https://www.bing.com/search?q=**RequestComplete**) . Poiché i metodi che restituiscono oggetti **richiesta** sono asincroni e potrebbero non essere completati durante l'ambito della funzione chiamante, dichiarare il riferimento all'oggetto **Request** a livello globale.

Per restituire un oggetto [**Request**](/windows/desktop/lwef/the-request-object) , è possibile usare i metodi seguenti: [**GestureAt**](gestureat-method.md), [**Get**](get-method.md), [**Hide**](hide-method.md), [**interrupt**](interrupt-method.md), [**Load**](load-method.md), [**MoveTo**](moveto-method.md), [**Play**](play-method.md), [**show**](show-method.md), [**Speak**](speak-method.md)e [**wait**](https://www.bing.com/search?q=**Wait**).

 

 