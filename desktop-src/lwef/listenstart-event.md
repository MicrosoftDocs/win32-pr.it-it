---
title: Evento ListenStart
description: Evento ListenStart
ms.assetid: 59feacd6-0b9f-4bf4-b544-48de49384312
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b8cc19ad727f8e9c4606bbbfba7b2e03e7d638
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856789"
---
# <a name="listenstart-event"></a>Evento ListenStart

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando inizia la modalità di ascolto (riconoscimento vocale).

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

Agente **secondario** *. * * * ListenStart (ByVal* *  *CharacterID * * *)**



| Parte          | Descrizione                                            |
|---------------|--------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere di ascolto sotto forma di stringa. |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Questo evento viene inviato a tutti i client quando viene avviata la modalità di ascolto perché l'utente ha premuto il tasto ascolto o il client di input-attivo denominato metodo [**Listen**](listen-method.md) con **true**. È possibile usare questo evento per evitare che il carattere parli mentre la modalità di ascolto è attiva.

Se si attiva la modalità di ascolto con il metodo [**Listen**](listen-method.md) e quindi l'utente preme il tasto ascolto, la modalità di ascolto viene reimpostata e continua fino a quando non viene completato il timeout della chiave di ascolto, viene rilasciato il tasto di attesa o l'utente termina di parlare, a seconda di quale sarà il momento successivo. In questa situazione, quando la modalità di ascolto è già attiva, non si otterrà un evento **ListenStart** aggiuntivo quando l'utente preme il tasto di attesa.

L'evento restituisce il carattere ai client attualmente caricati da questo carattere. Tutti gli altri client ricevono un carattere null (stringa vuota).

### <a name="see-also"></a>Vedere anche

[**Evento ListenComplete**](listencomplete-event.md), [ **metodo Listen**](listen-method.md)


 

 




