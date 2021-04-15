---
title: Elemento VIEW
description: Elemento VIEW
ms.assetid: e1dfde08-33a0-4f12-8db0-ad62e4a1d467
keywords:
- Interfacce Media Player di Windows, elemento di visualizzazione
- Skin, elemento VIEW
- Elemento VIEW
- riferimento per le interfacce, elemento di visualizzazione
- elementi, visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e907cced22b4d1cd498054df06ac8677a7488b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396235"
---
# <a name="view-element"></a>Elemento VIEW

L'elemento **View** contiene i dettagli dell'interfaccia utente di un oggetto Skin e usa gli attributi, i metodi e i gestori eventi illustrati nelle tabelle seguenti.

È possibile definire più elementi di **visualizzazione** come elementi figlio dell'elemento **Theme** di un'interfaccia per fornire interfacce diverse per situazioni diverse. Gli elementi della **vista** non possono essere specificati come elementi figlio di un altro elemento e contengono tutti gli altri elementi dell'interfaccia. Si noti che ogni vista ha un proprio ambito di variabili, ovvero non può condividere i valori di attributo con altre visualizzazioni.

L'attributo **View** Global può essere usato per fare riferimento a un elemento di **visualizzazione** specifico da qualsiasi punto al suo interno. Si tratta di un'alternativa all'utilizzo del relativo attributo **ID** , che deve essere utilizzato dall'interno di altri elementi di **visualizzazione** o dall'interno dell'elemento del **tema** .

L'elemento **View** supporta gli attributi seguenti. Gli attributi contrassegnati con un asterisco ( \* ) sono supportati anche dall'elemento **subview** .



| Attributo                                                       | Descrizione                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [BackgroundColor](view-backgroundcolor.md)\*                  | Specifica o Recupera il colore di sfondo della **vista** o della **vista**.                                             |
| [backgroundImage](view-backgroundimage.md) \*                  | Consente di specificare o recuperare l'immagine di sfondo della **vista** o della **vista**.                                             |
| [backgroundImageHueShift](view-backgroundimagehueshift.md)     | Specifica o recupera la quantità in base alla quale viene spostata la tonalità dell'immagine di sfondo.                                  |
| [backgroundImageSaturation](view-backgroundimagesaturation.md) | Specifica o Recupera il valore di saturazione dell'immagine di sfondo.                                                    |
| [backgroundTiled](view-backgroundtiled.md)\*                  | Specifica o recupera un valore che indica se l'immagine di sfondo  della vista **o della vista è** affiancata.         |
| [category](view-category.md)                                   | Specifica o recupera la categoria per la quale verrà visualizzata l'interfaccia utente.                                           |
| [focusObjectID](view-focusobjectid.md)                         | Specifica o recupera un valore che indica quale elemento dispone dello stato attivo della tastiera.                                             |
| [maxHeight](view-maxheight.md)                                 | Specifica o recupera l'altezza massima della **visualizzazione** durante il ridimensionamento.                                                |
| [maxWidth](view-maxwidth.md)                                   | Specifica o recupera la larghezza massima della **visualizzazione** durante il ridimensionamento.                                                 |
| [minHeight](view-minheight.md)                                 | Specifica o recupera l'altezza minima della **visualizzazione** durante il ridimensionamento.                                                |
| [minWidth](view-minwidth.md)                                   | Specifica o recupera la larghezza minima della **visualizzazione** durante il ridimensionamento.                                                 |
| [ridimensionabile](view-resizable.md)                                 | Specifica o recupera un valore che indica se la **vista** può essere ridimensionata.                                          |
| [resizeBackgroundImage](view-resizebackgroundimage.md)         | Specifica o recupera un valore che indica se è possibile ridimensionare l'immagine di sfondo.                                  |
| [scriptFile](view-scriptfile.md)                               | Specifica i nomi file dei file JScript associati.                                                                 |
| [timerInterval](view-timerinterval.md)                         | Specifica o recupera l'intervallo, in millisecondi, in cui il timer genera eventi nel gestore eventi **OnTimer** . |
| [title](view-title.md)                                         | Specifica o Recupera il titolo della **visualizzazione**. Può essere impostato solo in fase di progettazione.                                       |
| [titleBar](view-titlebar.md)                                   | Specifica o recupera un valore che indica se la barra del titolo della finestra è visualizzata.                                        |
| [transparencyColor](view-transparencycolor.md)\*              | Specifica o Recupera il colore di trasparenza dell'immagine di sfondo.                                                  |



 

L'elemento **View** supporta i metodi seguenti.



| Metodo                                              | Descrizione                                                |
|-----------------------------------------------------|------------------------------------------------------------|
| [close](view-close.md)                             | Chiude la **visualizzazione**.                                       |
| [massimizzare](view-maximize.md)                       | Ingrandisce la **visualizzazione**.                                    |
| [minimizzare](view-minimize.md)                       | Riduce al minimo la **visualizzazione**.                                    |
| [restore](view-restore.md)                         | Ripristina la **visualizzazione**.                                     |
| [returnToMediaCenter](view-returntomediacenter.md) | Restituisce l'utente alla modalità completa di Windows Media Player. |
| [size](view-size.md)                               | Ridimensiona la **visualizzazione** in un bordo specificato.                  |



 

L'elemento **View** può implementare i gestori eventi seguenti.



| Gestore di evento               | Descrizione                                                                |
|-----------------------------|----------------------------------------------------------------------------|
| [OnClose](view-onclose.md) | Gestisce un evento che si verifica quando la **visualizzazione** sta per essere chiusa.      |
| [OnError](view-onerror.md) | Gestisce un evento di errore se **Settings. enableErrorDialogs** è impostato su false. |
| [OnLoad](view-onload.md)   | Gestisce un evento che si verifica quando la **visualizzazione** viene visualizzata per la prima volta.         |
| [OnTimer](view-ontimer.md) | Gestisce gli eventi del timer.                                                      |



 

L'elemento **View** supporta gli attributi di ambiente ed è in grado di implementare i gestori eventi di ambiente, tranne nei casi indicati. Per ulteriori informazioni, vedere [attributi di ambiente](ambient-attributes.md) e [gestori eventi di ambiente](ambient-event-handlers.md),

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> </dl>

 

 




