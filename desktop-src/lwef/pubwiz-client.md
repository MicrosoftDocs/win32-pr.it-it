---
title: Progettazione Client-Side
description: Lo script nelle pagine HTML sul lato server comunica con il client della procedura guidata per l'ordine di stampa online in cui è ospitato. Questa comunicazione viene eseguita tramite i metodi e le proprietà a cui accede l'oggetto Window. External.
ms.assetid: fa76ccee-0b94-41b5-8cc8-eb7e1818dbed
keywords:
- pubblicazione guidata, progettazione lato client
- finestra. External, pubblicazione guidata
- procedure guidate di pubblicazione, finestra. esterno
- procedure guidate di pubblicazione, considerazioni sulla progettazione
- procedure guidate di pubblicazione, ordinamento guidato stampa online
- Ordinamento guidato stampa online, progettazione lato client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f794ee5f576077e0523f9a21101205ec789d4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963059"
---
# <a name="client-side-design"></a>Progettazione Client-Side

Lo script nelle pagine HTML sul lato server comunica con il client della procedura guidata per l'ordine di stampa online in cui è ospitato. Questa comunicazione viene eseguita tramite i metodi e le proprietà a cui accede l'oggetto **Window. External** .

In questo documento sono trattati gli argomenti seguenti.

-   [Metodi e proprietà](#methods-and-properties)
-   [Considerazioni sulla progettazione](#design-considerations)
-   [Argomenti correlati](#related-topics)

## <a name="methods-and-properties"></a>Metodi e proprietà

I metodi e le proprietà seguenti sono disponibili tramite l'oggetto **Window. External** .

-   [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback)
-   [**FinalNext**](/windows/desktop/shell/iwebwizardhost-finalnext)
-   [**Annulla**](/windows/desktop/shell/iwebwizardhost-cancel)
-   [**PassportAuthenticate**](/windows/desktop/shell/inewwdevents-passportauthenticate)
-   [**SetHeaderText**](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [**SetWizardButtons**](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [**Didascalia**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))
-   [**Proprietà**](/windows/desktop/shell/iwebwizardhost-property)

Lo script della pagina lato server chiama questi metodi per notificare al client gli eventi durante la procedura di pubblicazione. Si osservi ora [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback) come esempio. Quando viene visualizzata la prima pagina HTML sul lato server, la procedura guidata include le informazioni sugli handle per le pagine della procedura guidata precedenti e successive alle pagine HTML ospitate. A questo punto dell'esempio, l'utente, seduto alla prima pagina HTML, fa clic sul pulsante **indietro** . La procedura guidata invia una notifica di questo evento al server. Alla ricezione di questo messaggio, lo script sul lato server fa riferimento al relativo gestore **onback** per questo evento, che, poiché questa è la prima pagina HTML, chiama il metodo **FinalBack** . In questo modo verrà visualizzata la pagina della procedura guidata prima di accedere all'interfaccia utente sul lato server.

Per una descrizione completa di questi metodi e proprietà, vedere la documentazione relativa agli oggetti [**WebWizardHost**](/windows/desktop/shell/webwizardhost) e [**NewWDEvents**](/windows/desktop/shell/newwdevents) .

## <a name="design-considerations"></a>Considerazioni sulla progettazione

Il codice HTML che crea ogni pagina sul lato server viene visualizzato normalmente nel riquadro della procedura guidata. Quando si progettano queste pagine, tenere presente che non è possibile ridimensionare una finestra della procedura guidata. Le pagine devono pertanto essere costruite e dimensionate in modo che le barre di scorrimento vengano evitate quando possibile per fornire all'utente una navigazione uniforme nella procedura guidata.

Ogni pagina HTML deve anche fornire un gestore per gli eventi **onback**, **OnNext** e **OnCancel** . Il gestore **OnNext** gestirà anche l'evento **Finish** . Una pagina che non implementa una funzione **onback** viene considerata non valida e comporterà la visualizzazione di una pagina di errore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**WebWizardHost**](/windows/desktop/shell/webwizardhost)
</dt> <dt>

[**NewWDEvents**](/windows/desktop/shell/newwdevents)
</dt> <dt>

[Progettazione lato server](pubwiz-server.md)
</dt> </dl>

 

 