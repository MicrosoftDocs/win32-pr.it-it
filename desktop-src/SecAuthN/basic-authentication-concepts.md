---
description: In un modello di applicazione client/server, i client sono programmi che agiscono per conto di utenti che hanno bisogno di qualcosa.
ms.assetid: c3e38cd3-3749-4384-80ff-0551acfe1eec
title: Concetti di base sull'autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723cf42913906435c8dbc3c41950da8db8ece0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130430"
---
# <a name="basic-authentication-concepts"></a>Concetti di base sull'autenticazione

In un modello di applicazione client/server, i client sono programmi che agiscono per conto di utenti che hanno bisogno di qualcosa. Questo potrebbe essere l'apertura e l'utilizzo di un file, l'accesso a una cassetta postale, l'esecuzione di query su un database o la stampa di un documento. I server sono programmi che forniscono servizi ai client quali archiviazione file, gestione della posta elettronica, elaborazione di query e spooling di stampa. I client avviano un'azione, i server rispondono. In genere, un server è in ascolto su una porta di comunicazione in attesa che i client si connettano e chiedano il servizio.

Nel modello di protocollo Kerberos ogni connessione al client/server inizia con l'autenticazione. Il client e il server effettuano a loro volta una sequenza di azioni progettata per indicare alla parte in ciascuna estremità della connessione che la parte nell'altra estremità è autentica. Se l'autenticazione ha esito positivo, viene completata l'installazione della sessione e viene stabilita una sessione client/server sicura.

Il protocollo Kerberos si avvale di:

-   [Autenticazione della chiave](key-authentication.md)
-   [Messaggi di autenticazione](authenticator-messages.md)
-   [Distribuzione delle chiavi](key-distribution.md)
-   [Ticket di sessione](session-tickets.md)
-   [Ticket di concessione ticket](ticket-granting-tickets.md)

 

 



