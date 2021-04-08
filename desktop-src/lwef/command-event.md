---
title: Evento Command
description: Evento Command
ms.assetid: 3e180286-dfa0-4b34-90ee-3267ed6f48af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5647e7eac3aaba0a6094be6b52cc3726eba34ad7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046713"
---
# <a name="command-event"></a>Evento Command

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando l'utente sceglie un comando (client).

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Comando sub** *Agent* \_  **(ByVal** *userinput * * *)**



| Parte        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *UserInput* | Identifica l'oggetto [**Command**](/windows/desktop/lwef/the-command-object) restituito dal server. <br/> È possibile accedere alle proprietà seguenti dall'oggetto [**Command**](/windows/desktop/lwef/the-command-object) :<br/> CharacterID <br/> Valore stringa che identifica il nome (ID) del carattere che ha ricevuto il comando. <br/> [**Nome**](name-property.md)<br/> Valore stringa che identifica il nome (ID) del comando.<br/> [**Attendibilità**](confidence-property.md)<br/> Valore long integer che indica il Punteggio di confidenza per il comando. <br/> [**Chiamata vocale**](voice-property.md) <br/> Valore stringa che identifica il testo vocale per il comando.<br/> Alt1Name <br/> Valore stringa che identifica il nome del comando successivo (secondo) migliore.<br/> Alt1Confidence <br/> Valore long integer che indica il Punteggio di confidenza per il successivo (secondo) comando migliore.<br/> Alt1Voice <br/> Valore stringa che identifica il testo vocale per la corrispondenza successiva del comando alternativo migliore.<br/> Alt2Name <br/> Valore stringa che identifica il nome della terza corrispondenza del comando migliore.<br/> Alt2Confidence <br/> Un long integer che identifica il Punteggio di confidenza per la terza corrispondenza di comando migliore.<br/> Alt2Voice <br/> Valore stringa che identifica il testo vocale per la terza corrispondenza del comando migliore.<br/> [**Conteggio**](count-property.md) <br/> Valore long integer che indica il numero di alternative restituite.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Il server invia una notifica a questo evento quando l'applicazione è di input-attivo e l'utente sceglie un comando in base al menu di scelta rapida dell'input parlato o del carattere. L'evento restituisce il numero di possibili comandi corrispondenti in [**count**](count-property.md) , nonché il nome, il Punteggio di confidenza e il testo vocale per tali corrispondenze.

Se l'input vocale attiva questo evento, il server restituisce una stringa che identifica la migliore corrispondenza nel parametro [**Name**](name-property.md) e la seconda e la terza corrispondenza migliore in Alt1Name e Alt2Name. Una stringa vuota indica che l'input non corrisponde ad alcun comando definito dall'applicazione; ad esempio, potrebbe trattarsi di uno dei comandi definiti dal server. Se il comando è stato corrispondente al comando dell'agente; ad esempio, Hide, viene restituita una stringa vuota nel parametro **Name** , ma si riceverà comunque il testo udito nel parametro [**Voice**](voice-property.md) .

È possibile che venga restituito lo stesso nome di comando in più di una voce. I parametri [**Confidence**](confidence-property.md), Alt1Confidence e Alt2Confidence restituiscono i punteggi relativi, nell'intervallo compreso tra-100 e 100, restituiti dal motore di riconoscimento vocale per ogni corrispondenza corrispondente. I parametri [**Voice**](voice-property.md), Alt1Voice e Alt2Voice restituiscono il testo vocale per cui il motore di riconoscimento vocale corrisponde a ogni alternativa. Se [**count**](count-property.md) restituisce zero (0), il server ha rilevato un input parlato, ma ha determinato che non esiste alcun comando corrispondente.

Se l'input vocale non è l'origine del comando, ad esempio se l'utente ha selezionato il comando dal menu di scelta rapida del carattere, il server restituisce il nome (ID) del comando selezionato nella proprietà [**nome**](name-property.md). Restituisce anche il valore del parametro [**Confidence**](confidence-property.md) come 100 e il valore dei parametri [**Voice**](voice-property.md) come stringa vuota (""). Alt1Name e Alt2Name restituiscono anche stringhe vuote. Alt1Confidence e Alt2Confidence restituiscono zero (0) e Alt1Voice e Alt2Voice restituiscono stringhe vuote. [**Count**](count-property.md) restituisce 1.

> [!Note]  
> Non tutti i motori di riconoscimento vocale possono restituire tutti i valori per tutti i parametri di questo evento. Rivolgersi al fornitore del motore per determinare se il motore supporta l'interfaccia di Microsoft Speech API per la restituzione di alternative e punteggi di confidenza.

 

 

