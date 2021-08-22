---
title: Server-Side design
description: Le funzioni lato server comunicano con la procedura guidata client tramite l'oggetto windows.external. Lo script sul lato server fornisce queste funzioni per rispondere agli eventi della procedura guidata e recuperare informazioni sulla procedura guidata.
ms.assetid: 7cc8b814-f230-4326-a9df-a491ed35483e
keywords:
- procedure guidate di pubblicazione, progettazione lato server
- window.external, procedure guidate di pubblicazione
- procedure guidate di pubblicazione,window.external
- procedure guidate di pubblicazione, funzioni script di navigazione
- script, procedure guidate di pubblicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075e5a18b2150e504b6424fae2591ed83fdf707a6a20231b8f1186ddb6f3a67b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555811"
---
# <a name="server-side-design"></a>Server-Side design

Le funzioni lato server comunicano con la procedura guidata client tramite **l'oggetto windows.external.** Lo script sul lato server fornisce queste funzioni per rispondere agli eventi della procedura guidata e recuperare informazioni sulla procedura guidata.

Gli argomenti seguenti sono trattati in questo documento.

-   [Implementazione di funzioni di script di navigazione](#implementing-navigation-script-functions)
    -   [OnBack()](#onback)
    -   [OnNext()](#onnext)
    -   [OnCancel()](#oncancel)
-   [Altri metodi e proprietà](#other-methods-and-properties)
    -   [Metodi](#methods)
    -   [Proprietà](#properties)
-   [Argomenti correlati](#related-topics)

## <a name="implementing-navigation-script-functions"></a>Implementazione di funzioni di script di navigazione

Lo script sul lato server in ogni pagina HTML risponde ai pulsanti di spostamento tramite funzioni per **OnBack,** **OnNext** e **OnCancel.** Queste funzioni devono essere accessibili tramite **script IHTMLDocument::get \_** nel client e non accettano parametri.

### <a name="onback"></a>OnBack()

-   Risponde quando l'utente fa clic **su Indietro** nella procedura guidata.
-   Se la pagina sul lato server corrente è la prima pagina sul lato server, chiamare **window.external.FinalBack** per indicare al client di passare alla pagina sul lato client precedente.
-   Se la pagina sul lato server corrente non è la prima pagina sul lato server, passare alla pagina sul lato server precedente.
-   Questa funzione deve essere implementata per ogni pagina. Qualsiasi pagina che non riesce a eseguire questa operazione viene considerata non valida e visualizza una pagina di errore.

### <a name="onnext"></a>OnNext()

-   Risponde quando l'utente fa clic **su Avanti** nella procedura guidata.
-   Se la pagina sul lato server corrente è l'ultima pagina sul lato server, chiamare **window.external.FinalNext** per indicare al client di passare alla pagina successiva sul lato client o di completare la procedura guidata.
-   Se la pagina sul lato server corrente non è l'ultima pagina sul lato server, passare alla pagina successiva sul lato server.

### <a name="oncancel"></a>OnCancel()

-   Risponde quando l'utente fa clic **su Annulla** nella procedura guidata.
-   L'interfaccia utente deve essere progettata in modo che l'utente possa annullare in qualsiasi momento.
-   Dopo l'elaborazione di qualsiasi elaborazione nella **funzione OnCancel,** il client chiude la procedura guidata.

## <a name="other-methods-and-properties"></a>Altri metodi e proprietà

Le funzioni implementate dal client sono accessibili **tramite windows.external,** così come le proprietà. I servizi disponibili sono i seguenti:

### <a name="methods"></a>Metodi

-   [**SetHeaderText**](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [**SetWizardButtons**](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [**PassportAuthenticate**](/windows/desktop/shell/inewwdevents-passportauthenticate)

### <a name="properties"></a>Proprietà

-   [**Didascalia**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))
-   [**Proprietà**](/windows/desktop/shell/iwebwizardhost-property)

L'esempio di codice seguente illustra il codice lato server per una semplice pagina della procedura guidata che implementa la pagina di errore del servizio Web.


```
<html>
    <head>
        <script language="JavaScript">
            function window.onload()
            {
                window.external.SetWizardButtons(1, 0, 0);    
                <!-- Back button enabled -->
            }

            function window.onback()
            {
                window.external.FinalBack();
            }
        </script>
    </head>
.
.
.
</html>
                    
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione lato client](pubwiz-client.md)
</dt> <dt>

[Registrazione di un servizio](pubwiz-reg.md)
</dt> </dl>

 

 