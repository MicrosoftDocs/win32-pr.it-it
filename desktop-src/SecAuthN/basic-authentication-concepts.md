---
description: In un modello applicativo client/server, i client sono programmi che agiscono per conto degli utenti che necessitano di un'operazione eseguita.
ms.assetid: c3e38cd3-3749-4384-80ff-0551acfe1eec
title: Concetti relativi all'autenticazione di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d28aa1da3555561740dfd119603a42268ebf86056842788f7dbb1c473fe60e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141314"
---
# <a name="basic-authentication-concepts"></a>Concetti relativi all'autenticazione di base

In un modello applicativo client/server, i client sono programmi che agiscono per conto degli utenti che necessitano di un'operazione eseguita. Potrebbe trattarsi dell'apertura e dell'uso di un file, dell'accesso a una cassetta postale, dell'esecuzione di query su un database o della stampa di un documento. I server sono programmi che forniscono servizi ai client, ad esempio archiviazione file, gestione della posta elettronica, elaborazione di query e spooling di stampa. I client avviano l'azione, i server rispondono. In genere, un server è in ascolto su una porta di comunicazione in attesa che i client si connettano e chieda il servizio.

Nel modello di protocollo Kerberos ogni connessione al client/server inizia con l'autenticazione. Il client e il server effettuano a loro volta una sequenza di azioni progettata per indicare alla parte in ciascuna estremità della connessione che la parte nell'altra estremità è autentica. Se l'autenticazione ha esito positivo, viene completata l'installazione della sessione e viene stabilita una sessione client/server sicura.

Il protocollo Kerberos usa:

-   [Autenticazione con chiave](key-authentication.md)
-   [Authenticator messaggi](authenticator-messages.md)
-   [Distribuzione delle chiavi](key-distribution.md)
-   [Ticket di sessione](session-tickets.md)
-   [Ticket di concessione ticket](ticket-granting-tickets.md)

 

 



