---
description: L'operazione di blocco consente a un singolo indirizzo di gestire più sessioni di comunicazione.
ms.assetid: 65e22e4e-e346-41c2-929a-ba0d1f7f1732
title: Blocco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afacd6d9664e9a095a1e8b0c725dc0171da709fdecffb88b428231a5b5359a4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003639"
---
# <a name="hold"></a>Blocco

L'operazione di blocco consente a un singolo indirizzo di gestire più sessioni di comunicazione. L'inserimento di una sessione in un blocco rigido libera la riga o l'indirizzo dell'utente per effettuare altre chiamate. In genere, una chiamata in attesa non può essere trasferita o inclusa in una conferenza telefonica, ma può essere chiamata da una consulenza. Le chiamate di consulenza vengono avviate tramite [operazioni di](conference-ovr.md) conferenza [o](transfer-ovr.md) trasferimento.

Dopo che una chiamata è stata messa in attesa, lo stato della chiamata passa in genere allo stato di attesa. Mentre una chiamata è in attesa, l'applicazione può ricevere messaggi sulle modifiche di stato della chiamata mantenuta. Ad esempio, se l'entità mantenuta si blocca, lo stato della chiamata può passare a disconnesso.

In una situazione con bridge, l'operazione di blocco potrebbe non mettere effettivamente in attesa la chiamata. Lo stato di altre stazioni nella chiamata può essere regolato (ad esempio, il tentativo di "tenere" una chiamata quando altre stazioni partecipano non è possibile); al contrario, la chiamata può essere semplicemente modificata nello stato inattivo mentre rimane connessa ad altre stazioni.

Non tutti i provider di servizi supportano l'uso di questa operazione.

**TAPI 2.x:** Vedere [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold), [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold).

**TAPI 3.x:** Vedere [**ITBasicCallControl::Hold**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold).

 

 
