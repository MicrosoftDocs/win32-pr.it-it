---
title: Evento ListenStart
description: Evento ListenStart
ms.assetid: 59feacd6-0b9f-4bf4-b544-48de49384312
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0017b628af3ca266058de74508d379bd665c94f94c64207f4d7bef5487a0f4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976111"
---
# <a name="listenstart-event"></a>Evento ListenStart

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica all'inizio della modalità di ascolto (riconoscimento vocale).

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *agent.***ListenStart (ByVal* *  *CharacterID***)**



| Parte          | Descrizione                                            |
|---------------|--------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere di ascolto come stringa. |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Questo evento viene inviato a tutti i client all'avvio della modalità di ascolto perché l'utente ha premuto il tasto Listening o il client attivo di input ha chiamato il [**metodo Listen**](listen-method.md) con **True.** È possibile usare questo evento per evitare che il tuo carattere parla mentre è attiva la modalità di ascolto.

Se si attiva la modalità di ascolto con il metodo [**Listen**](listen-method.md) e quindi l'utente preme il tasto listening, la modalità di ascolto viene reimpostata e continua fino al completamento del timeout della chiave di ascolto, il tasto di ascolto viene rilasciato o l'utente termina la conversazione, a seconda di quale sia il momento successivo. In questo caso, quando la modalità di ascolto è già attivata, non si otterrà un evento **ListenStart** aggiuntivo quando l'utente preme il tasto Listening.

L'evento restituisce il carattere ai client in cui è attualmente caricato questo carattere. Tutti gli altri client ricevono un carattere Null (stringa vuota).

### <a name="see-also"></a>Vedere anche

[**Evento ListenComplete**](listencomplete-event.md), [ **metodo Listen**](listen-method.md)


 

 




