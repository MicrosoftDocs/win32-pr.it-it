---
title: Specifica delle risorse dell'immagine della barra multifunzione
description: Il Framework della barra multifunzione di Windows è progettato per supportare le risorse di immagine in modo esteso nell'interfaccia utente (UI) della barra multifunzione. Tutte le risorse immagine sono dichiarate in markup della barra multifunzione o eseguite da un'applicazione host della barra multifunzione.
ms.assetid: 37b57992-8da8-4e6b-869d-72a136f6ad77
keywords:
- Barra multifunzione di Windows, risorse immagine
- Barra multifunzione, risorse immagine
- Barra multifunzione di Windows, trasparenza
- Barra multifunzione, trasparenza
- Barra multifunzione di Windows, profondità colore
- Barra multifunzione, profondità colore
- Barra multifunzione di Windows, contrasto
- Barra multifunzione, contrasto
- risorse immagine nella barra multifunzione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e7666126e5b8f7fbe8b610678a8a1d71589373
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473923"
---
# <a name="specifying-ribbon-image-resources"></a>Specifica delle risorse dell'immagine della barra multifunzione

Il Framework della barra multifunzione di Windows è progettato per supportare le risorse di immagine in modo esteso nell'interfaccia utente (UI) della barra multifunzione. Tutte le risorse immagine sono dichiarate in [markup della barra multifunzione](windowsribbon-schema.md) o eseguite da un'applicazione host della barra multifunzione.

Per Windows 8 e versioni successive, il Framework della barra multifunzione supporta i formati grafici seguenti: file di bitmap (BMP) a 32 bit ARGB (BMP) e file Portable Network Graphics (PNG) con trasparenza.

Per Windows 7 e versioni precedenti, le risorse di immagine devono essere conformi al formato di grafica BMP standard usato in Windows.

> [!Note]  
> È possibile che si verifichi un errore di compilazione se al Framework viene fornito un formato di immagine non supportato.

 

## <a name="image-sizes"></a>Dimensioni delle immagini

Per garantire una maggiore flessibilità per i layout di controllo della barra multifunzione durante il ridimensionamento di una finestra dell'applicazione, il Framework della barra multifunzione accetta ed esegue il rendering delle immagini in una delle due dimensioni: grande o piccola.

Nelle immagini seguenti viene illustrata un'applicazione Ribbon che supporta più dimensioni della barra multifunzione tramite layout di controllo flessibili e la sostituzione di immagini di grandi dimensioni con piccole immagini, ove disponibili.

Lo screenshot seguente mostra la barra multifunzione con immagini di grandi dimensioni per i controlli dello zoom.

![screenshot che mostra una barra multifunzione che usa immagini di grandi dimensioni per i controlli dello zoom.](images/overviews/imageresources-largeimage.png)

Lo screenshot seguente mostra la stessa barra multifunzione ridimensionata con immagini piccole per i controlli zoom

![screenshot che mostra una barra multifunzione che usa immagini piccole per i controlli dello zoom.](images/overviews/imageresources-smallimage.png)

Lo screenshot seguente mostra la barra multifunzione nello stato nascosto. La barra multifunzione è nascosta quando tutti i layout di controllo potenziali sono esauriti e non è possibile eseguire il rendering della barra multifunzione con un'area di lavoro applicazione utilizzabile.

![screenshot che mostra una barra multifunzione compressa.](images/overviews/imageresources-noimage.png)

Per qualsiasi immagine, le dimensioni esatte del pixel dipendono dalla risoluzione dello schermo o da punti per pollice (dpi) del monitoraggio usato. A 96 dpi, le immagini di grandi dimensioni sono 32x32 pixel e le immagini piccole hanno dimensioni di 16x16 pixel. Le dimensioni dell'immagine aumentano in modo lineare rispetto a dpi, come illustrato nella tabella seguente.



| DPI     | Immagine piccola  | Immagine grande  |
|---------|--------------|--------------|
| 96 dpi  | pixel 16x16 | pixel 32x32 |
| 120 dpi | pixel 20x20 | 40x40 pixel |
| 144 dpi | pixel 24x24 | pixel 48x48 |
| 192 DPI | pixel 32x32 | pixel 64x64 |



 

Il Framework della barra multifunzione ridimensiona le risorse dell'immagine in modo obbligatorio. Tuttavia, poiché il ridimensionamento può produrre artefatti indesiderati e un calo delle immagini, è consigliabile che l'applicazione fornisca un piccolo set di risorse immagine che si estendono su diverse impostazioni dpi utilizzate comunemente. Se non viene trovata una corrispondenza esatta, l'immagine più vicina verrà ridimensionata verso l'alto o verso il basso.

