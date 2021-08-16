---
description: Il reindirizzamento della sessione consente a un'applicazione di deviare una sessione offerta a un altro indirizzo senza rispondere alla chiamata.
ms.assetid: b52cd5c2-fdd6-4240-b07b-b22733a89d27
title: reindirizzamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ea44aaa10bc174784822032359d68d24ba01b6f7f1dcdf0fb211554107b8b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761205"
---
# <a name="redirect"></a>reindirizzamento

Il reindirizzamento della sessione consente a un'applicazione di deviare una sessione offerta a un altro indirizzo senza rispondere alla chiamata. L'applicazione può eseguire il reindirizzamento in base a una chiamata per chiamata. Ad esempio, un'applicazione potrebbe consentire a un utente di specificare reindirizzamenti diversi in base alle informazioni sull'ID chiamante. Dopo che una chiamata è stata reindirizzata correttamente, lo stato passa in genere a inattivo e le risorse associate devono essere rilasciate.

Il reindirizzamento [](forward-ovr.md) differisce da quello in avanti perché, dopo la configurazione dell'inoltro, l'operazione viene eseguita da TAPI, dal provider di servizi o dall'opzione senza coinvolgere ulteriormente l'applicazione. Il reindirizzamento è diverso [dal trasferimento](transfer-ovr.md) perché il reindirizzamento non richiede prima di tutto la risposta alla chiamata.

Non tutti i provider di servizi supportano l'uso di questa operazione.

**TAPI 2.x:** Vedere [**lineRedirect.**](/windows/win32/api/tapi/nf-tapi-lineredirect)

 

 
