---
title: Metodo interrupt
description: Metodo interrupt
ms.assetid: b8442e25-a629-47c7-acdd-1d28e74d78a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58050e181525cc4a4b9f35ec169e92d91ab28e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104399031"
---
# <a name="interrupt-method"></a>Metodo interrupt

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Interrompe l'animazione per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID * * *").* *  *Richiesta* di interrupt



| Parte      | Descrizione                                                                  |
|-----------|------------------------------------------------------------------------------|
| *Richiesta* | Oggetto [**Request**](/windows/desktop/lwef/the-request-object) per una particolare chiamata di animazione. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile usarlo per sincronizzare l'animazione tra caratteri. Se, ad esempio, un altro carattere si trova in un'animazione di ciclo, questo metodo arresterà il ciclo e passerà all'animazione successiva nella coda del carattere. Non è possibile interrompere un'animazione di caratteri che non si sta usando (che non è stata caricata).

Per specificare il parametro request, è necessario creare una variabile e assegnare la richiesta di animazione che si vuole interrompere:


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



Non è possibile interrompere l'animazione dello stesso carattere specificato in questo metodo perché il server accoda il metodo **interrupt** nella coda di animazione di tale carattere. Pertanto, è possibile utilizzare solo **interrupt** per arrestare l'animazione di un altro carattere caricato.

Se si dichiara un riferimento a un oggetto e lo si imposta su questo metodo, viene restituito un oggetto [**Request**](/windows/desktop/lwef/the-request-object) .

> [!Note]  
> L' **interrupt** non Scarica la coda del carattere; arresta l'animazione esistente e passa all'animazione successiva nella coda del carattere. Per arrestare e scaricare la coda di un carattere, usare il metodo [**Stop**](stop-method.md) .

 

## <a name="see-also"></a>Vedere anche

[**Metodo Stop**](stop-method.md)


 

 