---
title: Evento ActivateInput
description: Evento ActivateInput
ms.assetid: bc395750-5da0-4379-8eca-3195e936052c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0b4fdf83256d58dd247dee85b639f5499f013e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045233"
---
# <a name="activateinput-event"></a>Evento ActivateInput

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando un client diventa attivo come input.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *Agent* \_ ActivateInput **(ByVal** *CharacterID * * *)**



| Parte          | Descrizione                                                                    |
|---------------|--------------------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere tramite il quale il client diventa attivo come input. |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Il client attivo per l'input riceve gli eventi di input del mouse e vocale forniti dal server. Il server invia questo evento solo al client che diventa attivo come input.

Questo evento può verificarsi quando l'utente passa all'oggetto [Command](the-command-object.md) , ad esempio scegliendo la voce oggetto comando nella finestra comandi o nel menu a comparsa per un carattere. Può inoltre verificarsi quando l'utente seleziona un carattere, facendo clic o pronunciando il relativo nome, quando un carattere diventa visibile e quando il carattere di un'altra applicazione client diventa nascosto. È anche possibile chiamare il [metodo Activate](activate-method.md) (con **stato** impostato su 2) per rendere esplicitamente il carattere in primo piano, il che comporta che l'applicazione client diventi input-Active e attiva questo evento. Tuttavia, questo evento non si verifica se si usa il metodo Activate solo per specificare se il client è il client attivo del carattere.

### <a name="see-also"></a>Vedere anche

[Evento **DeactivateInput**](deactivateinput-event.md), [metodo **Activate**](activate-method.md)


 

 




