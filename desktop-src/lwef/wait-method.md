---
title: Metodo Wait
description: Metodo Wait
ms.assetid: 968a3f19-6953-473b-ba98-0dc93696e703
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2e94b0f765a9861c30b254761fbc4dc2e72763
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299606"
---
# <a name="wait-method"></a>Metodo Wait

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Fa in modo che la coda dell'animazione per il carattere specificato attenda finché non viene completata la richiesta di animazione specificata.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID ***").*** Richiesta di attesa*



| Parte      | Descrizione                                                                     |
|-----------|---------------------------------------------------------------------------------|
| *Richiesta* | Oggetto [**Request**](/windows/desktop/lwef/the-request-object) che specifica un'animazione particolare. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare questo metodo solo quando sono supportati più caratteri (simultanei) e si sta tentando di sequenziare l'interazione dei caratteri. (Per un singolo carattere, ogni richiesta di animazione viene riprodotta in sequenza, dopo il completamento della richiesta precedente). Se si dispone di due caratteri e si desidera che la richiesta di animazione di un carattere attenda il completamento dell'animazione dell'altro carattere, impostare il metodo **wait** sull'oggetto [**richiesta**](/windows/desktop/lwef/the-request-object) di animazione dell'altro carattere. Per specificare il parametro request, è necessario creare una variabile e assegnare la richiesta di animazione che si vuole interrompere:


```
   Dim GenieRequest 
   Dim RobbyRequest 
   Dim Genie 
   Dim Robby 

   Sub window_Onload

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"
   Agent1.Characters.Load "Robby", "https://agent.microsoft.com/characters/v2/robby/robby.acf"

   Set Genie = Agent1.Characters("Genie")
   Set Robby = Agent1.Characters("Robby")

   Genie.Get "State", "Showing"
   Robby.Get "State", "Showing"

   Genie.Get "Animation", "Announce, AnnounceReturn, Pleased, _ 
      PleasedReturn"
   
   Robby.Get "Animation", "Confused, ConfusedReturn, Sad, SadReturn"

   Set Genie = Agent1.Characters ("Genie")
   Set Robby = Agent1.Characters ("Robby")

   Genie.MoveTo 100,100
   Genie.Show

   Robby.MoveTo 250,100
   Robby.Show

   Genie.Play "Announce"
   Set GenieRequest = Genie.Speak ("Why did the chicken cross the road?")
   
   Robby.Wait GenieRequest
   Robby.Play "Confused"
   Set RobbyRequest = Robby.Speak ("I don't know. Why did the chicken _
      cross the road?")
   
   Genie.Wait RobbyRequest
   Genie.Play "Pleased"
   Set GenieRequest = Genie.Speak ("To get to the other side.")
   
   Robby.Wait GenieRequest
   Robby.Play "Sad"
   Robby.Speak "I never should have asked."

   End Sub
```



È anche possibile semplificare il codice semplicemente chiamando **wait** direttamente, usando una richiesta di animazione specifica.


```
   Robby.Wait Genie.Play "GestureRight"
```



In questo modo si evita di dover dichiarare in modo esplicito un oggetto [**Request**](/windows/desktop/lwef/the-request-object) .

 

 