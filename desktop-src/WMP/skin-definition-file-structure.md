---
title: Struttura del file di definizione dell'interfaccia
description: Struttura del file di definizione dell'interfaccia
ms.assetid: 6b9ea288-ec64-473b-b796-ab637517099a
keywords:
- Windows Media Player, file di definizione dell'interfaccia
- skins, file di definizione dell'interfaccia
- file per le interfaccia, definizione dell'interfaccia
- file di definizione dell'interfaccia, struttura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c708e46f93e2d00820015a04b0f467da2deafe59e4dbafb0b9e4f3fb8660271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995281"
---
# <a name="skin-definition-file-structure"></a>Struttura del file di definizione dell'interfaccia

Il file di definizione dell'interfaccia deve seguire una struttura specifica. Si inizia con un **elemento THEME,** si creano uno o più elementi **VIEW** e quindi si definisce ogni elemento **VIEW** con gli elementi dell'interfaccia utente appropriati per il tipo di visualizzazione che si vuole usare.

## <a name="theme-elements"></a>Elementi THEME

Al livello superiore, è necessario avviare il file di definizione dell'interfaccia con **l'elemento THEME** e chiuderlo.


```C++
<THEME>
    ...
</THEME>

```



**L'elemento THEME** è l'elemento radice per l'interfaccia. Può essere presente un solo **elemento THEME** in un file di definizione dell'interfaccia e deve essere al primo livello. **Gli** elementi THEME hanno attributi specifici e di ambiente, anche se nella maggior parte dei casi non è necessario usarli. Per altre informazioni su questi attributi, vedere Le informazioni [di riferimento sulla programmazione dell'interfaccia](skin-programming-reference.md).

## <a name="view-elements"></a>Elementi VIEW

Ogni **THEME** deve avere almeno un **elemento VIEW.** **L'elemento VIEW** determina la particolare immagine visualizzata sullo schermo. È possibile avere più di una visualizzazione, quindi è possibile passare da una visualizzazione all'altra. Ad esempio, è possibile avere una visualizzazione di grandi dimensioni per l'uso delle playlist, una visualizzazione media per il controllo delle visualizzazioni e una visualizzazione di piccole dimensioni che si adatta a un angolo dello schermo.

Se si creano più viste, è necessario assicurarsi che ogni vista abbia un valore di attributo **ID** univoco che verrà usato per identificare la vista. È necessario definire **l'attributo backgroundImage** oppure la visualizzazione non avrà un'immagine iniziale. Se non si vuole visualizzare un'immagine rettangolare, è probabile che si voglia usare l'attributo **clippingColor** per definire le aree dell'interfaccia che non verranno visualizzate ed è probabile che si voglia impostare l'attributo **titleBar** dell'elemento **VIEW.**

Ogni **elemento VIEW** può anche avere uno o più elementi **SUBVIEW.** Un **elemento SUBVIEW** è simile a **un elemento VIEW** e può essere usato per parti dell'interfaccia che vuoi spostare, nascondere o mostrare. Ad esempio, un **elemento SUBVIEW** può essere usato per creare una barra temporale scorrevole che esce dall'interfaccia per visualizzare un equalizzatore grafico. **Gli elementi SUBVIEW** possono essere allineati a **VIEW** e avere altre relazioni speciali con **VIEW.**

## <a name="initializing-windows-media-player"></a>Inizializzazione di Windows Media Player

È possibile impostare determinate proprietà iniziali Windows Media Player usando gli elementi **PLAYER,** **SETTINGS** e **CONTROLS.** Ad esempio, è possibile impostare il volume su un livello iniziale o assegnare un valore predefinito per un nome file.

Il codice seguente illustra come impostare il valore **dell'URL** in un'interfaccia:


```C++
<PLAYER
  URL = "https://proseware.com/mellow.wma">
</PLAYER>

```



Se si vuole impostare **l'attributo autoStart** di **SETTINGS** su False, usare il codice seguente:


```C++
<PLAYER>
  <SETTINGS
    autoStart = "False">
  </SETTINGS>
</PLAYER>

```



Si noti che **l'elemento SETTINGS** è annidato all'interno **dell'elemento PLAYER.**

Usando questi elementi, è possibile specificare gli attributi e gli eventi seguenti in fase di progettazione:

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

-   **Autostart**
-   **Equilibrio**
-   **baseURL**
-   **defaultFrame**
-   **enableErrorDialogs**
-   **invokeURLs**
-   **Muto**
-   **playCount**
-   **Tasso**
-   **Volume**

## <a name="controls-element-attributes"></a>Attributi degli elementi CONTROLS

-   **currentMarker**
-   **currentPosition**

## <a name="other-user-interface-elements"></a>Altri elementi Interfaccia utente

Dopo aver definito gli elementi **THEME** e **VIEW,** è necessario popolare **view** con elementi dell'interfaccia utente specifici. Non è necessario usare tutti gli elementi disponibili in un'interfaccia, ma solo quelli necessari.

Se un elemento può essere visualizzato dall'utente, viene chiamato controllo . Per le interfaccia sono disponibili i controlli seguenti:

-   Pulsanti
-   Dispositivi di scorrimento, dispositivi di scorrimento personalizzati e indicatori di stato
-   Caselle di testo
-   Finestre video
-   Finestre di visualizzazione
-   Finestre playlist
-   Finestre della visualizzazione secondaria

Inoltre, diversi elementi possono essere usati per definire ulteriormente le Windows Media Player, ma richiedono elementi visivi come pulsanti o dispositivi di scorrimento:

-   Impostazioni video
-   Equalizer Impostazioni
-   Impostazioni di visualizzazione

## <a name="buttons"></a>Pulsanti

I pulsanti sono la parte più comune di un'interfaccia. È possibile usare i pulsanti per attivare azioni quali riproduzione, arresto, chiusura, riduzione a icona e passaggio a una visualizzazione diversa. Windows Media Player l'autore dell'interfaccia con due tipi di elementi pulsante: **l'elemento BUTTON** e l'elemento **BUTTONGROUP.** Sono inoltre disponibili diversi tipi predefiniti di pulsanti.

-   **Elemento BUTTON.** **L'elemento BUTTON** viene usato per i singoli pulsanti. Se si usa **l'elemento BUTTON,** è necessario fornire un'immagine per ogni pulsante e definire la posizione esatta in cui si vuole che il pulsante venga visualizzato rispetto all'immagine di sfondo. Uno dei vantaggi dell'elemento **BUTTON** è la modifica dinamica dell'immagine del pulsante.
-   **Elemento BUTTONGROUP.** **L'elemento BUTTONGROUP** viene usato per i gruppi di pulsanti. In realtà, è necessario racchiudere ogni **elemento BUTTONGROUP** con una coppia di **tag BUTTONGROUP.** L'uso dei gruppi di pulsanti è più semplice rispetto all'uso di singoli pulsanti perché non è necessario specificare la posizione esatta per ogni pulsante. È invece possibile specificare una mappa immagine separata che definisce le azioni che verranno eseguite quando il puntatore del mouse viene posizionato o fa clic su un'area sullo sfondo. L'uso delle mappe immagine è semplice perché è possibile copiare l'immagine creata per lo sfondo in un livello di mapping nel programma di modifica grafica. L'uso del programma di modifica grafica è più veloce e preciso rispetto al tentativo di definire esattamente dove deve essere posizionato un singolo pulsante sullo sfondo.
-   **Pulsanti predefiniti.** Sono disponibili diversi pulsanti predefiniti. Ad esempio, è possibile usare un pulsante PLAYELEMENT per riprodurre file multimediali digitali e un elemento STOPELEMENT per arrestare la riproduzione. Vedere [Elemento BUTTONGROUP](buttongroup-element.md) ed [elemento BUTTON](button-element.md) nelle informazioni di riferimento sulla programmazione dell'interfaccia utente. ImageBUTTON [può](imagebutton.md) essere usato per visualizzare immagini che possono cambiare in risposta a eventi specifici.

## <a name="sliders"></a>Dispositivi di scorrimento

I dispositivi di scorrimento sono utili per l'uso di informazioni che cambiano nel tempo. Ad esempio, è possibile usare un dispositivo di scorrimento per indicare la quantità di musica già riprodotta per un determinato file multimediale. I dispositivi di scorrimento possono essere orizzontali o verticali, lineari o circolari o qualsiasi forma che si possa pensare. I dispositivi di scorrimento sono disponibili in tre varietà: dispositivi di scorrimento, barre di stato e dispositivi di scorrimento personalizzati.

-   **Cursori.** È possibile usare **l'elemento SLIDER** per i controlli volume o per consentire all'utente di passare a una parte diversa del contenuto multimediale.
-   **Barre di stato.** Le barre di avanzamento sono simili ai dispositivi di scorrimento. Le barre di stato sono progettate per visualizzare graficamente la percentuale di un determinato processo completato, ma non per un processo con cui l'utente vorrà interagire. Ad esempio, potrebbe essere necessario usare un indicatore di stato per indicare lo stato di avanzamento del buffer.
-   **Dispositivi di scorrimento personalizzati.** Viene fornita la funzionalità del dispositivo di scorrimento personalizzato in modo da poter creare controlli come le manopole o creare meccanismi di controllo insoliti. Ad esempio, se si vuole creare un controllo del volume che racchiude l'interfaccia, è possibile farlo con un dispositivo di scorrimento personalizzato. Per configurare il dispositivo di scorrimento personalizzato, è necessario creare una mappa immagine contenente immagini in scala di grigi per definire le posizioni dei valori sul dispositivo di scorrimento. Questa operazione è relativamente semplice da eseguire con un programma di modifica grafica che supporta i livelli.

## <a name="text"></a>Testo

È possibile usare **l'elemento TEXT** per visualizzare il testo nell'interfaccia, ad esempio i titoli dei brani.

## <a name="video"></a>Video

È possibile visualizzare il video nell'interfaccia. **L'elemento VIDEO** consente di impostare le dimensioni e la posizione della finestra video.

È anche possibile consentire all'utente di modificare le impostazioni video con **l'elemento VIDEOSETTINGS.** Ad esempio, è possibile creare controlli per regolare la luminosità del video.

Se non si specifica un elemento video e il contenuto contiene video, Windows Media Player la modalità completa e l'interfaccia non verrà visualizzata.

## <a name="equalizer-settings"></a>Equalizzatore Impostazioni

È possibile impostare il filtro per bande di frequenza audio specifiche usando **l'elemento EQUALIZERSETTINGS.** È possibile aumentare il basso, modificare l'acuto e configurare i suoni in modo che corrispondano alle orecchini o al living.

## <a name="visualizations"></a>Visualizzazioni

È possibile visualizzare le visualizzazioni nell'interfaccia. Le visualizzazioni sono effetti visivi che cambiano nel tempo durante la riproduzione dell'audio Windows Media Player. **L'elemento EFFECTS** determina dove verranno riprodotte le visualizzazioni, le dimensioni della finestra e le visualizzazioni che verranno riprodotte.

## <a name="playlists"></a>Playlist

È possibile usare **l'elemento PLAYLIST** per consentire all'utente di selezionare un elemento da una playlist specifica.

## <a name="subviews"></a>Visualizzazioni secondarie

È possibile usare **l'elemento SUBVIEW** per visualizzare set secondari di controlli di interfaccia, ad esempio una playlist o controlli video.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File di interfaccia**](skin-files.md)
</dt> </dl>

 

 