Per semplificare questa operazione, le risorse di immagine possono essere dichiarate nel markup della barra multifunzione usando un set di elementi [**immagine**](windowsribbon-element-image.md) per ogni elemento [**Command**](windowsribbon-element-command.md) . In fase di esecuzione, il Framework seleziona l'immagine da visualizzare in base all'attributo *MinDPI* di ogni elemento **Image** .

> [!IMPORTANT]
>
> Quando una raccolta di risorse immagine progettate per supportare specifiche impostazioni DPI dello schermo viene fornita al framework della barra multifunzione tramite un set di elementi [**immagine**](windowsribbon-element-image.md) , il Framework usa l' **immagine** con un valore dell'attributo *MinDPI* che corrisponde all'impostazione DPI dello schermo corrente.
>
> Se nessun elemento [**Image**](windowsribbon-element-image.md) è dichiarato con un valore *MinDPI* che corrisponde all'impostazione DPI dello schermo corrente, il Framework seleziona l' **immagine** con il valore *MinDPI* più vicino inferiore rispetto all'impostazione DPI dello schermo corrente e ridimensiona la risorsa dell'immagine verso l'alto. In caso contrario, se non viene dichiarato alcun elemento **Image** con un valore dell'attributo *MinDPI* inferiore a quello della schermata corrente, il Framework sceglie il valore *MinDPI* più vicino maggiore dell'impostazione corrente DPI dello schermo e ridimensiona la risorsa immagine verso il basso.

 

Nell'esempio seguente viene illustrato come dichiarare un set di immagini per adattare le varie dimensioni della barra multifunzione e le impostazioni di sistema.


```C++
<Command.LargeImages>
  <Image Source="res/CutLargeImage32.bmp" Id="116" Symbol="ID_CUT_LARGEIMAGE1" MinDPI="96" />
  <Image Source="res/CutLargeImage40.bmp" Id="117" Symbol="ID_CUT_LARGEIMAGE2" MinDPI="120" />
  <Image Source="res/CutLargeImage48.bmp" Id="118" Symbol="ID_CUT_LARGEIMAGE3" MinDPI="144" />
  <Image Source="res/CutLargeImage64.bmp" Id="119" Symbol="ID_CUT_LARGEIMAGE4" MinDPI="192" />
</Command.LargeImages>
<Command.SmallImages>
  <Image Source="res/CutSmallImage16.bmp" Id="122" Symbol="ID_CUT_SMALLIMAGE1" MinDPI="96" />
  <Image Source="res/CutSmallImage20.bmp" Id="123" Symbol="ID_CUT_SMALLIMAGE2" MinDPI="120" />
  <Image Source="res/CutSmallImage24.bmp" Id="124" Symbol="ID_CUT_SMALLIMAGE3" MinDPI="144" />
  <Image Source="res/CutSmallImage32.bmp" Id="125" Symbol="ID_CUT_SMALLIMAGE4" MinDPI="192" />
</Command.SmallImages>
<Command.LargeHighContrastImages>
  <Image Source="res/CutLargeImage32HC.bmp" Id="130" Symbol="ID_CUT_LARGEIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutLargeImage40HC.bmp" Id="131" Symbol="ID_CUT_LARGEIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutLargeImage48HC.bmp" Id="132" Symbol="ID_CUT_LARGEIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutLargeImage64HC.bmp" Id="133" Symbol="ID_CUT_LARGEIMAGE4HC" MinDPI="192" />
</Command.LargeHighContrastImages>
<Command.SmallHighContrastImages>
  <Image Source="res/CutSmallImage16HC.bmp" Id="135" Symbol="ID_CUT_SMALLIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutSmallImage20HC.bmp" Id="136" Symbol="ID_CUT_SMALLIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutSmallImage24HC.bmp" Id="137" Symbol="ID_CUT_SMALLIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutSmallImage32HC.bmp" Id="138" Symbol="ID_CUT_SMALLIMAGE4HC" MinDPI="192" />
</Command.SmallHighContrastImages>
```



Se le immagini dichiarate nel markup vengono invalidate in fase di esecuzione per qualsiasi motivo, viene eseguita una query sulle nuove immagini nell'applicazione host. Quando queste immagini vengono generate e caricate a livello di codice, l'applicazione deve tentare di restituire immagini ridimensionate in base alle dimensioni predefinite delle icone di sistema determinate dalla [ \_ metrica di sistema CXICON SM](/windows/win32/api/winuser/nf-winuser-getsystemmetrics).

