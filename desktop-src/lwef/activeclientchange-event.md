---
title: Evento ActiveClientChange
description: Evento ActiveClientChange
ms.assetid: 617b40e6-cafb-463e-8b36-2a12c468d3ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8137edd559d934fd1a478350cd1185885c7dc148
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221425"
---
# <a name="activeclientchange-event"></a>Evento ActiveClientChange

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando viene modificato il client attivo del carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

Agente **secondario** *.* ActiveClientChange (ByVal *CharacterID*, ByVal *Active* **)**



| Parte          | Descrizione                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere per il quale si è verificato l'evento.                                                                                                                                                                                                      |
| *Attivo*      | Valore booleano che indica se il client diventa attivo o meno. Valore **true** L'applicazione client è diventata il client attivo del carattere. <br/> **False** L'applicazione client non è più il client attivo del carattere.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Quando più applicazioni client condividono lo stesso carattere, il client attivo del carattere riceve l'input del mouse (ad esempio, gli eventi di clic o di trascinamento del controllo agente Microsoft). Analogamente, quando vengono visualizzati più caratteri, il client attivo del carattere superiore (noto anche come client attivo di input) riceve gli eventi di [comando](command-event.md) .

Quando viene modificato il client attivo di un carattere, questo evento restituisce l'ID di tale carattere e **true** se l'applicazione è diventata il client attivo del carattere o **false** se non è più il client attivo del carattere.

Un'applicazione client può ricevere questo evento quando l'utente seleziona la voce di un'applicazione client nel menu popup del carattere o tramite il comando vocale, quando l'applicazione client modifica il proprio stato attivo o quando un'altra applicazione client chiude la connessione a Agent. Agent invia questo evento solo alle applicazioni client direttamente interessate; che diventeranno il client attivo o smetteranno di essere il client attivo.

### <a name="see-also"></a>Vedere anche

[* * * * ActivateInput * * evento * *](activateinput-event.md), [* * * * attivo * * proprietà * *](active-property.md), [* * * * DeactivateInput * * evento * *](deactivateinput-event.md), [* * * * Attiva * * metodo * *](activate-method.md)


 

 





