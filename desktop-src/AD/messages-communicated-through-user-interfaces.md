---
title: Messaggi comunicati tramite interfacce utente
description: In questo argomento sono elencati i messaggi che un servizio directory può inviare da un'interfaccia utente.
ms.assetid: c81a3c44-c01d-4029-8a7d-6e0911d4f5ab
ms.tgt_platform: multiple
keywords:
- Messaggi comunicati tramite interfacce utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab0d01717129db284f05b2361b2a067d611a33e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044108"
---
# <a name="messages-communicated-through-user-interfaces"></a>Messaggi comunicati tramite interfacce utente

In questo argomento sono elencati i messaggi che un servizio directory può inviare da un'interfaccia utente.

## <a name="common-query-page-messages"></a>Messaggi della pagina di query comuni

I messaggi seguenti vengono inviati a una pagina di estensione del modulo di query del servizio directory nella funzione di callback [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) :

-   [**\_CLEARFORM CQPM**](cqpm-clearform.md)
-   [**\_Abilitazione di CQPM**](cqpm-enable.md)
-   [**CQPM \_ GETparameters**](cqpm-getparameters.md)
-   [**\_HANDLERSPECIFIC CQPM**](cqpm-handlerspecific.md)
-   [**Guida di CQPM \_**](cqpm-help.md)
-   [**\_inizializzazione CQPM**](cqpm-initialize.md)
-   [**CQPM \_ permanente**](cqpm-persist.md)
-   [**versione di CQPM \_**](cqpm-release.md)
-   [**\_SETDEFAULTPARAMETERS CQPM**](cqpm-setdefaultparameters.md)

## <a name="miscellaneous-messages"></a>Messaggi esterni

Nella tabella seguente sono elencati i messaggi che possono essere inviati da un servizio directory.



| Message                  | Valore                     | Descrizione                                                                                                                                                                                                                                   |
|--------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_messaggio DSPROP ATTRCHANGED \_ | "DsPropAttrChanged"       | Messaggio inviato per sincronizzare le pagine delle proprietà e gli strumenti di amministrazione del servizio directory, dichiarati in DSClient. h.                                                                                                                       |
| GetClass DSQPM \_      | CQPM \_ HANDLERSPECIFIC + 0   | Messaggio di pagina inviato alle pagine del modulo per il recupero di un elenco di classi per la query, usato dal selettore dei campi e dalla proprietà per compilare l'elenco delle classi di visualizzazione. wParam = Flags e lParam = LPLPDSQUERYCLASSLIST, dichiarati in dsquery. h. |
| \_HELPTOPICS DSQPM        | (CQPM \_ HANDLERSPECIFIC + 1) | Un messaggio di pagina inviato alle pagine del modulo per la gestione della richiesta "argomenti della Guida". wParam = 0, lParam = hWndParent, dichiarato in dsquery. h.                                                                                                         |



 

 

 




