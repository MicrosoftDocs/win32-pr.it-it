---
title: Evento RequestComplete
description: Evento RequestComplete
ms.assetid: 543b79d1-f09d-4061-a1a8-8c8ab496bceb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5202cc6aee6e8727651279fd216d5f0e5676025584c9cb66c4c6ad958da54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746558"
---
# <a name="requestcomplete-event"></a>Evento RequestComplete

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando il server completa una richiesta in coda.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *agent*** \_ RequestComplete* *  **(ByVal** *Request***)**



| Parte      | Descrizione                                            |
|-----------|--------------------------------------------------------|
| *Richiesta* | Restituisce [**l'oggetto Request.**](/windows/desktop/lwef/the-request-object) |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Questo evento restituisce un [**oggetto Request.**](/windows/desktop/lwef/the-request-object) Poiché le richieste vengono elaborate in modo asincrono, è possibile usare questo evento per determinare quando il server completa l'elaborazione di una richiesta (ad esempio un metodo [**Get,**](get-method.md) [**Play**](play-method.md)o [**Speak)**](speak-method.md) per sincronizzare questo evento con altre azioni generate dall'applicazione. Il server invia l'evento solo al client che ha creato il riferimento all'oggetto **Request** e solo se è stata definita una variabile globale per il riferimento alla richiesta:


```
   Dim MyRequest 
   Dim Genie 

   Sub window_Onload
   
   Agent1.Characters.Load "Genie","https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent.Characters("Genie")

   ' This syntax will generate RequestStart and RequestComplete events.
   Set MyRequest = Genie.Get("state", "Showing")
   ' This syntax will not generate RequestStart and RequestComplete events.
   Genie.Get "state", "Hiding"
   
   End Sub

   Sub Agent1_RequestComplete(ByVal Request)

   If Request = MyRequest Then
      Status = "Showing animation is now loaded"

   End Sub
```



Poiché gli [**oggetti Request**](/windows/desktop/lwef/the-request-object) dell'animazione non vengono assegnati fino a quando il server non elabora la richiesta, assicurarsi che l'oggetto **Request** esista prima di provare a valutarlo. Ad esempio, in Visual Basic, se si usa un'istruzione condizionale per verificare se una richiesta specifica è stata completata, è possibile usare la **parola chiave Nothing:**


```
   Sub Agent1_RequestComplete (ByVal Request)

   If Not (MyRequest Is Nothing) Then
      If Request = MyRequest Then
      '-- Do whatever
      End If
   End If

   End Sub
```



> [!Note]  
> In VBScript 1.0 questo evento viene generato anche se non si definiscono riferimenti a un [**oggetto Request.**](/windows/desktop/lwef/the-request-object) Questo problema è stato risolto in VBScript 2.0, che può essere scaricato da <https://microsoft.com/msdownload/vbscript/scripting.asp> .

 

### <a name="see-also"></a>Vedere anche

[**Evento RequestStart**](requeststart-event.md)


 

 