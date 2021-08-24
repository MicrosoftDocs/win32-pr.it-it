---
title: Proprietà dell'oggetto Character
description: Proprietà dell'oggetto Character
ms.assetid: 86748de2-f5c8-4057-bfa4-79d46cac1e62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c80e16bdb35d3fdfd8687eb15f200d2005ab75027e4dcc786f883d21232af4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610691"
---
# <a name="character-object-properties"></a>Proprietà dell'oggetto Character

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

[**L'oggetto Character**](/windows/desktop/lwef/the-characters-object) espone le proprietà seguenti:

-   [**Attivo**](active-property.md)
-   [**AutoPopupMenu**](autopopupmenu-property.md)
-   [**Descrizione**](description-property.md)
-   [**Extradata**](extradata-property.md)
-   [**Guid**](guid-property.md)
-   [**HasOtherClients**](hasotherclients-property.md)
-   [**Altezza**](height-property.md)
-   [**HelpContextID**](helpcontextid-property-ch.md)
-   [**Helpfile**](helpfile-property.md)
-   [**HelpModeOn**](helpmodeon-property.md)
-   [**IdleOn**](idleon-property.md)
-   [**Languageid**](languageid-property.md)
-   [**Sinistra**](left-property.md)
-   [**MoveCause**](movecause-property.md)
-   [**Nome**](name-property.md)
-   [**OriginalHeight**](originalheight-property.md)
-   [**OriginalWidth**](originalwidth-property.md)
-   [**Passo**](pitch-property.md)
-   [**SoundEffectsOn**](soundeffectson-property.md)
-   [**Velocità**](speed-property.md)
-   [**SRModeID**](srmodeid-property.md)
-   [**SRStatus**](srstatus-property.md)
-   [**In alto**](top-property.md)
-   [**TTSModeID**](ttsmodeid-property.md)
-   [**Versione**](version-property.md)
-   [**VisibilityCause**](visibilitycause-property.md)
-   [**Visible**](visible-property-cob.md)
-   [**Larghezza**](width-property-co.md)

Si noti che le proprietà [**Height,**](height-property.md) [**Left,**](left-property.md) [**Top**](top-property.md)e [**Width**](width-property-co.md) di un carattere sono diverse da quelle che potrebbero essere supportate dall'ambiente di programmazione per la posizione del controllo. Le [**proprietà Character**](/windows/desktop/lwef/the-characters-object) si applicano alla presentazione visibile di un carattere, non alla posizione del controllo Microsoft Agent.

Come con i metodi dell'oggetto [**Character,**](/windows/desktop/lwef/the-characters-object) è possibile accedere alle proprietà di un carattere usando la raccolta [**Characters**](/windows/desktop/lwef/the-characters-object) o semplificare la sintassi dichiarando una variabile oggetto e impostandola su un carattere nella raccolta. Nell'esempio seguente Test1 e Test2 verranno impostati sullo stesso valore:


```
   Dim Genie 
   Dim MyRequest
   
   Sub window_Onload

   Agent.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent.Characters("Genie")

   Genie.MoveTo 15,15
   Set MyRequest = Genie.Show()

   End Sub

   Sub Agent_RequestComplete(ByVal Request)

   If Request = MyRequest Then 
      Test1 = Agent.Characters("Genie").Top
      Test2 = Genie.Top
      MsgBox "Test 1 is " + cstr(Test1) + "and Test 2 is " + cstr(Test2)
   End If

   End Sub
```



Poiché il server carica un carattere in modo asincrono, assicurarsi che il carattere sia stato caricato prima di eseguire una query delle relative proprietà, ad esempio usando [**l'evento RequestComplete.**](requestcomplete-event.md) In caso contrario, le proprietà potrebbero restituire valori non corretti.

 

 