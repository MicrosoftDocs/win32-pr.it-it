---
description: Un dispositivo telefonico è un dispositivo che supporta la classe del dispositivo telefonico e che include hookswitches, Handset, vivavoce e auricolari.
ms.assetid: c2660d77-0265-49d4-bd04-1cddd674b760
title: Elementi telefono dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5744967dc738a65d7632dc1a1f6126bfbc9887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312711"
---
# <a name="phone-device-elements"></a>Elementi telefono dispositivo

Un dispositivo telefonico è un dispositivo che supporta la classe del dispositivo telefonico e che include alcuni o tutti gli elementi seguenti:

-   **Hookswitch/trasduttore**: si tratta di un mezzo per l'input e l'output audio. Un dispositivo telefonico può avere diversi trasduttori, che possono essere attivati e disattivati (Offhook o inseriti OnHook) in un'applicazione o in un controllo utente manuale.

    Telefonia identifica tre tipi di dispositivi hookswitch comuni a molti set di telefono:

     **Handset**: la combinazione di parti orale e ear tradizionale che deve essere sollevata manualmente da una culla e mantenuta sull'orecchio dell'utente.  
    **Vivavoce**: consente all'utente di effettuare chiamate gratuite. Il vivavoce può essere interno o esterno al dispositivo telefonico. La parte speaker di un vivavoce consente più listener.  
    **Auricolare**: consente all'utente di effettuare chiamate senza intervento.  
    

    Hookswitch deve essere Offhook per consentire l'invio e/o la ricezione di dati audio da parte del trasduttore corrispondente.

-   Controllo del volume/controllo di guadagno/mute: ogni dispositivo hookswitch è l'associazione di un altoparlante e di un componente Microphone. L'API fornisce il controllo del volume e il muting dei componenti del altoparlante e per ottenere il controllo o la muting dei componenti del microfono.
-   [Ringer](ring.md): consente di avvisare gli utenti, in genere tramite un campanello. Un dispositivo telefonico può essere in grado di squillare in diversi modi o modelli.
-   [Display](display.md): meccanismo per la presentazione visiva dei messaggi all'utente. Una visualizzazione telefono è caratterizzata dal numero di righe e colonne.
-   [Pulsanti di telefono](phone-buttons.md): una matrice di pulsanti. Ogni volta che l'utente preme un pulsante del set di telefono, l'API segnala che è stato premuto il pulsante corrispondente. Gli identificatori della lampada Button identificano una coppia di pulsanti e lampade. Naturalmente, è possibile che le coppie pulsante-lampada siano senza pulsante o nessuna lampada. Gli identificatori della lampada da pulsante sono valori integer compresi tra 0 e il numero massimo di lampade di pulsanti disponibili sul dispositivo telefonico, meno uno. Ogni pulsante appartiene a una classe Button. Le classi includono pulsanti per l'aspetto delle chiamate, pulsanti delle funzionalità, pulsanti del tastierino e pulsanti locali.
-   [Lampade](lamps.md): una matrice di lampade, ad esempio LED, controllabile singolarmente dall'API. Le lampade possono essere illuminate in modalità diverse variando la frequenza di accensione e spegnimento. L'identificatore della lampada pulsante identifica la lampada.
-   [Aree dati](data-areas.md): aree di memoria del dispositivo telefonico in cui è possibile scaricare e/o caricare i dati o il codice di istruzione da. Le informazioni scaricate influiscono sul comportamento (o, in altre parole, programma) sul dispositivo telefonico.

TAPI consente a un'applicazione di monitorare e controllare gli elementi del dispositivo telefonico. Gli elementi più utili per un'applicazione sono i dispositivi hookswitch. Il set di telefono può fungere da dispositivo di I/O audio (nel computer) con controllo del volume, ottenere il controllo e il silenziamento, un suoneria (per avvisare l'utente), aree dati (per la programmazione del telefono) ed eventualmente una visualizzazione, sebbene la visualizzazione del computer sia più idonea. Il writer di applicazioni è sconsigliato per il controllo diretto o l'uso di lampade telefoniche o pulsanti telefonici, perché le funzionalità LAMP e Button possono variare notevolmente tra set di telefono e le applicazioni possono essere rapidamente personalizzate su set di telefoni specifici.

Non è disponibile un set di servizi di base garantito supportato da tutti i dispositivi telefonici, come per i dispositivi lineari (i servizi di telefonia Basic). Pertanto, prima che un'applicazione possa usare un dispositivo telefonico, l'applicazione deve innanzitutto determinare le funzionalità esatte del dispositivo telefonico. Le funzionalità di telefonia variano in base alla configurazione (client/client/server), all'hardware telefonico e al software del provider di servizi. Le applicazioni non devono presupporre che siano disponibili funzionalità di telefonia. Un'applicazione determina le funzionalità del dispositivo di un dispositivo telefonico chiamando la funzione [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) . Le funzionalità del dispositivo del telefono indicano quali di questi elementi esistono per ogni dispositivo telefonico presente nel sistema e quali sono le rispettive funzionalità. Sebbene sia fortemente orientato verso i set di telefoni reali, questa astrazione può fornire un'implementazione significativa (o un sottoinsieme) per altri dispositivi. Prendere come esempio un auricolare separato direttamente connesso e controllabile dal computer e utilizzato come dispositivo telefonico. Le modifiche apportate a hookswitch possono essere attivate dal rilevamento di energia vocale (Offhook) o da un periodo di silenzio (OnHook); la suoneria può essere emulata dalla generazione di un segnale acustico nell'auricolare; una visualizzazione può essere emulata tramite la conversione da sintesi vocale.

Non è necessario realizzare un dispositivo telefonico nell'hardware, ma è possibile emularlo nel software utilizzando un'interfaccia di comando grafica basata su mouse o tastiera e l'altoparlante del computer o il sistema acustico. Un "telefono soft" può essere un'applicazione che usa TAPI. Può anche essere un provider di servizi, che può essere elencato come un dispositivo telefonico disponibile per altre applicazioni tramite l'API e, in quanto tale, viene assegnato un identificatore del dispositivo telefonico.

A seconda dell'ambiente e della configurazione, i set di telefono possono essere dispositivi condivisi tra l'applicazione e l'opzione. Nell'API viene effettuato un piccolo provisioning, in cui l'opzione può sospendere temporaneamente il controllo dell'API di un dispositivo telefonico.

 

 



