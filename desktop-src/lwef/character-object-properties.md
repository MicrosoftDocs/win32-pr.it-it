---
title: Proprietà dell'oggetto character
description: Proprietà dell'oggetto character
ms.assetid: 86748de2-f5c8-4057-bfa4-79d46cac1e62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6212d6f0539b7fcb29faa883e6d88101952c12f5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398850"
---
# <a name="character-object-properties"></a>Proprietà dell'oggetto character

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

L'oggetto [**character**](/windows/desktop/lwef/the-characters-object) espone le proprietà seguenti:

-   [**Attivo**](active-property.md)
-   [**AutoPopupMenu**](autopopupmenu-property.md)
-   [**Descrizione**](description-property.md)
-   [**ExtraData**](extradata-property.md)
-   [**GUID**](guid-property.md)
-   [**HasOtherClients**](hasotherclients-property.md)
-   [**Altezza**](height-property.md)
-   [**HelpContextID**](helpcontextid-property-ch.md)
-   [**HelpFile**](helpfile-property.md)
-   [**HelpModeOn**](helpmodeon-property.md)
-   [**IdleOn**](idleon-property.md)
-   [**LanguageID**](languageid-property.md)
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

Si noti che le proprietà [**Height**](height-property.md), [**Left**](left-property.md), [**Top**](top-property.md)e [**Width**](width-property-co.md) di un carattere sono diverse da quelle che possono essere supportate dall'ambiente di programmazione per il posizionamento del controllo. Le proprietà dei [**caratteri**](/windows/desktop/lwef/the-characters-object) si applicano alla presentazione visibile di un carattere, non al percorso del controllo Microsoft Agent.

Come per i metodi dell'oggetto [**character**](/windows/desktop/lwef/the-characters-object) , è possibile accedere alle proprietà di un carattere usando la raccolta [**characters**](/windows/desktop/lwef/the-characters-object) oppure semplificare la sintassi dichiarando una variabile oggetto e impostandolo su un carattere nella raccolta. Nell'esempio seguente, test1 e Test2 verranno impostati sullo stesso valore:


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



Poiché il server carica un carattere in modo asincrono, verificare che il carattere sia stato caricato prima di eseguire una query sulle relative proprietà, ad esempio usando l'evento [**RequestComplete**](requestcomplete-event.md) . In caso contrario, le proprietà possono restituire valori non corretti.

 

 