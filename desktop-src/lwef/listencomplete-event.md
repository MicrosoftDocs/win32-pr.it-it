---
title: Evento ListenComplete
description: Evento ListenComplete
ms.assetid: 29e3f424-17b4-4287-b644-ed62b80e0035
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d25e9bfbf23c6a2911c718b576c99395ef06fd802853b39b699384a9ab92429b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883893"
---
# <a name="listencomplete-event"></a>Evento ListenComplete

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica al termine della modalità di ascolto (riconoscimento vocale).

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *agent.***ListenComplete (ByVal* *  *CharacterID,* **ByVal** *Cause***)**



| Parte          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere di ascolto come stringa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *Causa*       | Restituisce la causa dell'evento completo come numero intero che può essere uno dei seguenti: 1 La modalità di ascolto è stata disattivata dal codice del programma.<br/> 2 Timeout della modalità di ascolto (attivata dal codice programma).<br/> 3 Timeout della modalità di ascolto (attivata dalla chiave di ascolto).<br/> 4 La modalità di ascolto è stata disattivata perché l'utente ha rilasciato la chiave di ascolto.<br/> 5 Modalità di ascolto terminata perché l'utente ha terminato la conversazione.<br/> 6 Modalità di ascolto terminata perché il client attivo di input è stato disattivato.<br/> 7 Modalità di ascolto terminata perché il carattere predefinito è stato modificato.<br/> 8 Modalità di ascolto terminata perché l'utente ha disabilitato l'input vocale.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Questo evento viene inviato a tutti i client quando termina il timeout della modalità di ascolto, dopo che l'utente ha rilasciato il tasto Ascolto, quando il client attivo di input chiama il metodo [**Listen**](listen-method.md) con **False** o l'utente ha terminato la conversazione. È possibile usare questo evento per determinare quando riprendere l'output parlato (audio) del carattere.

Se si attiva la modalità di ascolto usando il metodo [**Listen**](listen-method.md) e quindi l'utente preme il tasto Ascolto, la modalità di ascolto viene reimpostata e continua fino al completamento del timeout della chiave di ascolto, il tasto ascolto viene rilasciato o l'utente termina la conversazione, a seconda di quale sia il momento successivo. In questo caso, non si riceverà un **evento ListenComplete** fino al completamento della modalità del tasto di ascolto.

L'evento restituisce il carattere ai client che dispongono attualmente di questo carattere caricato. Tutti gli altri client ricevono un carattere Null (stringa vuota).

### <a name="see-also"></a>Vedere anche

[**Evento ListenStart**](listenstart-event.md), [ **metodo Listen**](listen-method.md)


 

 





