---
title: Panoramica degli stili di visualizzazione
description: In questo argomento vengono descritti gli stili visivi e vengono identificati i componenti di Windows che li supportano. Vengono inoltre illustrati i passaggi che è necessario eseguire per utilizzare gli stili di visualizzazione nelle applicazioni.
ms.assetid: 5B5D7BB6-684F-478D-BF5F-B8D18BBCFF2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5663730c752fbf16c4f229a031eafa0c65bb9dbb
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474669"
---
# <a name="visual-styles-overview"></a>Panoramica degli stili di visualizzazione

In questo argomento vengono descritti gli stili visivi e vengono identificati i componenti di Windows che li supportano. Vengono inoltre illustrati i passaggi che è necessario eseguire per utilizzare gli stili di visualizzazione nelle applicazioni. Questo argomento include le sezioni seguenti:

-   [Temi e stili di visualizzazione](#themes-and-visual-styles)
-   [Componenti degli stili di visualizzazione](#visual-styles-components)
-   [Requisiti delle applicazioni per il supporto degli stili di visualizzazione](#application-requirements-for-supporting-visual-styles)
-   [Argomenti correlati](#related-topics)

## <a name="themes-and-visual-styles"></a>Temi e stili di visualizzazione

Windows include diverse funzionalità che consentono agli utenti di personalizzare l'interfaccia utente per soddisfare le esigenze e le preferenze specifiche. Queste funzionalità includono temi, introdotti in Microsoft Plus. per Windows 95. Un tema è una raccolta di impostazioni selezionabile dall'utente che include lo sfondo, i cursori, i tipi di carattere, i suoni e le icone. Di seguito sono riportate alcune caratteristiche dei temi.

-   Le impostazioni del tema sono specificate nei file con estensione Theme con un formato simile a win.ini file.
-   Un fornitore di software indipendente (ISV) può creare e distribuire un file con estensione Theme con un prodotto.
-   Nelle versioni precedenti a Windows Vista, i file di tema vengono visualizzati nella scheda tema del pannello di controllo schermo. In Windows Vista e versioni successive i temi vengono visualizzati nel pannello di controllo della personalizzazione.

Per ulteriori informazioni sui file con estensione Theme, vedere il [formato del file di tema](themesfileformat-overview.md).

Uno stile di visualizzazione è una specifica che definisce l'aspetto dei controlli comuni di Windows. Gli stili di visualizzazione sono associati ai temi; ovvero, un file con estensione Theme contiene una sezione che specifica lo stile di visualizzazione da applicare quando il particolare tema è attivo. Di seguito sono riportate alcune caratteristiche degli stili di visualizzazione.

-   Gli utenti possono modificare lo stile di visualizzazione in qualsiasi momento selezionando un tema diverso.
-   È necessario usare l'API degli stili di visualizzazione per applicare lo stile di visualizzazione attualmente attivo ai controlli personalizzati o creati dal proprietario dell'applicazione, se presenti.
-   Le informazioni che definiscono uno stile di visualizzazione vengono archiviate in un file con estensione MSSTYLES. Microsoft non supporta la creazione di file con estensione MSSTYLES.


Nella figura seguente viene illustrata una semplice finestra di dialogo con una barra delle applicazioni su un desktop Windows 7 che utilizza il tema Windows Aero senza trasparenza. Poiché l'applicazione non è configurata per l'utilizzo degli stili di visualizzazione, i pulsanti vengono visualizzati allo stesso modo indipendentemente dalle impostazioni del tema.

![Screenshot di una finestra di dialogo con pulsanti che non usano la trasparenza](images/tb-wostyles.png)

Al contrario, nella figura seguente viene mostrata la stessa finestra di dialogo sullo stesso desktop, ma questa volta l'applicazione è stata configurata per l'utilizzo con gli stili di visualizzazione. Si noti l'aspetto diverso dei pulsanti nell'area client. I pulsanti hanno un aspetto diverso perché il sistema ha applicato gli stili di visualizzazione definiti nel tema Aero.

![Screenshot di una finestra di dialogo con pulsanti che usano la trasparenza](images/tb-withstyles.png)

Nell'esempio seguente viene illustrata una finestra di dialogo simile in un desktop di Windows 8. In Windows 8, gli stili di visualizzazione sono sempre attivati, quindi le app di Windows 8 li ottengono gratuitamente.

![Screenshot di una semplice finestra di dialogo sul desktop di Windows 8](images/tb-win8.png)

## <a name="visual-styles-components"></a>Componenti degli stili di visualizzazione

Gli stili di visualizzazione sono supportati dai componenti seguenti:

-   Versione 6 o successiva della libreria di controlli comuni (ComCtl32.dll)
-   API degli stili di visualizzazione implementata in UxTheme.dll
-   Servizio temi
-   Uno o più file di definizione dello stile di visualizzazione (. msstyles)

L'API degli stili di visualizzazione dipende da un servizio di sistema denominato Themes. La libreria di controlli comuni esegue una query sul servizio Themes per ottenere informazioni correlate allo stile e, fino a Windows 7, usa il servizio per eseguire il rendering dei controlli nello stile di visualizzazione corrente.

In Windows 8 e versioni successive, l'API degli stili di visualizzazione funziona ancora se il servizio temi è disattivato. Ciò significa che i controlli comuni e l'area non client di Windows avranno ancora stili di visualizzazione quando il servizio temi è disattivato. Le funzionalità di Windows 8 che richiedono ancora il servizio temi includono:

-   Modifica dello stile di visualizzazione, in genere tramite la pagina **personalizzazione** delle **impostazioni del PC**.
-   Ottimizzazioni delle prestazioni in relazione al cambio di utenti, alla disconnessione, alla chiusura e alla condivisione tra sessioni utente.

L'API degli stili di visualizzazione Ottiene le informazioni sullo stile dal file con estensione MSSTYLES associato al tema attualmente selezionato. Il file. msstyles contiene un set di metriche, tipi di carattere, colori e bitmap che definiscono uno stile di visualizzazione

## <a name="application-requirements-for-supporting-visual-styles"></a>Requisiti delle applicazioni per il supporto degli stili di visualizzazione

Per usare gli stili di visualizzazione, l'applicazione deve essere in esecuzione in un sistema operativo che contiene ComCtl32.dll versione 6 o successiva. Se si desidera che l'applicazione utilizzi ComCtl32.dll versione 6, è necessario aggiungere un manifesto dell'applicazione o una direttiva del compilatore per specificare che è necessario utilizzare la versione 6, se disponibile. Per informazioni su come creare un manifesto dell'applicazione che consenta all'applicazione di usare gli stili di visualizzazione, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

Per i controlli comuni, non è necessaria alcuna azione aggiuntiva per assicurarsi che i controlli siano visualizzati nello stile di visualizzazione preferito dell'utente.

Se l'applicazione contiene controlli personalizzati o creati dal proprietario, è necessario usare l'API degli stili di visualizzazione per recuperare informazioni sullo stile di visualizzazione attualmente attivo e disegnare i controlli in tale stile.

Per le versioni di Windows precedenti a Windows 8, le applicazioni in genere devono fornire due percorsi di codice distinti per il disegno di controlli personalizzati e creati dal proprietario. Un percorso di codice consente di disegnare i controlli quando un tema che usa stili di visualizzazione è attivo e un altro percorso di codice disegna i controlli quando il tema classico di Windows o un tema a contrasto elevato è attivo. In Windows 8, tuttavia, gli stili di visualizzazione sono sempre attivati, pertanto non è necessario separare i percorsi di codice. Le applicazioni manifeste per Windows 8 ottengono un contrasto elevato "gratuitamente". Per ulteriori informazioni, vedere [supporto di contrasto elevato temi](supporting-high-contrast-themes.md).

Per altre informazioni su, vedere [uso degli stili di visualizzazione con controlli personalizzati e Owner-Drawn](using-visual-styles.md) e [riferimenti agli stili visivi](uxctl-ref.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stili di visualizzazione](themes-overview.md)
</dt> </dl>

 

 




