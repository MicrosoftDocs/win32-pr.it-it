---
title: Panoramica degli stili di visualizzazione
description: Questo argomento descrive gli stili di visualizzazione e identifica Windows componenti che li supportano. Vengono inoltre illustrati i passaggi da eseguire per usare gli stili di visualizzazione nelle applicazioni.
ms.assetid: 5B5D7BB6-684F-478D-BF5F-B8D18BBCFF2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 237ac858e1a60e615a6af177728102fb7e6ea1737a3a2d94d93091264b02121a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077727"
---
# <a name="visual-styles-overview"></a>Panoramica degli stili di visualizzazione

Questo argomento descrive gli stili di visualizzazione e identifica Windows componenti che li supportano. Vengono inoltre illustrati i passaggi da eseguire per usare gli stili di visualizzazione nelle applicazioni. Questo argomento include le sezioni seguenti:

-   [Temi e stili di visualizzazione](#themes-and-visual-styles)
-   [Componenti degli stili di visualizzazione](#visual-styles-components)
-   [Requisiti dell'applicazione per il supporto degli stili di visualizzazione](#application-requirements-for-supporting-visual-styles)
-   [Argomenti correlati](#related-topics)

## <a name="themes-and-visual-styles"></a>Temi e stili di visualizzazione

Windows include diverse funzionalità che consentono agli utenti di personalizzare l'interfaccia utente in base alle proprie esigenze e preferenze. Queste funzionalità includono i temi, che sono stati introdotti in Microsoft Plus! per Windows 95. Un tema è una raccolta selezionabile dall'utente di impostazioni che include sfondo, cursori, tipi di carattere, suoni e icone. Di seguito sono riportate alcune caratteristiche dei temi.

-   Le impostazioni del tema vengono specificate nei file con estensione theme con un formato simile a win.ini file.
-   Un fornitore di software indipendente (ISV) può creare e distribuire un file con estensione theme con un prodotto.
-   Nelle versioni precedenti Windows Vista, i file del tema vengono visualizzati nella scheda Tema del pannello di controllo Schermo. In Windows Vista e versioni successive, i temi vengono visualizzati nel pannello di controllo Personalizzazione.

Per altre informazioni sui file con estensione theme, vedere [Formato di file del tema](themesfileformat-overview.md).

Uno stile di visualizzazione è una specifica che definisce l'aspetto dei controlli Windows comuni. Gli stili di visualizzazione sono associati ai temi. in altri casi, un file con estensione theme contiene una sezione che specifica lo stile di visualizzazione da applicare quando il tema specifico è attivo. Di seguito sono riportate alcune caratteristiche degli stili di visualizzazione.

-   Gli utenti possono modificare lo stile di visualizzazione in qualsiasi momento selezionando un tema diverso.
-   È necessario usare l'API degli stili di visualizzazione per applicare lo stile di visualizzazione attualmente attivo ai controlli personalizzati o disegnati dal proprietario dell'applicazione, se presenti.
-   Le informazioni che definiscono uno stile di visualizzazione vengono archiviate in un file con estensione msstyles. Microsoft non supporta la creazione di file con estensione msstyles.


La figura seguente mostra una semplice finestra di dialogo con una barra delle applicazioni, in un desktop Windows 7 che usa il tema Windows Aero senza trasparenza. Poiché l'applicazione non è configurata per l'uso degli stili di visualizzazione, i pulsanti vengono visualizzati allo stesso modo indipendentemente dalle impostazioni del tema.

![Screenshot di una finestra di dialogo con pulsanti che non usano la trasparenza](images/tb-wostyles.png)

La figura seguente mostra invece la stessa finestra di dialogo sullo stesso desktop, ma questa volta l'applicazione è stata configurata per l'utilizzo degli stili di visualizzazione. Si noti il diverso aspetto dei pulsanti nell'area client. I pulsanti hanno un aspetto diverso perché il sistema ha applicato gli stili di visualizzazione definiti nel tema Aero.

![Screenshot di una finestra di dialogo con pulsanti che usano la trasparenza](images/tb-withstyles.png)

L'esempio seguente mostra una finestra di dialogo simile in un Windows 8 desktop. In Windows 8, gli stili di visualizzazione sono sempre disponibili, quindi Windows 8 le app ottengono il testo "gratuitamente".

![Screenshot di una semplice finestra di dialogo sul desktop di Windows 8](images/tb-win8.png)

## <a name="visual-styles-components"></a>Componenti degli stili di visualizzazione

Gli stili di visualizzazione sono supportati dai componenti seguenti:

-   Versione 6 o successiva della libreria di controllo comune (ComCtl32.dll)
-   API degli stili di visualizzazione implementata in UxTheme.dll
-   Servizio Temi
-   Uno o più file di definizione dello stile di visualizzazione (con estensione msstyles)

L'API degli stili di visualizzazione dipende da un servizio di sistema denominato Temi. La libreria di controlli comune esegue una query sul servizio Temi per ottenere informazioni relative allo stile e, fino Windows 7, usa il servizio per eseguire il rendering dei controlli nello stile di visualizzazione corrente.

In Windows 8 e versioni successive, l'API degli stili di visualizzazione funziona ancora se il servizio Temi è disattivato. Ciò significa che i controlli comuni e l'area non client delle finestre avranno comunque stili di visualizzazione quando il servizio Temi è disattivato. Le Windows 8 funzionalità che richiedono ancora il servizio Temi includono:

-   Modifica dello stile di visualizzazione, in genere tramite la **pagina Personalizzazione** di **PC Impostazioni**.
-   Ottimizzazioni delle prestazioni relative al cambio di utenti, alla disconnessione, all'arresto e alla condivisione tra sessioni utente.

L'API degli stili di visualizzazione ottiene informazioni sullo stile dal file msstyles associato al tema attualmente selezionato. Il file msstyles contiene un set di metriche, tipi di carattere, colori e bitmap che definiscono uno stile di visualizzazione

## <a name="application-requirements-for-supporting-visual-styles"></a>Requisiti dell'applicazione per il supporto degli stili di visualizzazione

Per usare gli stili di visualizzazione, l'applicazione deve essere in esecuzione in un sistema operativo che ComCtl32.dll versione 6 o successiva. Se si vuole che l'applicazione usi ComCtl32.dll versione 6, è necessario aggiungere un manifesto dell'applicazione o una direttiva del compilatore per specificare che deve essere usata la versione 6, se disponibile. Per informazioni su come creare un manifesto dell'applicazione che consente all'applicazione di usare gli stili di visualizzazione, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

Per i controlli comuni, non sono necessarie altre azioni per garantire che i controlli siano visualizzati nello stile di visualizzazione preferito dell'utente.

Se l'applicazione contiene controlli personalizzati o disegnati dal proprietario, è necessario usare l'API degli stili di visualizzazione per recuperare informazioni sullo stile di visualizzazione attualmente attivo e per disegnare i controlli in tale stile.

Per Windows versioni precedenti Windows 8, le applicazioni devono in genere fornire due percorsi di codice separati per disegnare controlli personalizzati e disegnati dal proprietario. Un percorso Windows di codice disegna i controlli quando un tema che usa gli stili di visualizzazione è attivo e un altro tracciato di codice disegna i controlli quando è attivo il tema classico o un tema a contrasto elevato. In Windows 8, tuttavia, gli stili di visualizzazione sono sempre disponibili, quindi non sono necessari percorsi di codice a titolo separato. Le applicazioni che si manifestano per Windows 8 a contrasto elevato "gratuitamente". Per altre informazioni, vedere [Supporting Contrasto elevato Themes](supporting-high-contrast-themes.md).

Per altre informazioni, vedere [Using Visual Styles with Custom and Owner-Drawn Controls](using-visual-styles.md) and Visual Styles [Reference](uxctl-ref.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stili di visualizzazione](themes-overview.md)
</dt> </dl>

 

 




