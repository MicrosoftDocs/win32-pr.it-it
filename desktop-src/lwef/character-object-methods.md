---
title: Metodi dell'oggetto Character
description: Metodi dell'oggetto Character
ms.assetid: 0f926b7b-c1cf-4bd6-ba8c-1b2877eb1d24
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141c0fbcfe26e198984fd4a4d8c6c67858085e41178786d2cb78d2938231fdf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480315"
---
# <a name="character-object-methods"></a>Metodi dell'oggetto Character

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il server espone anche i metodi per ogni carattere in una [**raccolta Characters.**](/windows/desktop/lwef/the-characters-object) Sono supportati i metodi seguenti:

-   [**Attiva**](activate-method.md)
-   [**GestureAt**](gestureat-method.md)
-   [**Ottieni**](get-method.md)
-   [**Nascondi**](hide-method.md)
-   [**Interrompere**](interrupt-method.md)
-   [**Attesa**](listen-method.md)
-   [**Moveto**](moveto-method.md)
-   [**Esegui**](play-method.md)
-   [**Mostra**](show-method.md)
-   [**ShowPopupMenu**](showpopupmenu-method.md)
-   [**Speak**](speak-method.md)
-   [**Fermare**](stop-method.md)
-   [**StopAll**](stopall-method.md)
-   [**Pensare**](think-method.md)
-   [**Attesa**](wait-method.md)

Per usare un metodo, fare riferimento al carattere nella raccolta. In VBScript e Visual Basic eseguire questa operazione specificando l'ID per un carattere:


```
   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Display the character
   Agent1.Characters("Genie").Show
   Agent1.Characters("Genie").Play "Greet"
   Agent1.Characters("Genie").Speak "Hello. "

   End Sub
```



Per semplificare la sintassi del codice, è possibile definire una variabile oggetto e impostarla per fare riferimento a un oggetto carattere nella [**raccolta Characters.**](/windows/desktop/lwef/the-characters-object) è quindi possibile usare la variabile per fare riferimento ai metodi o alle proprietà del carattere. L'esempio seguente illustra come eseguire questa operazione usando l'istruzione Visual Basic Set:


```
   'Define a global object variable
   Dim Genie as Object

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", " Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   'Get the Restpose animation
   Genie.Get "animation", "RestPose"

   'Make the character say Hello
   Genie.Speak "Hello."

   End Sub
```



In Visual Basic 5.0 è anche possibile creare il riferimento dichiarando la variabile come [**oggetto Character:**](/windows/desktop/lwef/the-characters-object)


```
   Dim Genie as IAgentCtlCharacterEx

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   End Sub
```



La dichiarazione dell'oggetto di tipo IAgentCtlCharacterEx abilita l'associazione anticipata sull'oggetto, con prestazioni migliori.

In VBScript non è possibile dichiarare un riferimento come tipo specifico. È tuttavia possibile dichiarare semplicemente il riferimento alla variabile:


```
<SCRIPT LANGUAGE = "VBSCRIPT">
<!—--

   Dim Genie
   
   Sub window_OnLoad
   
   'Load the character
   AgentCtl.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   'Create an object reference to the character in the collection
   set Genie= AgentCtl.Characters ("Genie")

   'Get the Showing state animation
   Genie.Get "state", "Showing"

   'Display the character
   Genie.Show

   End Sub

-->
   </SCRIPT>
```



Alcuni linguaggi di programmazione non supportano le raccolte. Tuttavia, è possibile accedere ai metodi di un oggetto [**Character**](/windows/desktop/lwef/the-characters-object) con il [**metodo Character:**](character-method.md)


```
   agent.Characters.Character("CharacterID").method
```



È anche possibile creare un riferimento all'oggetto [**Character**](/windows/desktop/lwef/the-characters-object) per semplificare l'esecuzione del codice di script:


```
<SCRIPT LANGUAGE="JScript" FOR="window" EVENT="onLoad()">
<!--
   
   //Load the character's data
   AgentCtl.Characters.Load ("Genie", _
      "https://agent.microsoft.com/characters/v2/genie/genie.acf");   

   //Create a reference to this object
   Genie = AgentCtl.Characters.Character("Genie");
   
   //Get the Showing state animation
   Genie.Get("state", "Showing");

   //Display the character
   Genie.Show();

-->
</SCRIPT>
```



 

 