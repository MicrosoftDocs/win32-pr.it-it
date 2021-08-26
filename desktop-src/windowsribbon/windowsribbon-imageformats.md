---
title: Specifica delle risorse immagine della barra multifunzione
description: Come sistema di presentazione dei comandi completo, il framework Windows ribbon è progettato per supportare ampiamente le risorse immagine nell'interfaccia utente della barra multifunzione. Tutte le risorse immagine vengono dichiarate nel markup della barra multifunzione o vengono sottoposti a query da un'applicazione host della barra multifunzione.
ms.assetid: 37b57992-8da8-4e6b-869d-72a136f6ad77
keywords:
- Windows Barra multifunzione, risorse immagine
- Barra multifunzione, risorse immagine
- Windows Barra multifunzione, trasparenza
- Barra multifunzione, trasparenza
- Windows Barra multifunzione, profondità del colore
- Barra multifunzione, profondità del colore
- Windows Barra multifunzione, contrasto
- Barra multifunzione, contrasto
- Risorse immagine nella Windows multifunzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c485de9c0d9d1b51b09d4a2b9dba95dd30a778922750a7f388c7a5c8963cda6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932596"
---
# <a name="specifying-ribbon-image-resources"></a>Specifica delle risorse immagine della barra multifunzione

Come sistema di presentazione dei comandi completo, il framework Windows ribbon è progettato per supportare ampiamente le risorse immagine nell'interfaccia utente della barra multifunzione. Tutte le risorse immagine vengono dichiarate nel [markup della barra multifunzione o](windowsribbon-schema.md) vengono sottoposti a query da un'applicazione host della barra multifunzione.

Per Windows 8 e versioni successive, il framework della barra multifunzione supporta i formati grafici seguenti: file bitmap ARGB (BMP) a 32 bit e file Portable Network Graphics (PNG) con trasparenza.

Per Windows 7 e versioni precedenti, le risorse immagine devono essere conformi al formato grafico BMP standard usato in Windows.

> [!Note]  
> Se al framework viene fornito un formato di immagine non supportato, può verificarsi un errore di compilazione.

 

## <a name="image-sizes"></a>Dimensioni delle immagini

Per offrire maggiore flessibilità per i layout dei controlli della barra multifunzione durante il ridimensionamento di una finestra dell'applicazione, il framework della barra multifunzione accetta ed esegue il rendering delle immagini in una delle due dimensioni seguenti: grande o piccola.

Le immagini seguenti illustrano un'applicazione barra multifunzione che supporta più dimensioni della barra multifunzione tramite layout di controllo flessibili e la sostituzione di immagini di grandi dimensioni con immagini di piccole dimensioni, se disponibili.

Lo screenshot seguente mostra la barra multifunzione con immagini di grandi dimensioni per i controlli Zoom.

![Screenshot che mostra una barra multifunzione che usa immagini di grandi dimensioni per i controlli zoom.](images/overviews/imageresources-largeimage.png)

Lo screenshot seguente mostra la stessa barra multifunzione ridimensionata con immagini piccole per i controlli Zoom

![Screenshot che mostra una barra multifunzione che usa immagini di piccole dimensioni per i controlli zoom.](images/overviews/imageresources-smallimage.png)

Lo screenshot seguente mostra la barra multifunzione in stato nascosto. La barra multifunzione è nascosta quando tutti i potenziali layout di controllo sono stati esauriti e non è possibile eseguire il rendering della barra multifunzione con un'area di lavoro dell'applicazione utilizzabile.

![Screenshot che mostra una barra multifunzione compressa.](images/overviews/imageresources-noimage.png)

Per qualsiasi immagine, le dimensioni esatte in pixel dipendono dalla risoluzione dello schermo o punti per pollice (dpi) del monitor in uso. A 96 dpi, le immagini di grandi dimensioni hanno una dimensione di 32x32 pixel e le immagini piccole hanno una dimensione di 16x16 pixel. Le dimensioni delle immagini aumentano in modo lineare rispetto a dpi, come illustrato nella tabella seguente.



| DPI     | Immagine piccola  | Immagine grande  |
|---------|--------------|--------------|
| 96 dpi  | 16x16 pixel | 32x32 pixel |
| 120 dpi | 20x20 pixel | 40x40 pixel |
| 144 dpi | 24x24 pixel | 48x48 pixel |
| 192 dpi | 32x32 pixel | 64x64 pixel |



 

Il framework della barra multifunzione ridimensiona le risorse immagine in base alle esigenze. Tuttavia, poiché il ridimensionamento può produrre artefatti indesiderati e una riduzione delle prestazioni delle immagini, è consigliabile che l'applicazione fornica un piccolo set di risorse immagine che si estendono su varie impostazioni dpi di uso comune. Se non viene trovata una corrispondenza esatta, l'immagine più vicina verrà ridimensionata verso l'alto o verso il basso.

Per semplificare questa operazione, le risorse immagine possono essere dichiarate nel markup della barra multifunzione usando un set di [**elementi Image**](windowsribbon-element-image.md) per ogni [**elemento**](windowsribbon-element-command.md) Command. In fase di esecuzione, il framework seleziona l'immagine da visualizzare in base *all'attributo MinDPI* di ogni **elemento** Image.

