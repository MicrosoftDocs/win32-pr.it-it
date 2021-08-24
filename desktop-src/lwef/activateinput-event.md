---
title: Evento ActivateInput
description: Evento ActivateInput
ms.assetid: bc395750-5da0-4379-8eca-3195e936052c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db21d605a014002063a7c5aa42554a06adb1ed35296242944de789daeb3155c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610681"
---
# <a name="activateinput-event"></a>Evento ActivateInput

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando un client diventa attivo per l'input.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *agent* \_ ActivateInput **(ByVal** *CharacterID***)**



| Parte          | Descrizione                                                                    |
|---------------|--------------------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere tramite il quale il client diventa attivo per l'input. |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Il client attivo per l'input riceve gli eventi di input del mouse e del riconoscimento vocale forniti dal server. Il server invia questo evento solo al client che diventa attivo per l'input.

Questo evento può verificarsi quando l'utente passa all'oggetto [Command,](the-command-object.md) ad esempio scegliendo la voce dell'oggetto Command nella finestra comandi o nel menu a comparsa per un carattere. Può verificarsi anche quando l'utente seleziona un carattere (facendo clic o pronunciando il nome), quando un carattere diventa visibile e quando il carattere di un'altra applicazione client diventa nascosto. È anche possibile chiamare il metodo [Activate](activate-method.md) (con **State** impostato su 2) per impostare in modo esplicito il carattere in primo piano, in modo che l'applicazione client diventi attiva per l'input e attivi l'evento. Tuttavia, questo evento non si verifica se si usa il metodo Activate solo per specificare se il client è il client attivo del carattere.

### <a name="see-also"></a>Vedere anche

[**Evento DeactivateInput**](deactivateinput-event.md), [ **metodo Activate**](activate-method.md)


 

 




