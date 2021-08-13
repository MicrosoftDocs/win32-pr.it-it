---
title: Metodo Interrupt
description: Metodo Interrupt
ms.assetid: b8442e25-a629-47c7-acdd-1d28e74d78a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e66814963bb3de3db95d60cbc25777244626168e95ceee4bd3d8d76992dd72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749258"
---
# <a name="interrupt-method"></a>Metodo Interrupt

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Interrompe l'animazione per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Richiesta di_ *  *interruzione*



| Parte      | Descrizione                                                                  |
|-----------|------------------------------------------------------------------------------|
| *Richiesta* | Oggetto [**Request**](/windows/desktop/lwef/the-request-object) per una chiamata di animazione specifica. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile usarlo per sincronizzare l'animazione tra i caratteri. Ad esempio, se un altro carattere è in un'animazione a ciclo continuo, questo metodo arresta il ciclo e passa all'animazione successiva nella coda del carattere. Non è possibile interrompere un'animazione di caratteri non in uso (che non è stata caricata).

Per specificare il parametro request, è necessario creare una variabile e assegnare la richiesta di animazione da interrompere:


```
   Dim GenieRequest as Object
   Dim RobbyRequest as Object
   Dim Genie as Object
   Dim Robby as Object

   Sub FormLoad()

      MyAgent1.Characters.Load "Genie", "Genie.acs"

      MyAgent1.Characters.Load "Robby", "Robby.acs"

      Set Genie = MyAgent1.Characters ("Genie")
      Set Robby = MyAgent1.Characters ("Robby")

      Genie.Show

      Genie.Speak "Just a moment"

      Set GenieRequest = Genie.Play ("Processing")

      Robby.Show
      Robby.Play "confused"
      Robby.Speak "Hey, Genie. What are you doing?"
      Robby.Interrupt GenieRequest

      Genie.Speak "I was just checking on something."

   End Sub
```



Non è possibile interrompere l'animazione dello stesso carattere specificato in questo metodo perché il server accoda il metodo **Interrupt** nella coda di animazione del carattere. Pertanto, è possibile usare **Interrupt solo per** arrestare l'animazione di un altro carattere caricato.

Se si dichiara un riferimento a un oggetto e lo si imposta su questo metodo, viene restituito [**un oggetto Request.**](/windows/desktop/lwef/the-request-object)

> [!Note]  
> **L'interrupt** non scarica la coda del carattere. arresta l'animazione esistente e passa all'animazione successiva nella coda del carattere. Per arrestare e scaricare la coda di un carattere, usare il [**metodo Stop.**](stop-method.md)

 

## <a name="see-also"></a>Vedere anche

[**Metodo Stop**](stop-method.md)


 

 