---
title: Client-Side progettazione
description: Lo script nelle pagine HTML sul lato server comunica con il client dell'Ordinamento guidato stampa online in cui è ospitato. Questa comunicazione viene eseguita tramite metodi e proprietà accessibili dall'oggetto window.external.
ms.assetid: fa76ccee-0b94-41b5-8cc8-eb7e1818dbed
keywords:
- pubblicazione guidata, progettazione lato client
- window.external, procedure guidate di pubblicazione
- pubblicazione guidata, window.external
- pubblicazione guidata,considerazioni sulla progettazione
- pubblicazione guidata, Online Print Ordering Wizard
- Online Print Ordering Wizard,client-side design
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c40aafc7a08820125df222c1c6d911b0d2b4d0a1fb625b7c62fc6d4be8bebd7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665081"
---
# <a name="client-side-design"></a>Client-Side progettazione

Lo script nelle pagine HTML sul lato server comunica con il client dell'Ordinamento guidato stampa online in cui è ospitato. Questa comunicazione viene eseguita tramite metodi e proprietà accessibili **dall'oggetto window.external.**

In questo documento vengono trattati gli argomenti seguenti.

-   [Metodi e proprietà](#methods-and-properties)
-   [Considerazioni sulla progettazione](#design-considerations)
-   [Argomenti correlati](#related-topics)

## <a name="methods-and-properties"></a>Metodi e proprietà

I metodi e le proprietà seguenti sono disponibili tramite **l'oggetto window.external.**

-   [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback)
-   [**FinalNext**](/windows/desktop/shell/iwebwizardhost-finalnext)
-   [**Annulla**](/windows/desktop/shell/iwebwizardhost-cancel)
-   [**PassportAuthenticate**](/windows/desktop/shell/inewwdevents-passportauthenticate)
-   [**SetHeaderText**](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [**SetWizardButtons**](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [**Didascalia**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))
-   [**Proprietà**](/windows/desktop/shell/iwebwizardhost-property)

Lo script della pagina lato server chiama questi metodi per notificare al client gli eventi durante la procedura di pubblicazione. Si esamini [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback) come esempio. Quando viene visualizzata la prima pagina HTML sul lato server, la procedura guidata ha la conoscenza degli handle per le pagine della procedura guidata che precedono e segue le pagine HTML ospitate. A questo punto dell'esempio, l'utente, che si trova nella prima pagina HTML, fa clic sul **pulsante** Indietro. La procedura guidata invia una notifica di questo evento al server. Alla ricezione di questo messaggio, lo script sul lato server fa riferimento al relativo gestore **OnBack** per questo evento, che, poiché si tratta della prima pagina HTML, chiama il **metodo FinalBack.** In questo modo la procedura guidata passa alla pagina della procedura guidata visualizzata prima di accedere all'interfaccia utente lato server.

Per una descrizione completa di questi metodi e proprietà, vedere la documentazione per gli oggetti [**WebWizardHost**](/windows/desktop/shell/webwizardhost) e [**NewWDEvents.**](/windows/desktop/shell/newwdevents)

## <a name="design-considerations"></a>Considerazioni sulla progettazione

Il codice HTML che rappresenta ogni pagina lato server viene visualizzato normalmente nel riquadro della procedura guidata. Quando si progettano queste pagine, tenere presente che non è possibile ridimensionare una finestra della procedura guidata. Le pagine devono quindi essere costruite e ridimensionate in modo che le barre di scorrimento siano evitate ogni volta che è possibile, per consentire all'utente di eseguire una navigazione uniforme nella procedura guidata.

Ogni pagina HTML deve inoltre fornire un gestore per gli eventi **OnBack,** **OnNext** **e OnCancel.** Il **gestore OnNext** gestirà anche l'evento **Finish.** Una pagina che non implementa una funzione **OnBack** viene considerata non valida e causa la visualizzazione di una pagina di errore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**WebWizardHost**](/windows/desktop/shell/webwizardhost)
</dt> <dt>

[**NewWDEvents**](/windows/desktop/shell/newwdevents)
</dt> <dt>

[Progettazione lato server](pubwiz-server.md)
</dt> </dl>

 

 