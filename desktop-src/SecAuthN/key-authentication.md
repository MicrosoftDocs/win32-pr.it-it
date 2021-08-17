---
description: Molte forme di autenticazione si basano sull'idea che un'entità possa dimostrare la propria identità se può dimostrare di conoscere una chiave, ad esempio una password, che solo l'entità può conoscere.
ms.assetid: e17e4eb7-133e-46a0-8247-00a58b88bf61
title: Autenticazione della chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9273bc3fc57bca5157431ce78495f2b5c4b97595ed8513ba76fa068ef76fe0b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117787263"
---
# <a name="key-authentication"></a>Autenticazione della chiave

Molte forme di autenticazione si basano sull'idea che un'entità possa dimostrare la propria identità se può dimostrare di conoscere una chiave, ad esempio una password, che solo l'entità può conoscere.

Le tecniche di autenticazione che si basano su un segreto, ad esempio una password, devono avere un modo per evitare che il segreto diventi pubblico. Un proprietario della password non può raggiungere una porta e assegnare la password. Qualcuno accanto al portista potrebbe essere in ascolto; o potrebbe essere la porta sbagliata. Per mantenere un segreto, è necessario un modo per dimostrare che un utente conosce la password senza rivelarla. Questa è l'idea alla base dell'autenticazione con chiave privata, un metodo di verifica usato in tutto il [*protocollo Kerberos.*](../secgloss/k-gly.md)

Si noti che il "segreto" nell'autenticazione con chiave privata è che il processo di autenticazione avviene "in segreto", senza mai rivelare effettivamente il contenuto della chiave.

Per il funzionamento dell'autenticazione con chiave privata, le [](../secgloss/s-gly.md) due parti di una transazione devono condividere una chiave della sessione di crittografia che è anche un segreto, noto solo a loro e a nessun altro utente. La chiave è [*simmetrica.*](../secgloss/s-gly.md) si tratta di una singola chiave usata sia per la crittografia che per la decrittografia. Una parte del processo di autenticazione dimostra di conoscere la chiave crittografando un messaggio. L'altra parte dimostra di conoscere la chiave decrittografando il messaggio.

 

 
