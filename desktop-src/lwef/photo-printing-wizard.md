---
title: Stampa guidata foto
description: La Stampa guidata foto consente agli utenti di stampare foto fornendo un'interfaccia della procedura guidata di facile utilizzo.
ms.assetid: 9cc2c7d4-a2aa-4abc-9c63-b091e044804f
keywords:
- Stampa guidata foto
- IDropTarget, Stampa guidata foto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38199f7977e428f41cbc0560e0eab9ad2e106709579255ec8c3a1e74d7f7a402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475450"
---
# <a name="photo-printing-wizard"></a>Stampa guidata foto

La Stampa guidata foto consente agli utenti di stampare foto fornendo un'interfaccia della procedura guidata di facile utilizzo. La procedura guidata consente all'utente di specificare le dimensioni di stampa delle foto e altre opzioni di stampa e quindi invia le foto alla stampante. La procedura guidata è progettata in modo che possa essere richiamata a livello di codice da qualsiasi applicazione che voglia offrire agli utenti la possibilità di stampare foto e specificare il ridimensionamento e altre opzioni di stampa. La Stampa guidata foto è disponibile in Windows XP e Windows Vista.

-   [Funzionalità fornite dalla Stampa guidata foto](#features-provided-by-the-photo-print-wizard)
-   [Formati di file di foto supportati](#supported-photo-file-formats)
-   [Avvio della Stampa guidata foto a livello di codice](#programmatically-launching-the-photo-print-wizard)

## <a name="features-provided-by-the-photo-print-wizard"></a>Funzionalità fornite dalla Stampa guidata foto

La Stampa guidata foto offre diverse opzioni che potrebbero non essere disponibili nelle finestre di dialogo comuni della stampante, ad esempio modelli multi-layout con dimensioni accurate. I modelli di layout consentono agli utenti di usare in modo più efficiente lo spazio disponibile sulla carta da stampa. Altre opzioni che è possibile specificare o accedere tramite la Stampa guidata foto includono:

-   Selezione di una stampante da un elenco di stampanti disponibili o destinazioni di stampa virtuale (ad esempio, Microsoft XPS Document Writer). In Windows Vista possono essere disponibili le opzioni seguenti, a seconda delle funzionalità della stampante o della destinazione di stampa virtuale:
    -   Dimensioni della carta. Ad esempio, "Letter", "Legal", "A3".
    -   Qualità di stampa, in termini di risoluzioni di punti per pollice (dpi) supportate.
    -   Tipo di carta. Ad esempio, "Plain" o "Glossy".
-   Avvio delle preferenze e delle proprietà di stampa per una determinata stampante.
-   Impostazione dei valori della casella di selezione **Copies of each picture** (Windows Vista) o Number of times to use each picture (on Windows XP) (Copies of each picture (in Windows Vista) o **Number of times to use** each picture (on Windows XP) spin box values (Numero di volte in cui usare ogni immagine Windows XP).
-   Specifica di un modello di layout di stampa. Ad esempio, **foto a pagina intera o** Portafoglio **stampa**.
-   Selezione **dell'opzione Adatta immagine alla cornice** (disponibile solo Windows Vista).
-   Anteprima della foto stampata con le opzioni attualmente specificate.
-   Accesso alle opzioni di stampa avanzate, ad esempio **Sharpen** per la stampa e la gestione dei colori **(disponibile** solo Windows Vista).

Qualsiasi applicazione può trarre vantaggio dalle funzionalità e dalla funzionalità di stampa di foto offerte dalla Stampa guidata foto. Un'applicazione può passare i file da stampare. La Stampa guidata foto si occupa quindi della preparazione del file per la stampa in base alle opzioni specificate dall'utente e invia i file preparati alla stampante.

La figura seguente illustra l'interfaccia della Stampa guidata foto Windows Vista

![Creazione guidata stampa di foto in Windows Vista](images/ppw-vista.png)

La figura seguente illustra l'interfaccia della Stampa guidata foto Windows XP

![la procedura guidata di stampa di foto in Windows XP](images/ppw-xp.png)

## <a name="supported-photo-file-formats"></a>Formati di file di foto supportati

In Windows XP, la Stampa guidata foto supporta tutti i formati di file di grafica supportati da Windows GDI+. Attualmente, questi formati di file includono:

-   Bitmap (BMP)
-   Graphics Interchange Format (GIF)
-   Joint Photographic Experts Group (JPEG)
-   File di immagine scambiabile (EXIF)
-   Portable Network Graphics (PNG)
-   Tagged Image File Format (TIFF)

Per altre informazioni sui formati di file di grafica supportati GDI+, vedere [Tipi di bitmap](../gdiplus/-gdiplus-types-of-bitmaps-about.md).

In Windows Vista, la Stampa guidata foto supporta qualsiasi formato di file di immagine per cui è installato un codec WIC (Windows Imaging Component). WIC offre diversi codec standard, tra cui:

-   Bitmap (BMP)
-   GIF
-   Formato icona (ICO)
-   JPEG
-   PNG
-   TIFF
-   Windows Formato foto multimediale

Per altre informazioni sui codec WIC e WIC, vedere Windows [Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)

## <a name="programmatically-launching-the-photo-print-wizard"></a>Avvio della Stampa guidata foto a livello di codice

Per richiamare la Stampa guidata foto, chiamare [l'interfaccia IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) con l'identificatore di classe (CLSID) seguente:


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
```



I file che devono essere elaborati dalla Stampa guidata foto vengono specificati in un [oggetto IDataObject.](/windows/win32/api/objidl/nn-objidl-idataobject)

Nell'esempio di codice seguente viene illustrato come richiamare la Stampa guidata foto.


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



 

 