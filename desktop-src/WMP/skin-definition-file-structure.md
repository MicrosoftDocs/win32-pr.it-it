---
title: Struttura del file di definizione dell'interfaccia
description: Struttura del file di definizione dell'interfaccia
ms.assetid: 6b9ea288-ec64-473b-b796-ab637517099a
keywords:
- Interfacce di Media Player di Windows, file di definizione dell'interfaccia
- interfacce, file di definizione dell'interfaccia
- file per le interfacce, definizione dell'interfaccia
- file di definizione dell'interfaccia, struttura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64226fb918bcbf93c95ece52075e2c8e7ed13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044981"
---
# <a name="skin-definition-file-structure"></a>Struttura del file di definizione dell'interfaccia

Il file di definizione dell'interfaccia deve seguire una struttura specifica. Si inizia con un elemento del **tema** , si creano uno o più elementi di **visualizzazione** e quindi si definisce ogni elemento di **visualizzazione** con gli elementi dell'interfaccia utente appropriati per il tipo di visualizzazione che si vuole usare.

## <a name="theme-elements"></a>Elementi del tema

Al livello principale, è necessario avviare il file di definizione dell'interfaccia con l'elemento del **tema** e chiuderlo.


```C++
<THEME>
    ...
</THEME>

```



L'elemento **Theme** è l'elemento radice dell'interfaccia personalizzata. In un file di definizione dell'interfaccia può essere presente un solo elemento **Theme** , che deve essere al livello principale. Gli elementi del **tema** hanno attributi specifici e di ambiente, sebbene nella maggior parte dei casi non sarà necessario usarli. Per ulteriori informazioni su questi attributi, vedere la Guida di riferimento per la [programmazione dell'interfaccia](skin-programming-reference.md).

## <a name="view-elements"></a>Elementi di visualizzazione

Ogni **tema** deve avere almeno un elemento di **visualizzazione** . L'elemento **View** regola l'immagine specifica visualizzata sullo schermo. Potrebbe essere necessario disporre di più di una visualizzazione, in modo che sia possibile spostarsi avanti e indietro. Ad esempio, potrebbe essere necessario disporre di una visualizzazione di grandi dimensioni per l'utilizzo di playlist, una visualizzazione media per il controllo delle visualizzazioni e una piccola visualizzazione che si riferisca a un angolo dello schermo.

Se si creano più visualizzazioni, è necessario assicurarsi che ogni vista disponga di un valore di attributo **ID** univoco che verrà usato per identificare la visualizzazione. È necessario definire l'attributo **BackgroundImage** o la visualizzazione non avrà un'immagine iniziale. Se non si desidera visualizzare un'immagine rettangolare, è probabile che si desideri utilizzare l'attributo **clippingColor** per definire le aree dell'interfaccia che non saranno visualizzate e sarà probabilmente necessario impostare **l'attributo del** titolo dell'elemento **View** .

Ogni elemento di **visualizzazione** può avere anche uno o più elementi della **visualizzazione** . Un elemento di **Sottovisualizzazione** è simile a una **visualizzazione** e può essere usato per parti dell'interfaccia che si desidera spostare, nascondere o mostrare. Ad esempio, è possibile usare un elemento di **visualizzazione** per creare una barra di scorrimento che estrae dall'interfaccia per visualizzare un equalizzatore grafico. Gli elementi di **visualizzazione subvisione** possono essere allineati con la **visualizzazione** e avere altre relazioni speciali con la **visualizzazione**.

## <a name="initializing-windows-media-player"></a>Inizializzazione di Windows Media Player

È possibile impostare determinate proprietà iniziali di Windows Media Player usando gli elementi **Player**, **Settings** e **Controls** . Ad esempio, è possibile impostare il volume su un livello iniziale o fornire un valore predefinito per un nome file.

Il codice seguente illustra come impostare il valore dell' **URL** in un'interfaccia personalizzata:


```C++
<PLAYER
  URL = "https://proseware.com/mellow.wma">
</PLAYER>

```



Se si desidera impostare l'attributo **autostart** delle **Impostazioni** su false, utilizzare il codice seguente:


```C++
<PLAYER>
  <SETTINGS
    autoStart = "False">
  </SETTINGS>
</PLAYER>

```



Si noti che l'elemento **Settings** è annidato all'interno dell'elemento **Player** .

Utilizzando questi elementi, è possibile specificare gli attributi e gli eventi seguenti in fase di progettazione:

**Attributi dell'elemento PLAYER**

-   **url**
-   **responseBuffering**
-   **Currentitemchange**
-   **Currentplaylistchange**
-   **Error (Errore) (Error (Errore)e)**
-   **Markerhit**
-   **Mediachange**
-   **Mediacollectionchange**
-   **Modechange**
-   **Mpenstatechange**
-   **Mlaylistchange**
-   **Mlaystatechange**
-   **Mositionchange**
-   **Mcriptcommand**
-   **Mtatuschange**

**Attributi dell'elemento SETTINGS**

-   **Avvio automatico**
-   **bilanciare**
-   **baseURL**
-   **defaultFrame**
-   **enableErrorDialogs**
-   **invokeURLs**
-   **mute**
-   **playCount**
-   **tasso**
-   **volume**

## <a name="controls-element-attributes"></a>Controlla gli attributi degli elementi

-   **currentMarker**
-   **currentPosition**

## <a name="other-user-interface-elements"></a>Altri elementi dell'interfaccia utente

Dopo aver definito il **tema** e gli elementi di **visualizzazione** , è necessario popolare la **visualizzazione** con elementi dell'interfaccia utente specifici. Non è necessario usare tutti gli elementi disponibili in un'interfaccia, solo quelli necessari.

Se un elemento può essere visualizzato dall'utente, viene chiamato controllo. Per le interfacce sono disponibili i controlli seguenti:

-   Pulsanti
-   Dispositivi di scorrimento, dispositivi di scorrimento personalizzati e barre di stato
-   Caselle di testo
-   Finestre video
-   Finestre di visualizzazione
-   Finestre playlist
-   Finestre di visualizzazione

Inoltre, è possibile usare diversi elementi per definire ulteriormente le azioni Media Player di Windows, ma richiedono elementi visivi come pulsanti o dispositivi di scorrimento:

-   Impostazioni video
-   Impostazioni equalizzatore
-   Impostazioni di visualizzazione

## <a name="buttons"></a>Pulsanti

I pulsanti sono la parte più comune di un'interfaccia. È possibile utilizzare i pulsanti per attivare azioni quali riproduzione, arresto, uscita, riduzione a icona e passaggio a una visualizzazione diversa. Windows Media Player fornisce l'autore dell'interfaccia con due tipi di elementi Button: l'elemento **Button** e l'elemento **ButtonGroup** . Sono inoltre disponibili diversi tipi predefiniti di pulsanti.

-   **Elemento BUTTON.** L'elemento **Button** viene usato per i singoli pulsanti. Se si usa l'elemento **Button** , è necessario fornire un'immagine per ogni pulsante e definire la posizione esatta in cui si desidera che il pulsante appaia rispetto all'immagine di sfondo. Uno dei vantaggi dell'elemento **Button** è la possibilità di modificare l'immagine del pulsante dinamicamente.
-   **Elemento BUTTONGROUP.** L'elemento **ButtonGroup** viene usato per i gruppi di pulsanti. Infatti, è necessario racchiudere ogni elemento **ButtonGroup** con una coppia di tag **ButtonGroup** . L'uso di gruppi di pulsanti è più semplice rispetto all'uso di singoli pulsanti, perché non è necessario specificare il percorso esatto per ciascun pulsante. Viene invece fornita una mappa immagine separata che definisce le azioni che si verificano quando il mouse passa sopra o fa clic su un'area sullo sfondo. L'uso di mappe di immagini è facile grazie al fatto che è possibile creare in background e copiarlo in un livello di mapping nel programma di modifica della grafica. L'uso del programma di modifica della grafica è più veloce e preciso rispetto al tentativo di definire esattamente la posizione di un singolo pulsante sullo sfondo.
-   **Pulsanti predefiniti.** Sono disponibili diversi pulsanti predefiniti. Ad esempio, è possibile usare un pulsante PLAYelement per riprodurre file multimediali digitali e un elemento STOPelement per arrestare la riproduzione. Vedere elemento [ButtonGroup](buttongroup-element.md) e [Button nell'elemento](button-element.md) Reference Programming Skin. Il [IMAGEBUTTON](imagebutton.md) può essere utilizzato per visualizzare le immagini che possono essere modificate in risposta a eventi specifici.

## <a name="sliders"></a>Dispositivi di scorrimento

I dispositivi di scorrimento sono utili per lavorare con le informazioni modificate nel tempo. Ad esempio, è possibile usare un dispositivo di scorrimento per indicare la quantità di musica già riprodotta per un determinato file multimediale. I dispositivi di scorrimento possono essere orizzontali, verticali, lineari o circolari o qualsiasi forma che può essere considerata. I dispositivi di scorrimento sono disponibili in tre tipi: i dispositivi di scorrimento, le barre di avanzamento e i dispositivi di scorrimento personalizzati.

-   **Scorrimento.** È possibile usare l'elemento **Slider** per i controlli volume o consentire all'utente di spostarsi in una parte diversa del contenuto multimediale.
-   **Indicatori di stato.** Gli indicatori di stato sono simili ai dispositivi di scorrimento. Gli indicatori di stato sono progettati per visualizzare graficamente la percentuale di un determinato processo completato, ma non per un processo con cui l'utente dovrà interagire. È ad esempio possibile utilizzare un indicatore di stato per indicare lo stato di avanzamento del buffer.
-   **Dispositivi di scorrimento personalizzati.** Viene fornita la funzionalità di dispositivo di scorrimento personalizzata, in modo da poter creare controlli come le manopole o eseguire meccanismi di controllo insoliti. Se, ad esempio, si desidera creare un controllo volume che esegue il wrapping dell'interfaccia, è possibile eseguire questa operazione con un dispositivo di scorrimento personalizzato. Per configurare il dispositivo di scorrimento personalizzato, è necessario creare una mappa immagine che contiene immagini di scala di grigi per definire le posizioni dei valori sul dispositivo di scorrimento. Questa operazione è relativamente semplice con un programma di modifica della grafica che supporta i livelli.

## <a name="text"></a>Testo

È possibile usare l'elemento di **testo** per visualizzare il testo sull'interfaccia, ad esempio i titoli delle canzoni.

## <a name="video"></a>Video

È possibile visualizzare il video nell'interfaccia. L'elemento **video** consente di impostare le dimensioni e la posizione della finestra del video.

È anche possibile consentire all'utente di modificare le impostazioni video con l'elemento **VIDEOSETTINGS** . Ad esempio, è possibile creare controlli per regolare la luminosità del video.

Se non si specifica un elemento video e il contenuto contiene video, Windows Media Player tornerà alla modalità Full e l'interfaccia non verrà visualizzata.

## <a name="equalizer-settings"></a>Impostazioni equalizzatore

È possibile impostare il filtro per bande di frequenza audio specifiche usando l'elemento **EQUALIZERSETTINGS** . È possibile aumentare i bassi, modificare gli acuti e configurare i suoni in modo che corrispondano alle orecchie o alla sala da lavoro.

## <a name="visualizations"></a>Visualizzazioni

È possibile visualizzare le visualizzazioni nell'interfaccia personalizzata. Le visualizzazioni sono effetti visivi che cambiano nel tempo quando l'audio viene riprodotto tramite Windows Media Player. L'elemento **Effects** determina la posizione in cui verranno riprodotte le visualizzazioni, le dimensioni della finestra e le visualizzazioni che verranno riprodotte.

## <a name="playlists"></a>Playlist

È possibile usare l'elemento **playlist** per consentire all'utente di selezionare un elemento da una playlist specifica.

## <a name="subviews"></a>Visualizzazioni secondarie

È possibile utilizzare l'elemento di **visualizzazione** secondaria per visualizzare set secondari di controlli dell'interfaccia, ad esempio una playlist o controlli video.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File di interfaccia**](skin-files.md)
</dt> </dl>

 

 




