---
description: L'operazione di risposta è una risposta tipica delle applicazioni a una sessione di comunicazione offerta. Se ha esito positivo, questa operazione causa la transizione di una sessione nello stato connesso.
ms.assetid: 34ac0b34-1d1b-4657-a737-27a4ed9326af
title: Risposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e08081b32b7ba3a3a24cde3ec37c1a6118582cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529221"
---
# <a name="answer"></a>Risposta

L'operazione di risposta è la risposta tipica di un'applicazione a una sessione di comunicazione offerta. Se ha esito positivo, questa operazione causa la transizione di una sessione nello stato connesso.

In alcuni ambienti di telefonia (ad esempio ISDN), in cui gli avvisi utente sono separati dall'offerta di chiamata, l'applicazione ha la possibilità di [accettare](accept-ovr.md) una chiamata prima di rispondere o rifiutare ([eliminare](drop-ovr.md)) o [reindirizzare](redirect-ovr.md) la chiamata all' *offerta* .

Se viene eseguita un'operazione di risposta per una nuova sessione quando una sessione è già attiva, l'effetto della sessione attiva esistente dipende dalle funzionalità del provider di servizi. La prima chiamata può non essere interessata, può essere eliminata automaticamente oppure può essere automaticamente messa in attesa. TAPI invierà le notifiche degli eventi appropriate per entrambe le chiamate.

In una situazione con Bridge, se una chiamata è connessa ma nello stato attivo, è possibile aggiungerla usando l'operazione di risposta.

Se il provider di servizi lo supporta, l'applicazione ha la possibilità di inviare informazioni utente utente al momento della risposta.

**TAPI 2. x:** Vedere [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).

**TAPI 3. x:** Vedere [**ITBasicCallControl:: Answer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).

 

 
