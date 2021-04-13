---
title: Evento ListenComplete
description: Evento ListenComplete
ms.assetid: 29e3f424-17b4-4287-b644-ed62b80e0035
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dbfe0fac272b50af3f82efdc8a422bebddbf786
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396699"
---
# <a name="listencomplete-event"></a>Evento ListenComplete

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando la modalità di ascolto (riconoscimento vocale) è terminata.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

 *Agente secondario. * * * ListenComplete (ByVal* *  *CharacterID*, **ByVal** *cause * * *)**



| Parte          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere di ascolto sotto forma di stringa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *Causa*       | Restituisce la parte dell'evento completo come numero intero che può essere uno dei seguenti: 1 la modalità di ascolto è stata disattivata dal codice del programma.<br/> si è verificato un timeout di 2 modalità di ascolto (attivata dal codice del programma).<br/> si è verificato un timeout di 3 modalità di ascolto (attivata dal tasto di attesa).<br/> 4 la modalità di ascolto è stata disattivata perché l'utente ha rilasciato il tasto di attesa.<br/> 5 modalità di ascolto terminata perché l'utente ha terminato di parlare.<br/> 6 modalità di ascolto terminata perché il client di input-attivo è stato disattivato.<br/> 7 modalità di ascolto terminata perché il carattere predefinito è stato modificato.<br/> 8 modalità di ascolto terminata perché l'utente ha disabilitato l'input vocale.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Questo evento viene inviato a tutti i client quando termina il timeout della modalità di ascolto, dopo che l'utente rilascia il tasto di attesa, quando il client attivo di input chiama il metodo [**Listen**](listen-method.md) con **false** oppure l'utente ha terminato di parlare. È possibile usare questo evento per determinare quando riavviare l'output di tipo carattere parlato.

Se si attiva la modalità di ascolto utilizzando il metodo [**Listen**](listen-method.md) e quindi l'utente preme il tasto ascolto, la modalità di ascolto viene reimpostata e continua fino a quando non viene completato il timeout della chiave di ascolto, viene rilasciata la chiave in ascolto o l'utente termina di parlare, a seconda di quale dei più tardi. In questa situazione, non si riceverà un evento **ListenComplete** fino al completamento della modalità della chiave di ascolto.

L'evento restituisce il carattere ai client attualmente caricati da questo carattere. Tutti gli altri client ricevono un carattere null (stringa vuota).

### <a name="see-also"></a>Vedere anche

[**Evento ListenStart**](listenstart-event.md), [ **metodo Listen**](listen-method.md)


 

 





