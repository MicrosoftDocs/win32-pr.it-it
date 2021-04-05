---
description: Le operazioni di connessione consentono a un'applicazione di inviare cifre aggiuntive in una sessione creata in precedenza. Un esempio di utilizzo della composizione parziale consiste nel comporre un'estensione. La composizione parziale viene a volte definita composizione incrementale o composizione ritardata.
ms.assetid: 1dfaefd7-f8dd-451e-af18-249c89bdb517
title: Dial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1c603d8e846694b4728d1b5ad4c887be34fbac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750778"
---
# <a name="dial"></a>Dial

Le operazioni di connessione consentono a un'applicazione di inviare cifre aggiuntive in una sessione creata in precedenza. Un esempio di utilizzo della composizione parziale consiste nel comporre un'estensione. La composizione parziale viene a volte definita composizione incrementale o composizione ritardata.

Quando l'indirizzo specificato è incompleto, la composizione di alcune cifre può essere posticipata inserendo un punto e virgola (;) alla fine del numero. Viene quindi usata un'operazione di connessione per inviare dati di indirizzo aggiuntivi nella sessione esistente, ad esempio la composizione dell'indirizzo di un'entità a cui verrà trasferita la chiamata.

Ogni provider di servizi deve rifiutare una stringa di connessione che contiene **?** e consentire all'applicazione di gestirla nel modo appropriato. Ad esempio, l'applicazione può usare la composizione parziale per comporre la stringa, fino a, ma senza includere **?** , quindi visualizzare una finestra di dialogo per consentire all'utente di segnalare quando il resto della stringa di connessione deve essere composto.

Un ulteriore motivo per cui un'applicazione può utilizzare la composizione parziale è se il provider di servizi non supporta uno o più caratteri di controllo del rilevamento dello stato di avanzamento della chiamata. Questi caratteri, che possono verificarsi in un indirizzo di connessione, sono W (attendi il tono di connessione); @ (attendi la risposta non interattiva); e $ (attendi il tono di richiesta della scheda chiamante). Questi e tutti gli altri caratteri utilizzati nelle stringhe di indirizzi sono descritti in modo più dettagliato negli [indirizzi di connessione](address-ovr.md).

Il provider indica i modificatori di stringa di composizione "Wait" supportati. Un'applicazione TAPI 2 trova questi dati nel membro **dwDevCapFlags** della struttura [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps) restituita da [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps). Un'applicazione TAPI 3 chiama [**ITAddressCapabilities:: Get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) con *AddressCap* impostato sul membro **AC \_ DEVCAPFLAGS** della [**\_ funzionalità Address**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability).

L'applicazione può scegliere di preanalizzare le stringhe comparabili per i caratteri non supportati oppure può passare la stringa "non elaborata" come parte dell'avvio di una sessione. Se la stringa contiene un modificatore non supportato o un "?", il provider restituirà un errore che indica il modificatore che causa il problema prima all'interno della stringa:

-   \_DIALBILLING LINEERR
-   \_DIALQUIET LINEERR
-   \_DIALDIALTONE LINEERR
-   \_DIALPROMPT LINEERR

L'applicazione può quindi individuare il modificatore offensivo nella stringa, prendere le cifre a sinistra del modificatore, aggiungere un punto e virgola e avviare una sessione usando l'indirizzo parziale. Il resto della stringa può essere inviato usando l'operazione di connessione.

Non tutti i provider di servizi supportano l'utilizzo di questa operazione.

**TAPI 2. x:** Vedere [**lineDial**](/windows/win32/api/tapi/nf-tapi-linedial).

**TAPI 3. x:** Vedere [**ITBasicCallControl::D IAL**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-dial).

 

 