> [!IMPORTANT]
>
> Quando al framework della barra multifunzione viene fornita una raccolta di risorse immagine progettate per supportare impostazioni dpi dello schermo specifiche tramite un set di elementi [**Image,**](windowsribbon-element-image.md) il framework usa l'attributo **Image** con un valore di attributo *MinDPI* corrispondente all'impostazione dpi dello schermo corrente.
>
> Se nessun elemento [**Image**](windowsribbon-element-image.md) viene dichiarato con un valore *MinDPI* corrispondente all'impostazione dpi dello schermo corrente, il framework seleziona l'immagine con il valore  *MinDPI* più vicino minore dell'impostazione dpi dello schermo corrente e ridimensiona la risorsa immagine. In caso contrario, se nessun elemento **Image** viene dichiarato con un valore di attributo *MinDPI* minore dell'impostazione dpi dello schermo corrente, il framework seleziona il valore *MinDPI* più vicino maggiore dell'impostazione dpi dello schermo corrente e ridimensiona la risorsa immagine.

 

L'esempio seguente illustra come dichiarare un set di immagini per supportare diverse dimensioni della barra multifunzione e impostazioni di sistema.


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



Se le immagini dichiarate nel markup vengono invalidate in fase di esecuzione per qualsiasi motivo, viene eseguita una query sull'applicazione host per le nuove immagini. Quando queste immagini vengono generate e caricate a livello di codice, l'applicazione deve tentare di restituire immagini ridimensionate in base alle dimensioni predefinite delle icone di sistema determinate dalla metrica di sistema [ \_ SM CXICON](/windows/win32/api/winuser/nf-winuser-getsystemmetrics).

> [!Note]  
> Le immagini di grandi dimensioni hanno dimensioni di SM CXICON di SM CXICON e le immagini di piccole dimensioni hanno dimensioni di \_ \_ SM \_ CXICON/2 di SM \_ CXICON/2.

 

## <a name="color-depth-transparency-and-contrast"></a>Profondità del colore, trasparenza e contrasto

Si prevede che le immagini normali siano in formato pixel ARGB a 32 bit per pixel (BPP) e ridimensionate in base alle dimensioni predefinite dell'icona di sistema. Questo formato supporta sia la trasparenza che l'antialiasing (usando 8 bit per canale).

> [!WARNING]
> Molti strumenti di modifica delle immagini non mantengono il canale alfa a 8 bit con ordine massimo durante il caricamento o il salvataggio di 32 immagini BPP.

 

Perché un'immagine venga visualizzata correttamente in modalità a contrasto elevato, deve essere in un formato pixel a 4 BPP. Quando viene eseguito il rendering dell'immagine, il framework della barra multifunzione modifica il mapping di colori specifici in base al contesto a contrasto elevato dell'immagine.

La tabella seguente elenca il comportamento di rendering dei colori a contrasto elevato del framework.



Colore dei pixel

Valore RGB

Comportamento

Sfondo bianco

Sfondo scuro

Magenta

800080

Modalità trasparente

Modalità trasparente

Nero

000000

FINESTRA \_ COLORETESTO

Bianco

Bianco

FFFFFF

FINESTRA \_ COLORE

Nero

GRIGIO SCURO

808080

COLORE \_ 3DSHADOW

COLORE \_ 3DSHADOW

Grigio

C0C0C0

COLORE \_ 3DFACE

COLORE \_ 3DFACE

GRIGIO CHIARO

DFDFDF

COLORE \_ 3DLIGHT

COLORE \_ 3DLIGHT

BLU SCURO

000080

n/d

Bianco



 

Per altre informazioni sui formati di immagine supportati dal framework della barra multifunzione, vedere gli argomenti seguenti:

-   [Struttura BITMAPINFOHEADER:](/previous-versions//dd183376(v=vs.85)) descrive il formato a 32 pixel ARGB BPP.
-   [Funzione CreateDIBSection:](/windows/win32/api/wingdi/nf-wingdi-createdibsection) descrive come creare un'immagine in formato pixel ARGB da 32 BPP.
-   [Funzione LoadImage:](/windows/win32/api/winuser/nf-winuser-loadimagea) descrive come caricare un'immagine in formato pixel ARGB da 32 BPP.

## <a name="accessibility"></a>Accessibilità

Basandosi sulle risorse immagine per fornire informazioni, trasmettere funzionalità di controllo ed esporre lo stato dell'applicazione, aumenta la necessità di requisiti di accessibilità durante la progettazione e lo sviluppo dell'applicazione.

Per il supporto del contrasto elevato di base, la barra multifunzione consente la visualizzazione di un set separato di file di immagine quando è attivo un tema a contrasto elevato. Queste immagini possono essere di 32 BPP o 4 BPP, con colori mappati a una tavolozza speciale in cui i colori scuro e chiaro vengono invertiti a seconda dei colori di primo piano e di sfondo del tema attivo a contrasto elevato.

L'esempio seguente illustra come vengono dichiarate le risorse immagine a contrasto elevato nel markup della barra multifunzione:


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

[**Command.SmallImages**](windowsribbon-element-command-smallimages.md)
</dt> <dt>

[UI \_ PKEY \_ SmallImage](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> <dt>

[**Command.LargeImages**](windowsribbon-element-command-largeimages.md)
</dt> <dt>

[UI \_ PKEY \_ LargeImage](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> <dt>

[**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)
</dt> <dt>

[UI \_ PKEY \_ SmallHighContrastImage](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> <dt>

[**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)
</dt> <dt>

[UI \_ PKEY \_ LargeHighContrastImage](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 