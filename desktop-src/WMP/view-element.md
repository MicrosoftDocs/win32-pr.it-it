---
title: Elemento VIEW
description: Elemento VIEW
ms.assetid: e1dfde08-33a0-4f12-8db0-ad62e4a1d467
keywords:
- Windows Media Player skin, elemento VIEW
- skins,elemento VIEW
- Elemento VIEW
- riferimento per le skin, elemento VIEW
- elementi,VIEW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a2d2b14f75d3cf5405c1663e23ad343e3c22bb2a80f60919de4505808cdf0a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571653"
---
# <a name="view-element"></a>Elemento VIEW

**L'elemento VIEW** contiene i dettagli dell'interfaccia utente di un'interfaccia e usa gli attributi, i metodi e i gestori eventi illustrati nelle tabelle seguenti.

Più **elementi VIEW** possono essere definiti come elementi figlio dell'elemento **THEME** di un'interfaccia per fornire interfacce diverse per situazioni diverse. **Gli** elementi VIEW non possono essere specificati come elementi figlio di qualsiasi altro elemento e contengono tutti gli altri elementi dell'interfaccia. Si noti che ogni vista ha un proprio ambito variabile, il che significa che non può condividere i valori degli attributi con altre viste.

**L'attributo** globale view può essere usato per fare riferimento a un elemento **VIEW** specifico da qualsiasi posizione al suo interno. Si tratta di un'alternativa all'uso del relativo **attributo id,** che deve essere usato dall'interno di altri elementi **VIEW** o dall'interno dell'elemento **THEME.**

**L'elemento VIEW** supporta gli attributi seguenti. Anche gli attributi contrassegnati con un asterisco ( \* ) sono supportati **dall'elemento SUBVIEW.**



| Attributo                                                       | Descrizione                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [backgroundColor](view-backgroundcolor.md)\*                  | Specifica o recupera il colore di sfondo di **VIEW** o **SUBVIEW.**                                             |
| [backgroundImage](view-backgroundimage.md) \*                  | Specifica o recupera l'immagine di sfondo di **VIEW** o **SUBVIEW.**                                             |
| [backgroundImageHueShift](view-backgroundimagehueshift.md)     | Specifica o recupera la quantità di spostamento della tonalità dell'immagine di sfondo.                                  |
| [backgroundImageSaturation](view-backgroundimagesaturation.md) | Specifica o recupera il valore di saturazione dell'immagine di sfondo.                                                    |
| [backgroundTiled](view-backgroundtiled.md)\*                  | Specifica o recupera un valore che indica se l'immagine di sfondo dell'oggetto **VIEW** o **SUBVIEW** è affiancata.         |
| [category](view-category.md)                                   | Specifica o recupera la categoria per cui verrà visualizzata l'interfaccia utente.                                           |
| [focusObjectID](view-focusobjectid.md)                         | Specifica o recupera un valore che indica quale elemento ha lo stato attivo della tastiera.                                             |
| [Maxheight](view-maxheight.md)                                 | Specifica o recupera l'altezza massima della **vista** durante il ridimensionamento.                                                |
| [maxWidth](view-maxwidth.md)                                   | Specifica o recupera la larghezza massima dell'oggetto **VIEW** durante il ridimensionamento.                                                 |
| [minHeight](view-minheight.md)                                 | Specifica o recupera l'altezza minima della **vista** durante il ridimensionamento.                                                |
| [Minwidth](view-minwidth.md)                                   | Specifica o recupera la larghezza minima dell'oggetto **VIEW durante** il ridimensionamento.                                                 |
| [Ridimensionabile](view-resizable.md)                                 | Specifica o recupera un valore che indica se **l'oggetto VIEW** può essere ridimensionato.                                          |
| [resizeBackgroundImage](view-resizebackgroundimage.md)         | Specifica o recupera un valore che indica se l'immagine di sfondo può essere ridimensionata.                                  |
| [scriptFile](view-scriptfile.md)                               | Specifica i nomi di file dei file JScript file.                                                                 |
| [Timerinterval](view-timerinterval.md)                         | Specifica o recupera l'intervallo, in millisecondi, in cui il timer genera eventi al gestore dell'evento **ontimer.** |
| [title](view-title.md)                                         | Specifica o recupera il titolo dell'oggetto **VIEW.** Può essere impostato solo in fase di progettazione.                                       |
| [Titlebar](view-titlebar.md)                                   | Specifica o recupera un valore che indica se viene visualizzata la barra del titolo della finestra.                                        |
| [transparencyColor](view-transparencycolor.md)\*              | Specifica o recupera il colore di trasparenza dell'immagine di sfondo.                                                  |



 

**L'elemento VIEW** supporta i metodi seguenti.



| Metodo                                              | Descrizione                                                |
|-----------------------------------------------------|------------------------------------------------------------|
| [close](view-close.md)                             | Chiude l'oggetto **VIEW.**                                       |
| [Massimizzare](view-maximize.md)                       | Ingrandisce **view**.                                    |
| [Minimizzare](view-minimize.md)                       | Riduce a icona **l'oggetto VIEW.**                                    |
| [restore](view-restore.md)                         | Ripristina l'oggetto **VIEW.**                                     |
| [returnToMediaCenter](view-returntomediacenter.md) | Restituisce l'utente alla modalità completa di Windows Media Player. |
| [size](view-size.md)                               | Ridimensiona **l'oggetto VIEW** su un bordo specificato.                  |



 

**L'elemento VIEW** può implementare i gestori eventi seguenti.



| Gestore di evento               | Descrizione                                                                |
|-----------------------------|----------------------------------------------------------------------------|
| [onclose](view-onclose.md) | Gestisce un evento che si verifica quando **l'oggetto VIEW** sta per essere chiuso.      |
| [Onerror](view-onerror.md) | Gestisce un evento di errore **se Impostazioni.enableErrorDialogs** è impostato su false. |
| [Onload](view-onload.md)   | Gestisce un evento che si verifica alla **prima** visualizzazione di VIEW.         |
| [ontimer](view-ontimer.md) | Gestisce gli eventi timer.                                                      |



 

**L'elemento VIEW** supporta gli attributi di ambiente e può implementare i gestori eventi di ambiente, tranne dove specificato. Per altre informazioni, vedere [Attributi di ambiente](ambient-attributes.md) e Gestori eventi di [ambiente](ambient-event-handlers.md),

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> </dl>

 

 




