---
title: Metodo Stop (funzionalità dell Windows legacy)
description: Metodo Stop
ms.assetid: 68372f72-db9c-447c-a3e4-488940c730d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572a93db5697aaae0dcfed6b45a834323c106bba447d2d9a8e94109f788af25c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745963"
---
# <a name="stop-method-legacy-windows-environment-features"></a>Metodo Stop (funzionalità dell Windows legacy)

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Arresta l'animazione per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Arresta_ *  \[ *richiesta*\]



| Parte      | Descrizione                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------|
| *Richiesta* | facoltativo. Oggetto [**Request**](/windows/desktop/lwef/the-request-object) che specifica una chiamata di animazione specifica. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Per specificare il parametro della richiesta, è necessario creare una variabile e assegnare la richiesta di animazione che si vuole arrestare. Se non si imposta il parametro **Request,** il server arresta tutte le animazioni per il carattere, incluse le  chiamate  [**Get**](get-method.md) in coda, e cancella la coda di animazione, a meno che il carattere non riproduce attualmente l'animazione Nascondere o Mostrare. Questo metodo non arresta le chiamate **Get** non in coda.

Per arrestare un'animazione specifica o [**una chiamata Get,**](get-method.md) dichiarare una variabile oggetto e assegnare la richiesta di animazione a tale variabile:


```
   Dim MyRequest
   Dim Genie

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")

   Genie.Get "state", "Showing"
   Genie.Get "animation", "Greet, GreetReturn"

   Genie.Show
   
   'This animation will never play
   Set MyRequest = Genie.Play ("Greet")
   
   Genie.Stop MyRequest
```



Questo metodo non genererà un [**oggetto**](/windows/desktop/lwef/the-request-object) Request.

## <a name="see-also"></a>Vedere anche

[**Metodo StopAll**](stopall-method.md)


 

 
