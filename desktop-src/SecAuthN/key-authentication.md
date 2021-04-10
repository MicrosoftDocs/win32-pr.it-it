---
description: Molte forme di autenticazione si basano sull'idea che un'entità possa dimostrare la propria identità se è in grado di dimostrare che conosce una chiave, ad esempio una password, che può essere nota solo.
ms.assetid: e17e4eb7-133e-46a0-8247-00a58b88bf61
title: Autenticazione della chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deaadfdb61340955209ded22b5302e5436271ccc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231844"
---
# <a name="key-authentication"></a>Autenticazione della chiave

Molte forme di autenticazione si basano sull'idea che un'entità possa dimostrare la propria identità se è in grado di dimostrare che conosce una chiave, ad esempio una password, che può essere nota solo.

Le tecniche di autenticazione basate su un segreto, ad esempio una password, devono avere un modo per evitare che il segreto diventi una conoscenza pubblica. Un proprietario della password non può passare a una porta e fornire la password. Un utente oltre a portiere potrebbe essere in attesa; o potrebbe essere lo sportello errato. Per tenere un segreto, è necessario che un utente conosca la password senza rivelare la password. Si tratta dell'idea alla base dell'autenticazione con chiave privata, un metodo di verifica usato in tutto il [*protocollo Kerberos*](../secgloss/k-gly.md).

Si noti che il "segreto" nell'autenticazione con chiave privata è che il processo di autenticazione viene eseguita in segreto, ovvero senza mai rivelare effettivamente il contenuto della chiave.

Per il corretto funzionamento dell'autenticazione con chiave privata, le due parti di una transazione devono condividere una [*chiave di sessione*](../secgloss/s-gly.md) crittografica, che è anche segreta, nota solo a loro e a nessun'altra. La chiave è [*simmetrica*](../secgloss/s-gly.md). ovvero una singola chiave utilizzata sia per la crittografia che per la decrittografia. Una parte del processo di autenticazione dimostra la propria conoscenza della chiave mediante la crittografia di un messaggio. L'altra parte dimostra la propria conoscenza della chiave mediante la decrittografia del messaggio.

 

 