> [!Note]  
> Le immagini di grandi dimensioni hanno una dimensione di SM \_ CXICON per SM \_ CXICON e le immagini piccole hanno una dimensione di SM \_ CXICON/2 per SM \_ CXICON/2.

 

## <a name="color-depth-transparency-and-contrast"></a>Profondità di colore, trasparenza e contrasto

Si prevede che le immagini regolari siano in formato pixel ARGB a 32 bit per pixel (BPP) e ridimensionate in base alle dimensioni dell'icona di sistema predefinite. Questo formato supporta la trasparenza e l'anti-aliasing (con 8 bit per canale).

> [!WARNING]
> Molti strumenti di modifica delle immagini non mantengono il canale alfa a 8 bit di ordine più alto durante il caricamento o il salvataggio di immagini di 32 BPP.

 

Per visualizzare correttamente un'immagine in modalità a contrasto elevato, è necessario che sia in formato pixel a 4 BPP. Quando viene eseguito il rendering dell'immagine, il Framework della barra multifunzione esegue il mapping dei colori specifici in base al contesto a contrasto elevato dell'immagine.

La tabella seguente elenca il comportamento di rendering dei colori a contrasto elevato del Framework.



Colore dei pixel

Valore RGB

Comportamento

Sfondo bianco

Sfondo scuro

MAGENTA

800080

Modalità trasparente

Modalità trasparente

NERO

000000

\_WINDOWTEXT colore

BIANCO

BIANCO

FFFFFF

\_finestra colori

NERO

GRIGIO SCURO

808080

\_3DSHADOW colore

\_3DSHADOW colore

GRIGIO

C0C0C0

\_3DFACE colore

\_3DFACE colore

GRIGIO CHIARO

ATTIGLIO

\_3DLIGHT colore

\_3DLIGHT colore

BLU SCURO

000080

n/d

BIANCO



 

Per ulteriori informazioni sui formati di immagine supportati dal framework della barra multifunzione, vedere gli argomenti seguenti:

-   [Struttura BITMAPINFOHEADER](/previous-versions//dd183376(v=vs.85)) : descrive il formato pixel ARGB di 32 BPP.
-   [Funzione CreateDIBSection](/windows/win32/api/wingdi/nf-wingdi-createdibsection) : descrive come creare un'immagine in formato pixel ARGB a 32 BPP.
-   [Funzione LoadImage](/windows/win32/api/winuser/nf-winuser-loadimagea) : descrive come caricare un'immagine in formato pixel ARGB a 32 BPP.

## <a name="accessibility"></a>Accessibilità

Basandosi sulle risorse immagine per fornire informazioni, trasmettere funzionalità di controllo ed esporre lo stato dell'applicazione, è possibile aumentare la necessità di requisiti di accessibilità durante la progettazione e lo sviluppo di applicazioni.

Per il supporto di base a contrasto elevato, la barra multifunzione consente di visualizzare un set separato di file di immagine quando è attivo un tema a contrasto elevato. Queste immagini possono essere di 32 BPP o 4 BPP, con colori mappati a una tavolozza speciale in cui i colori scuro e chiaro vengono invertiti a seconda dei colori di primo piano e di sfondo del tema attivo a contrasto elevato.

Nell'esempio seguente viene illustrato come vengono dichiarate le risorse immagine a contrasto elevato nel markup della barra multifunzione:


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px.bmp" MinDPI="192" />
      </Command.LargeImages>
      <Command.LargeHighContrastImages>
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px-HC.bmp" MinDPI="192" />
      </Command.LargeHighContrastImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px.bmp" MinDPI="192" />
      </Command.SmallImages>
      <Command.SmallHighContrastImages>
        <Image Source="cmdNew-16px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="192" />
      </Command.SmallHighContrastImages>
    </Command>
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Comando. SmallImages**](windowsribbon-element-command-smallimages.md)
</dt> <dt>

[Interfaccia utente \_ pkey \_ smallImage](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> <dt>

[**Comando. LargeImages**](windowsribbon-element-command-largeimages.md)
</dt> <dt>

[Interfaccia utente \_ pkey \_ largeImage](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> <dt>

[**Comando. SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)
</dt> <dt>

[Interfaccia utente \_ pkey \_ SmallHighContrastImage](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> <dt>

[**Comando. LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)
</dt> <dt>

[Interfaccia utente \_ pkey \_ LargeHighContrastImage](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 