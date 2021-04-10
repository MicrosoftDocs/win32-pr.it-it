---
description: L'operazione di attesa consente a un singolo indirizzo di gestire più sessioni di comunicazione.
ms.assetid: 65e22e4e-e346-41c2-929a-ba0d1f7f1732
title: Contenere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df54b246c5bde5914a14b53dd56b71688d92a5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879874"
---
# <a name="hold"></a>Contenere

L'operazione di attesa consente a un singolo indirizzo di gestire più sessioni di comunicazione. L'inserimento di una sessione in un disco rigido libera la riga o l'indirizzo dell'utente per effettuare altre chiamate. Non è in genere possibile trasferire o includere una chiamata su un disco rigido in una chiamata di conferenza, ma è possibile eseguire una chiamata di consultazione. Le chiamate di consultazione vengono avviate mediante operazioni di [conferenza](conference-ovr.md) o di [trasferimento](transfer-ovr.md) .

Dopo che una chiamata è stata posizionata correttamente in attesa, lo stato della chiamata passa in genere allo stato onHolding. Mentre è in attesa una chiamata, l'applicazione può ricevere messaggi sulle modifiche di stato della chiamata mantenuta. Se, ad esempio, l'entità tenuta si blocca, lo stato della chiamata può passare a disconnected.

In una situazione con Bridge, è possibile che l'operazione di attesa non inserisca effettivamente la chiamata in attesa. Lo stato di altre stazioni della chiamata può governare, ad esempio il tentativo di "mantenere" una chiamata quando non è possibile partecipare ad altre stazioni. al contrario, la chiamata può essere semplicemente modificata nello stato inattivo mentre rimane connessa in altre stazioni.

Non tutti i provider di servizi supportano l'utilizzo di questa operazione.

**TAPI 2. x:** Vedere [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold), [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold).

**TAPI 3. x:** Vedere [**ITBasicCallControl:: Holding**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold).

 

 
