---
title: Evento RequestStart
description: Evento RequestStart
ms.assetid: ecfb9691-cbc4-48f5-8e26-a99389e85eed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2be5954636084d3cbc299c718f2b4e6d9330ef90
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727026"
---
# <a name="requeststart-event"></a>Evento RequestStart

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando il server inizia una richiesta in coda.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

Agente **secondario** ** * * \_ RequestStart* *  **(richiesta ByVal** ** * *)**



| Parte      | Descrizione                                            |
|-----------|--------------------------------------------------------|
| *Richiesta* | Restituisce l'oggetto [**Request**](/windows/desktop/lwef/the-request-object) . |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

L'evento restituisce un oggetto [**Request**](/windows/desktop/lwef/the-request-object) . Poiché le richieste vengono elaborate in modo asincrono, è possibile usare questo evento per determinare quando il server inizia a elaborare una richiesta, ad esempio un metodo [**Get**](get-method.md), [**Play**](play-method.md)o [**Speak**](speak-method.md) , e quindi sincronizzarlo con altre azioni generate dall'applicazione. L'evento viene inviato solo al client che ha creato il riferimento all'oggetto **richiesta** e solo se è stata definita una variabile globale per il riferimento alla richiesta:


```
   Dim MyRequest 
   Dim Genie 

   Sub window_Onload
   
   Agent1.Characters.Load "Genie", _
      "https://agent.microsoft.com/characters/v2/genie/genie.acf"   

   Set Genie = Agent1.Characters("Genie")

   ' This syntax will generate RequestStart and RequestComplete events.
   Set MyRequest = Genie.Get("state", "Showing")

   ' This syntax will not generate RequestStart and RequestComplete events.
   Genie.Get ("state", "Hiding")

   End Sub

   Sub Agent1_RequestStart(ByVal Request)

   If Request = MyRequest Then
      Status = "Loading the Showing animation"

   End Sub
```



Lo [**stato**](status-property.md) restituisce 4 (richiesta in corso) per l'oggetto [**Request**](/windows/desktop/lwef/the-request-object) restituito.

Poiché gli oggetti [**richiesta**](/windows/desktop/lwef/the-request-object) di animazione non vengono assegnati finché il server non elabora la richiesta, assicurarsi che l'oggetto **richiesta** esista prima di provare a valutarlo. Ad esempio, in Visual Basic, se si usa un condizionale per verificare se una richiesta specifica è stata completata, è possibile usare la parola chiave **Nothing** :


```
   Sub Agent1_RequestStart (ByVal Request)

   If Not (MyRequest Is Nothing) Then
      If Request = MyRequest Then
      '-- Do whatever
      End If
   End If

   End Sub
```



> [!Note]  
> In VBScript 1,0, questo evento viene generato anche se non si definiscono riferimenti a un oggetto [**Request**](/windows/desktop/lwef/the-request-object) . Questo problema è stato risolto in VBScript 2,0, che può essere scaricato da <https://microsoft.com/msdownload/vbscript/scripting.asp> .

 

### <a name="see-also"></a>Vedere anche

[**Evento RequestComplete**](requestcomplete-event.md)


 

 