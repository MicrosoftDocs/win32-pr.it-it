---
description: Le azioni personalizzate ICE comunicano chiamando MsiProcessMessage e pubblicando un messaggio di tipo INSTALLMESSAGE \_ USER.
ms.assetid: 36307589-de0e-4eaf-b439-e7ba3cd96fb3
title: Linee guida per i messaggi ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0951f8573fce1b9dbe81b107fba2f2beb674ed063fae53182a7d2694ded35abb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821671"
---
# <a name="ice-message-guidelines"></a>Linee guida per i messaggi ICE

Le azioni personalizzate ICE comunicano chiamando [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) e pubblicando un messaggio di tipo INSTALLMESSAGE \_ USER.

Quando si crea una stringa di messaggio per un'azione personalizzata ICE, formattare la stringa come indicato di seguito.

*Nome di ICE* <tab> *Tipo di messaggio* <tab> *Descrizione* <tab> *URL o percorso della Guida* <tab> *Nome tabella* <tab> *Nome colonna* <tab> *Chiave primaria* <tab> *Chiave primaria* <tab> *Chiave primaria* . . . (ripetere per tutte le chiavi primarie necessarie)

I primi tre campi della stringa sono obbligatori in ogni messaggio.

Il campo Tipo di messaggio specifica se ice segnala un errore, un errore, un avviso o un messaggio informativo.



| Valore | Tipo di messaggio                                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Messaggio di errore che segnala l'errore dell'azione personalizzata ICE.                                                                                                       |
| 1     | Messaggio di errore che segnala la creazione di database che causano un comportamento non corretto.                                                                                             |
| 2     | Messaggio di avviso che segnala la creazione di database che causa un comportamento non corretto in determinati casi. Gli avvisi possono anche segnalare effetti collaterali imprevisti della creazione di database. |
| 3     | Messaggio informativo.                                                                                                                                                |



 

Se la Guida non è disponibile, il campo URL della Guida potrebbe essere una stringa vuota.

I messaggi di errore e di avviso devono specificare i campi Nome tabella, Nome colonna e Chiave primaria. Se uno di questi campi viene omesso, tutti i campi che segue il primo campo vuoto devono essere lasciati fuori dal messaggio. Ad esempio, un nome di tabella viene fornito senza un nome di colonna e chiavi primarie o un nome di tabella e un nome di colonna senza chiavi primarie. Tuttavia, non è possibile usare un nome di colonna e chiavi primarie senza un nome di tabella. È possibile che siano elencate più chiavi primarie fino a quando a tutte le chiavi primarie della tabella non sono stati specificati valori.

## <a name="examples"></a>Esempio

Il primo messaggio illustrato [dall'esempio ICE in C++](sample-ice-in-c-.md):

"ICE01 \\ t3 \\ tCreated 29/04/1998 by <insert author's name here>".

Il secondo messaggio inviato dall'esempio ICE:

"ICE01 \\ t3 \\ tLast modified 05/06/1999 by <insert author's name here>".

Terzo messaggio pubblicato dall'esempio ICE.

"ICE01 \\ t3 \\ tSimple ICE to illustrating the ICE concept".

 

 



