---
title: Progettazione Server-Side
description: Le funzioni lato server comunicano con la creazione guidata client tramite l'oggetto Windows. External. Lo script lato server fornisce queste funzioni per rispondere agli eventi della procedura guidata e per recuperare informazioni sulla procedura guidata.
ms.assetid: 7cc8b814-f230-4326-a9df-a491ed35483e
keywords:
- pubblicazione guidata, progettazione lato server
- finestra. External, pubblicazione guidata
- procedure guidate di pubblicazione, finestra. esterno
- procedure guidate di pubblicazione, funzioni script di spostamento
- script, pubblicazione guidata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b3b218bbca297be446016335d90fe717a88bba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963089"
---
# <a name="server-side-design"></a>Progettazione Server-Side

Le funzioni lato server comunicano con la creazione guidata client tramite l'oggetto **Windows. External** . Lo script lato server fornisce queste funzioni per rispondere agli eventi della procedura guidata e per recuperare informazioni sulla procedura guidata.

In questo documento sono trattati gli argomenti seguenti.

-   [Implementazione di funzioni script di spostamento](#implementing-navigation-script-functions)
    -   [Onback ()](#onback)
    -   [OnNext ()](#onnext)
    -   [OnCancel ()](#oncancel)
-   [Altri metodi e proprietà](#other-methods-and-properties)
    -   [Metodi](#methods)
    -   [Proprietà](#properties)
-   [Argomenti correlati](#related-topics)

## <a name="implementing-navigation-script-functions"></a>Implementazione di funzioni script di spostamento

Script sul lato server in ogni pagina HTML risponde ai pulsanti di spostamento tramite le funzioni per **onback**, **OnNext** e **OnCancel**. Queste funzioni devono essere accessibili tramite **\_ lo script IHTMLDocument:: Get** nel client e non accettano parametri.

### <a name="onback"></a>Onback ()

-   Risponde quando l'utente fa clic **nuovamente** nella procedura guidata.
-   Se la pagina del lato server corrente è la prima pagina sul lato server, chiamare **Window. External. FinalBack** per indicare al client di passare alla pagina del lato client precedente.
-   Se la pagina del lato server corrente non è la prima pagina sul lato server, passare alla pagina precedente sul lato server.
-   Questa funzione deve essere implementata per ogni pagina. Le pagine che non riescono a eseguire questa operazione vengono considerate non valide e visualizzano una pagina di errore.

### <a name="onnext"></a>OnNext ()

-   Risponde quando l'utente fa clic su **Avanti** nella procedura guidata.
-   Se la pagina del lato server corrente è l'ultima pagina sul lato server, chiamare **Window. External. FinalNext** per indicare al client di passare alla pagina successiva sul lato client o completare la procedura guidata.
-   Se la pagina del lato server corrente non è l'ultima pagina sul lato server, passare alla pagina successiva sul lato server.

### <a name="oncancel"></a>OnCancel ()

-   Risponde quando l'utente fa clic su **Annulla** nella procedura guidata.
-   L'interfaccia utente deve essere progettata in modo che l'utente possa essere annullata in qualsiasi momento.
-   Una volta elaborate le elaborazioni nella funzione **OnCancel** , il client chiude la procedura guidata.

## <a name="other-methods-and-properties"></a>Altri metodi e proprietà

È possibile accedere alle funzioni implementate dal client tramite **Windows. External**, così come sono proprietà. I servizi disponibili sono i seguenti:

### <a name="methods"></a>Metodi

-   [**SetHeaderText**](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [**SetWizardButtons**](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [**PassportAuthenticate**](/windows/desktop/shell/inewwdevents-passportauthenticate)

### <a name="properties"></a>Proprietà

-   [**Didascalia**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))
-   [**Proprietà**](/windows/desktop/shell/iwebwizardhost-property)

Nell'esempio di codice riportato di seguito viene illustrato il codice sul lato server per una semplice pagina della procedura guidata che implementa la pagina di errore del servizio Web.


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

 

 