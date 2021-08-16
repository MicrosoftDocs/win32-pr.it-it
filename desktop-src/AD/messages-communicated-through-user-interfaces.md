---
title: Messaggi comunicati tramite interfacce utente
description: In questo argomento vengono elencati i messaggi che un servizio directory può inviare da un'interfaccia utente.
ms.assetid: c81a3c44-c01d-4029-8a7d-6e0911d4f5ab
ms.tgt_platform: multiple
keywords:
- Messaggi comunicati tramite interfacce utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b20b2706ae9f03109064c459ce494fb38da3f4579ca8f5b03ade970fcb0391f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186573"
---
# <a name="messages-communicated-through-user-interfaces"></a>Messaggi comunicati tramite interfacce utente

In questo argomento vengono elencati i messaggi che un servizio directory può inviare da un'interfaccia utente.

## <a name="common-query-page-messages"></a>Messaggi comuni della pagina query

I messaggi seguenti vengono inviati a una pagina di estensione del modulo di query del servizio directory nella funzione di callback [**CQPageProc:**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)

-   [**CQPM \_ CLEARFORM**](cqpm-clearform.md)
-   [**CQPM \_ ENABLE**](cqpm-enable.md)
-   [**CQPM \_ GETPARAMETERS**](cqpm-getparameters.md)
-   [**CQPM \_ HANDLERSPECIFIC**](cqpm-handlerspecific.md)
-   [**Guida di \_ CQPM**](cqpm-help.md)
-   [**CQPM \_ INITIALIZE**](cqpm-initialize.md)
-   [**CQPM \_ PERSIST**](cqpm-persist.md)
-   [**VERSIONE \_ CQPM**](cqpm-release.md)
-   [**CQPM \_ SETDEFAULTPARAMETERS**](cqpm-setdefaultparameters.md)

## <a name="miscellaneous-messages"></a>Messaggi esterni

Nella tabella seguente sono elencati i messaggi che un servizio directory può inviare.



| Message                  | Valore                     | Descrizione                                                                                                                                                                                                                                   |
|--------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DSPROP \_ ATTRCHANGED \_ MSG | "DsPropAttrChanged"       | Messaggio inviato per la sincronizzazione delle pagine delle proprietà e degli strumenti di amministrazione del servizio directory, dichiarato in Dsclient.h.                                                                                                                       |
| DSQPM \_ GETCLASSLIST      | CQPM \_ HANDLERSPECIFIC+0   | Messaggio di pagina inviato alle pagine del modulo per il recupero di un elenco di classi per la query, usato dal selettore di campo e dall'area delle proprietà per compilare l'elenco delle classi di visualizzazione. wParam = flags e lParam = LPLPDSQUERYCLASSLIST, dichiarato in Dsquery.h. |
| ARGOMENTI DELLA GUIDA DI DSQPM \_        | (CQPM \_ HANDLERSPECIFIC+1) | Messaggio di pagina inviato alle pagine del modulo per la gestione della richiesta "Argomenti della Guida". wParam = 0, lParam = hWndParent, dichiarato in Dsquery.h.                                                                                                         |



 

 

 




