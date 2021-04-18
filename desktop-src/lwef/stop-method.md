---
title: Metodo Stop (funzionalità legacy dell'ambiente Windows)
description: Metodo Stop
ms.assetid: 68372f72-db9c-447c-a3e4-488940c730d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20192634c197559ca54bb8af3d8a29f37beb53e2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300856"
---
# <a name="stop-method-legacy-windows-environment-features"></a>Metodo Stop (funzionalità legacy dell'ambiente Windows)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Arresta l'animazione per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("**_CharacterID_*_"). Arresta_ *  \[ *richiesta*\]



| Parte      | Descrizione                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------|
| *Richiesta* | facoltativo. Oggetto [**Request**](/windows/desktop/lwef/the-request-object) che specifica una particolare chiamata di animazione. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Per specificare il parametro request, è necessario creare una variabile e assegnare la richiesta di animazione che si desidera arrestare. Se non si imposta il parametro **Request** , il server interrompe tutte le animazioni per il carattere, incluse le chiamate [**Get**](get-method.md) in coda, e cancella la coda delle animazioni, a meno che il carattere non stia attualmente **eseguendo l'animazione o la** **visualizzazione** . Questo metodo non interrompe le chiamate **Get** non in coda.

Per arrestare un'animazione o una chiamata [**Get**](get-method.md) specifica, dichiarare una variabile oggetto e assegnare la richiesta di animazione alla variabile:


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



Questo metodo non genererà un oggetto [**Request**](/windows/desktop/lwef/the-request-object) .

## <a name="see-also"></a>Vedere anche

[**Metodo StopAll**](stopall-method.md)


 

 
