---
title: Metodi dell'oggetto character
description: Metodi dell'oggetto character
ms.assetid: 0f926b7b-c1cf-4bd6-ba8c-1b2877eb1d24
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19bb0dbb256c99660cbce1613c9fdd27d85a92dc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956362"
---
# <a name="character-object-methods"></a>Metodi dell'oggetto character

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il server espone inoltre i metodi per ogni carattere in una raccolta di [**caratteri**](/windows/desktop/lwef/the-characters-object) . Sono supportati i metodi seguenti:

-   [**Activate**](activate-method.md)
-   [**GestureAt**](gestureat-method.md)
-   [**Recupero**](get-method.md)
-   [**Nascondi**](hide-method.md)
-   [**Interrompere**](interrupt-method.md)
-   [**Attesa**](listen-method.md)
-   [**MoveTo**](moveto-method.md)
-   [**Esegui**](play-method.md)
-   [**Visualizza**](show-method.md)
-   [**ShowPopupMenu**](showpopupmenu-method.md)
-   [**Speak**](speak-method.md)
-   [**Interrompere**](stop-method.md)
-   [**StopAll**](stopall-method.md)
-   [**Pensare**](think-method.md)
-   [**Attesa**](wait-method.md)

Per usare un metodo, fare riferimento al carattere nella raccolta. In VBScript e Visual Basic è possibile eseguire questa operazione specificando l'ID per un carattere:


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



Per semplificare la sintassi del codice, è possibile definire una variabile oggetto e impostarla in modo che faccia riferimento a un oggetto character nella raccolta [**Characters**](/windows/desktop/lwef/the-characters-object) . è quindi possibile usare la variabile per fare riferimento a metodi o proprietà del carattere. Nell'esempio seguente viene illustrato come è possibile eseguire questa operazione utilizzando l'istruzione set Visual Basic:


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



In Visual Basic 5,0, è anche possibile creare il riferimento dichiarando la variabile come oggetto [**character**](/windows/desktop/lwef/the-characters-object):


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



La dichiarazione di un oggetto di tipo IAgentCtlCharacterEx consente di associare in anticipo l'oggetto, con un conseguente miglioramento delle prestazioni.

In VBScript non è possibile dichiarare un riferimento come un tipo particolare. È tuttavia possibile dichiarare semplicemente il riferimento alla variabile:


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



Alcuni linguaggi di programmazione non supportano le raccolte. È tuttavia possibile accedere ai metodi di un oggetto [**character**](/windows/desktop/lwef/the-characters-object) con il metodo [**character**](character-method.md) :


```
   agent.Characters.Character("CharacterID").method
```



Inoltre, è possibile creare un riferimento all'oggetto [**carattere**](/windows/desktop/lwef/the-characters-object) per semplificare il codice di script:


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



 

 