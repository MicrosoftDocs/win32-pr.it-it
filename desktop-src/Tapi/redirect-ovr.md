---
description: Il reindirizzamento della sessione consente a un'applicazione di deflettere una sessione offerta in un altro indirizzo senza rispondere alla chiamata.
ms.assetid: b52cd5c2-fdd6-4240-b07b-b22733a89d27
title: reindirizzamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100ade9315c3b5e8e68c17bf34a0b6d54a9d9663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760808"
---
# <a name="redirect"></a>reindirizzamento

Il reindirizzamento della sessione consente a un'applicazione di deflettere una sessione offerta in un altro indirizzo senza rispondere alla chiamata. L'applicazione può eseguire il reindirizzamento in base a una chiamata. Ad esempio, un'applicazione potrebbe consentire a un utente di specificare reindirizzamenti diversi in base alle informazioni sull'ID chiamante. Dopo che una chiamata è stata reindirizzata correttamente, lo stato passa in genere a inattivo e le risorse associate devono essere rilasciate.

Il reindirizzamento differisce [da quello](forward-ovr.md) che una volta impostato, l'operazione viene eseguita da TAPI, dal provider di servizi o dallo switch senza ulteriore coinvolgimento dell'applicazione. Il reindirizzamento differisce dal [trasferimento](transfer-ovr.md) in quanto il reindirizzamento non richiede prima di tutto la risposta alla chiamata.

Non tutti i provider di servizi supportano l'utilizzo di questa operazione.

**TAPI 2. x:** Vedere [**lineRedirect**](/windows/win32/api/tapi/nf-tapi-lineredirect).

 

 
