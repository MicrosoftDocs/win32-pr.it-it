---
title: Errori mciSendString
description: Errori mciSendString
ms.assetid: 286102bd-fcf3-425b-9adc-e0ca2d62e453
keywords:
- Valori restituiti MCIERR, errori mciSendString
- riferimenti multimediali, errori di mciSendString
- informazioni di riferimento per gli errori mciSendString e multimediali
- Interfaccia di controllo multimediale (MCI), errori di mciSendString
- MCI (interfaccia di controllo multimediale), errori di mciSendString
- informazioni di riferimento per MCI, errori di mciSendString
- Riferimento a MCI, errori di mciSendString
- Interfaccia di controllo multimediale (MCI), errori
- MCI (interfaccia di controllo multimediale), errori
- informazioni di riferimento per MCI, errori
- Riferimento a MCI, errori
- errori mciSendString
- mciSendString (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063db1986d3bff2416ad17886afb3b6281e20165
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872445"
---
# <a name="mcisendstring-errors"></a>Errori mciSendString

Gli errori seguenti vengono restituiti dalla funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) ma non da [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)):



| Valore                             | Significato                                           |
|-----------------------------------|---------------------------------------------------|
| costante MCIERR non \_ valida \_             | Il valore specificato per un parametro è sconosciuto.   |
| MCIERR \_ integer non valido \_              | Numero intero nel comando non valido o mancante. |
| \_flag duplicati MCIERR \_          | Un flag o un valore è stato specificato due volte.              |
| MCIERR \_ \_ stringa di comando mancante \_  | Non è stato specificato alcun comando.                         |
| MCIERR \_ \_ nome dispositivo \_ mancante     | Non è stato specificato alcun nome dispositivo.                     |
| MCIERR \_ \_ argomento stringa \_ mancante | Nel comando manca un valore stringa.      |
| MCIERR \_ nuovo \_ richiede \_ alias      | È necessario usare un alias con il nome del dispositivo "nuovo". |
| MCIERR \_ Nessuna \_ \_ virgoletta di chiusura        | Virgolette di chiusura mancanti.              |
| \_notifica MCIERR \_ per \_ \_ apertura automatica    | Il flag di notifica non è valido con l'apertura automatica.      |
| \_overflow param \_ MCIERR           | Lunghezza della stringa di output insufficiente.            |
| \_interno del parser MCIERR \_          | Si è verificato un errore interno del parser.                |
| \_parola chiave non riconosciuta MCIERR \_     | È stato specificato un parametro di comando sconosciuto.       |



 

 

 