---
description: Le azioni personalizzate del ghiaccio comunicano chiamando MsiProcessMessage e inviando un \_ messaggio di tipo utente INSTALLMESSAGE.
ms.assetid: 36307589-de0e-4eaf-b439-e7ba3cd96fb3
title: Linee guida per i messaggi di ghiaccio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4bee7dbf22184883e49da4d5a5f66f9debb577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966639"
---
# <a name="ice-message-guidelines"></a>Linee guida per i messaggi di ghiaccio

Le azioni personalizzate del ghiaccio comunicano chiamando [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) e inviando un \_ messaggio di tipo utente INSTALLMESSAGE.

Quando si crea una stringa di messaggio per un'azione personalizzata ICE, formattare la stringa come indicato di seguito.

*Nome del ghiaccio* <tab> *Tipo* <tab> di messaggio *Descrizione* <tab> di *URL o percorso* <tab> della Guida *Nome tabella* <tab> *Nome colonna* <tab> *Chiave primaria* <tab> *Chiave primaria* <tab> *Chiave primaria* . . . (ripetere per tutte le chiavi primarie necessarie)

I primi tre campi della stringa sono necessari in ogni messaggio.

Il campo tipo di messaggio specifica se il ghiaccio segnala un errore, un errore, un avviso o un messaggio informativo.



| Valore | Tipo di messaggio                                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Messaggio di errore che segnala l'errore dell'azione personalizzata ICE.                                                                                                       |
| 1     | Segnalazione dei messaggi di errore creazione di un database che determina un comportamento non corretto.                                                                                             |
| 2     | Avviso che segnala la creazione di un database che causa un comportamento errato in alcuni casi. Gli avvisi possono anche segnalare effetti collaterali imprevisti della creazione di database. |
| 3     | Messaggio informativo.                                                                                                                                                |



 

Se la guida non è disponibile, il campo URL della guida può essere una stringa vuota.

I messaggi di errore e di avviso devono fornire il nome della tabella, il nome della colonna e i campi di chiave primaria. Se uno di questi campi viene omesso, tutti i campi che seguono il primo campo vuoto devono essere esclusi dal messaggio. Ad esempio, viene fornito un nome di tabella senza un nome di colonna e chiavi primarie oppure un nome di tabella e viene fornito un nome di colonna senza chiavi primarie. Tuttavia, non è possibile utilizzare un nome di colonna e chiavi primarie senza un nome di tabella. È possibile che vengano elencate più chiavi primarie fino a quando non sono state assegnate a tutte le chiavi primarie della tabella.

## <a name="examples"></a>Esempio

Il primo messaggio illustrato dal [ghiaccio di esempio in C++](sample-ice-in-c-.md):

"ICE01 \\ T3 \\ tcreato 04/29/1998 <inserire il nome dell'autore qui>".

Secondo messaggio inviato dal ghiaccio di esempio:

"ICE01 \\ T3 \\ tLast modificato 05/06/1999 da <inserire il nome dell'autore qui>".

Terzo messaggio inviato dall'esempio ICE.

"ICE01 \\ T3 \\ tSimple Ice per illustrare il concetto di ghiaccio".

 

 



