---
title: Stampa guidata foto
description: La stampa guidata foto consente agli utenti di stampare le foto fornendo un'interfaccia di facile utilizzo della procedura guidata.
ms.assetid: 9cc2c7d4-a2aa-4abc-9c63-b091e044804f
keywords:
- Stampa guidata foto
- IDropTarget, stampa guidata foto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 708f051f658739cebd08e4f8643e5dd7fc0c6f7f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104399001"
---
# <a name="photo-printing-wizard"></a>Stampa guidata foto

La stampa guidata foto consente agli utenti di stampare le foto fornendo un'interfaccia di facile utilizzo della procedura guidata. La procedura guidata consente all'utente di specificare le dimensioni di stampa foto e altre opzioni di stampa, quindi di inviare le foto alla stampante. La procedura guidata è progettata in modo da poter essere richiamata a livello di codice da qualsiasi applicazione che desideri offrire agli utenti la possibilità di stampare foto e specificare il ridimensionamento e altre opzioni di stampa. La stampa guidata foto è disponibile in Windows XP e Windows Vista.

-   [Funzionalità fornite dalla procedura guidata di stampa foto](#features-provided-by-the-photo-print-wizard)
-   [Formati di file di foto supportati](#supported-photo-file-formats)
-   [Avvio a livello di codice della procedura guidata di stampa foto](#programmatically-launching-the-photo-print-wizard)

## <a name="features-provided-by-the-photo-print-wizard"></a>Funzionalità fornite dalla procedura guidata di stampa foto

La procedura guidata per la stampa fotografica offre diverse opzioni che potrebbero non essere disponibili nelle finestre di dialogo comuni della stampante, ad esempio modelli a più layout con dimensioni accurate. I modelli di layout consentono agli utenti di sfruttare al meglio lo spazio disponibile su carta stampata fotografica. Altre opzioni che è possibile specificare o a cui si accede tramite la procedura guidata di stampa foto includono:

-   Selezione di una stampante da un elenco di stampanti disponibili o destinazioni di stampa virtuale (ad esempio, Microsoft XPS Document Writer). In Windows Vista è possibile che siano disponibili le opzioni seguenti, a seconda delle funzionalità della stampante o della destinazione di stampa virtuale:
    -   Formato della carta. Ad esempio, "Letter", "Legal", "a3".
    -   Qualità di stampa, in termini di risoluzioni DPI (punti per pollice) supportati.
    -   Tipo di carta. Ad esempio, "Plain" o "glossy".
-   Avvio delle preferenze di stampa e delle proprietà per una particolare stampante.
-   Impostazione delle **copie di ogni immagine** (in Windows Vista) o **numero di volte in cui utilizzare** i valori della casella di selezione di ogni immagine (in Windows XP).
-   Specifica di un modello di layout di stampa. Ad esempio, vengono **stampate** **foto a pagina intera** o portafogli.
-   Selezione dell'opzione **Adatta immagine a frame** (disponibile solo in Windows Vista).
-   Visualizzazione in anteprima della foto stampata con le opzioni attualmente specificate.
-   Accesso a opzioni di stampa avanzate, ad esempio **nitidezza per la stampa e la** **gestione dei colori** (disponibile solo in Windows Vista).

Qualsiasi applicazione può trarre vantaggio dalle funzionalità e dalla funzionalità di stampa foto offerte dalla procedura guidata di stampa foto. Un'applicazione può passare i file da stampare. La stampa guidata foto esegue quindi la preparazione del file per la stampa in base alle opzioni specificate dall'utente e invia i file preparati alla stampante.

Nella figura seguente è illustrata l'interfaccia della procedura guidata stampa foto in Windows Vista

![Creazione guidata foto in Windows Vista](images/ppw-vista.png)

Nella figura seguente è illustrata l'interfaccia della procedura guidata stampa foto in Windows XP

![procedura guidata di stampa fotografica in Windows XP](images/ppw-xp.png)

## <a name="supported-photo-file-formats"></a>Formati di file di foto supportati

In Windows XP, la procedura guidata di stampa fotografica supporta tutti i formati di file grafici supportati da Windows GDI+. Attualmente, questi formati di file includono:

-   Bitmap (BMP)
-   Graphics Interchange Format (GIF)
-   Joint Photographic Experts Group (JPEG)
-   File di immagine scambiabile (EXIF)
-   Portable Network Graphics (PNG)
-   Tagged Image File Format (TIFF)

Per ulteriori informazioni sui formati di file grafici supportati da GDI+, vedere [tipi di bitmap](../gdiplus/-gdiplus-types-of-bitmaps-about.md).

In Windows Vista, la procedura guidata di stampa fotografica supporta qualsiasi formato di file di immagine per cui è installato un codec di Windows Imaging Component (WIC). WIC fornisce diversi codec standard, tra cui:

-   Bitmap (BMP)
-   GIF
-   Formato dell'icona (ICO)
-   JPEG
-   PNG
-   TIFF
-   Formato foto Windows Media

Per ulteriori informazioni sui codec WIC e WIC, vedere [componente Windows Imaging](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)

## <a name="programmatically-launching-the-photo-print-wizard"></a>Avvio a livello di codice della procedura guidata di stampa foto

Per richiamare la stampa guidata foto, chiamare l'interfaccia [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) con l'identificatore di classe seguente (CLSID):


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
```



I file da elaborare tramite la procedura guidata di stampa foto sono specificati in un oggetto [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) .

Nell'esempio di codice riportato di seguito viene illustrato come richiamare la stampa guidata foto.


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
            
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PrintPhotosDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



 

 