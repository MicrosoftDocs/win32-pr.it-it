---
description: Un dispositivo telefono è un dispositivo che supporta la classe di dispositivi telefonici e che include hookswitch, ricevitori, viva voce e visori.
ms.assetid: c2660d77-0265-49d4-bd04-1cddd674b760
title: Telefono Elementi del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c882e7f9ebe279d0ee6622708f8b735b68f4c37a2f93dffe2a870271d556cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774171"
---
# <a name="phone-device-elements"></a>Telefono Elementi del dispositivo

Un dispositivo telefono è un dispositivo che supporta la classe del dispositivo telefonico e che include alcuni o tutti gli elementi seguenti:

-   **Hookswitch/trasduttore:** si tratta di un mezzo per l'input e l'output audio. Un dispositivo telefono può avere diversi trasduttori, che possono essere attivati e disattivati (offhook o posizionati in onhook) sotto il controllo utente manuale o dell'applicazione.

    La telefonia identifica tre tipi di dispositivi hookswitch comuni a molti set di telefoni:

     **Ricevitore:** la tradizionale combinazione di bocche e orecchini che deve essere sollevata manualmente da una culla e mantenuta sull'udito dell'utente.  
    **Speakerphone**: consente all'utente di eseguire chiamate hands-free. La voce voce può essere interna o esterna al dispositivo telefonico. La parte speaker di un altoparlante consente più listener.  
    **Visore:** consente all'utente di eseguire chiamate hands-free.  
    

    Un hookswitch deve essere offhook per consentire l'invio e/o la ricezione dei dati audio dal trasduttore corrispondente.

-   Controllo volume/Controllo del guadagno/Disattivazione del microfono: ogni dispositivo hookswitch è l'associazione di un altoparlante e di un componente microfono. L'API fornisce il controllo del volume e la disattivazione dei componenti del parlante e per ottenere il controllo o la disattivazione dei componenti del microfono.
-   [Ringer:](ring.md)un mezzo per avvisare gli utenti, in genere tramite una campana. Un dispositivo telefono può essere in grado di eseguire il ring in un'ampia gamma di modalità o modelli.
-   [Display](display.md): meccanismo per la presentazione visiva dei messaggi all'utente. La visualizzazione di un telefono è caratterizzata dal numero di righe e colonne.
-   [Telefono pulsanti:](phone-buttons.md)matrice di pulsanti. Ogni volta che l'utente preme un pulsante sul set di telefoni, l'API segnala che è stato premuto il pulsante corrispondente. Gli identificatori a forma di pulsante identificano una coppia di pulsanti e lampioni. Naturalmente, è possibile avere coppie pulsante-lampe con nessun pulsante o nessuna lampadina. Gli identificatori della lampadina dei pulsanti sono valori interi che vanno da 0 al numero massimo di pulsanti-lampe disponibili nel dispositivo telefonico, meno uno. Ogni pulsante appartiene a una classe di pulsanti. Le classi includono i pulsanti di aspetto delle chiamate, i pulsanti delle funzionalità, i pulsanti del tastierino numerico e i pulsanti locali.
-   [Lamps](lamps.md): matrice di lampadine (ad esempio LED) controllabili singolarmente dall'API. Le lampadine possono essere accese in modalità diverse variando la frequenza di on e off. L'identificatore della lampadina del pulsante identifica la lampadina.
-   [Aree dati:](data-areas.md)aree di memoria nel dispositivo telefonico da cui è possibile scaricare e/o caricare dati o codice di istruzione. Le informazioni scaricate influiranno sul comportamento (o, in altre parole, sul programma) del dispositivo telefonico.

TAPI consente a un'applicazione di monitorare e controllare gli elementi del dispositivo telefonico. Gli elementi più utili per un'applicazione sono i dispositivi hookswitch. Il set di telefoni può fungere da dispositivo di I/O audio (al computer) con controllo del volume, controllo e disattivazione dell'audio, una suoneria (per avvisare l'utente), aree dati (per la programmazione del telefono) e, forse, uno schermo, anche se lo schermo del computer è più in grado di. L'autore dell'applicazione è sconsigliato dal controllo diretto o dall'uso di lampadine o pulsanti del telefono, perché le funzionalità delle lampadine e dei pulsanti possono variare notevolmente tra i set di telefoni e le applicazioni possono diventare rapidamente personalizzate per set di telefoni specifici.

Non esiste alcun set di servizi di base garantito supportato da tutti i dispositivi telefonici, come per i dispositivi line (i servizi Telefonia di base). Pertanto, prima che un'applicazione possa usare un dispositivo telefono, l'applicazione deve determinare le funzionalità esatte del dispositivo. La funzionalità di telefonia varia a seconda della configurazione (client e client/server), dell'hardware telefonico e del software del provider di servizi. Le applicazioni non devono presunzioni sulle funzionalità di telefonia disponibili. Un'applicazione determina le funzionalità del dispositivo di un dispositivo telefono chiamando la [**funzione phoneGetDevCaps.**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) Le funzionalità del dispositivo di un telefono indicano quali di questi elementi esistono per ogni dispositivo telefono presente nel sistema e quali sono le relative funzionalità. Sebbene fortemente orientata verso i set di telefoni reali, questa astrazione può fornire un'implementazione significativa (o subset) anche per altri dispositivi. Si consideri come esempio un visore separato direttamente connesso e controllabile dal computer e gestito come dispositivo telefonico. Le modifiche del hookswitch possono essere attivate dal rilevamento dell'energia vocale (offhook) o da un periodo di silenzio (onhook); il ringing può essere emulato dalla generazione di un segnale udibile nel visore; una visualizzazione può essere emulata tramite la conversione da testo a voce.

Un dispositivo telefono non deve essere realizzato nell'hardware, ma può essere emulato nel software usando un'interfaccia grafica basata su mouse o tastiera e il sistema audio o altoparlante del computer. Un "telefono soft" può essere un'applicazione che usa TAPI. Può anche essere un provider di servizi, che può essere elencato come dispositivo telefonico disponibile per altre applicazioni tramite l'API e di conseguenza viene assegnato un identificatore di dispositivo telefono.

A seconda dell'ambiente e della configurazione, i set di telefoni possono essere dispositivi condivisi tra l'applicazione e il commutatore. Viene effettuato un provisioning secondario nell'API in cui il commutatore può sospendere temporaneamente il controllo dell'API di un dispositivo telefono.

 

 



