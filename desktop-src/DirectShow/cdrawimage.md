---
description: La classe CDrawImage è una classe helper che gestisce il disegno per un filtro renderer video.
ms.assetid: 7a6b3726-dbf5-4b60-8cf1-42034a321293
title: Classe CDrawImage (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 001b91338b2956f663d777cbc9597fa2d9a478f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333467"
---
# <a name="cdrawimage-class"></a>Classe CDrawImage

La `CDrawImage` classe è una classe helper che gestisce il disegno per un filtro renderer video. Tutte le operazioni di disegno vengono eseguite utilizzando GDI. Questa classe non fornisce alcun supporto per il rendering con DirectDraw. La `CDrawImage` classe richiede che il filtro proprietario usi anche la classe [**CBaseWindow**](cbasewindow.md) , che gestisce la finestra del video. Il `CDrawImage` costruttore accetta un puntatore all'oggetto **CBaseWindow** .

Il diagramma seguente mostra il modo migliore per usare questa classe in un filtro renderer video personalizzato.

![renderer video personalizzato con cdrawimage](images/videorenderer.png)

Per usare questa classe, eseguire le operazioni seguenti:

-   Quando i pin si connettono, chiamare i metodi [**CDrawImage:: NotifyMediaType**](cdrawimage-notifymediatype.md) e [**CDrawImage:: NotifyAllocator**](cdrawimage-notifyallocator.md) .
-   Ogni volta che il tipo di supporto cambia, chiamare di nuovo **NotifyMediaType** .
-   Prima che venga eseguito il rendering, chiamare [**CDrawImage:: SetDrawContext**](cdrawimage-setdrawcontext.md).
-   Chiamare [**CDrawImage:: SetSourceRect**](cdrawimage-setsourcerect.md) se il rettangolo di origine cambia e [**CDrawImage:: SetTargetRect**](cdrawimage-settargetrect.md) se il rettangolo di destinazione viene modificato.
-   Gestire la tavolozza per le immagini pallettizzati, come descritto nella sezione sulle tavolozze seguenti.

## <a name="allocators"></a>Allocatori

Il filtro illustrato nel diagramma precedente usa una classe allocator personalizzata, [**CImageAllocator**](cimageallocator.md). Questo allocatore crea la precedenza nella memoria condivisa tramite la funzione **CreateDIBSection** di GDI. Gli esempi creati dall'allocatore sono oggetti [**CImageSample**](cimagesample.md) .

Se il filtro è proprietario dell'allocatore per la connessione, gli esempi di supporti sono sicuramente oggetti [**CImageSample**](cimagesample.md) . In tal caso, l'oggetto **CDrawImage** può ottimizzare il disegno usando **BitBlt** o StretchBlt. In caso contrario, è necessario utilizzare le funzioni più lente **SetDIBitsToDevice** o **StretchDIBits** . L'opzione più veloce viene implementata dal metodo [**CDrawImage:: FastRender**](cdrawimage-fastrender.md) , l'opzione più lenta per il metodo [**CDrawImage:: SlowRender**](cdrawimage-slowrender.md) . Nonostante il nome, è probabile che non si verifichi un notevole miglioramento delle prestazioni in **SlowRender**, soprattutto su hardware più recente.

## <a name="palettes"></a>Tavolozze

Se per il disegno viene usato il metodo [**FastRender**](cdrawimage-fastrender.md) e l'immagine è pallettizzati, il filtro deve gestire la tavolozza, come indicato di seguito:

-   La classe [**CImageSample**](cimagesample.md) contiene un numero di versione della tavolozza, archiviato nella struttura [**DIBDATA**](dibdata.md) . Il valore viene inizializzato quando l'allocatore crea l'esempio.
-   La classe **CDrawImage** contiene anche un numero di versione della tavolozza, inizializzato al momento della creazione.
-   Ogni volta che il tipo di supporto viene modificato in un nuovo formato pallettizzati, chiamare [**CDrawImage:: IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md). Questo metodo incrementa il numero di versione della tavolozza dell'oggetto **CDrawImage** . Se il filtro usa la classe [**CImagePalette**](cimagepalette.md) per gestire le informazioni sulla tavolozza, è possibile chiamare semplicemente [**CImagePalette::P reparepalette**](cimagepalette-preparepalette.md) ogni volta che viene modificato il tipo di supporto. Il metodo **PreparePalette** incrementa la versione della tavolozza solo se necessario.
-   Il metodo [**FastRender**](cdrawimage-fastrender.md) confronta la versione della tavolozza **CDrawImage** con la versione della tavolozza dell'esempio. Se il numero di versione dell'esempio è in ritardo rispetto al numero di versione di **CDrawImage** , il metodo **FastRender** chiama [**CDrawImage:: UpdateColourTable**](cdrawimage-updatecolourtable.md). Il metodo **UpdateColourTable** imposta la tabella dei colori nel contesto di dispositivo, usando la funzione **SetDIBColorTable** di GDI. Inoltre, la versione della tavolozza nell'esempio viene aggiornata con il numero di versione corrente.
-   Se il pin si riconnette, il filtro deve chiamare [**CDrawImage:: ResetPaletteVersion**](cdrawimage-resetpaletteversion.md) per reimpostare la versione della tavolozza. Sulla riconnessione del PIN, l'allocatore rialloca tutti gli esempi.



| Variabili membro protette                                            | Descrizione                                                                                                                     |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**\_bStretch m**](cdrawimage-m-bstretch.md)                          | Indica se l'immagine video deve essere adattata alla finestra di destinazione.                                              |
| [**\_bUsingImageAllocator m**](cdrawimage-m-busingimageallocator.md)  | Indica se l'allocatore per la connessione pin è un oggetto **CImageAllocator** .                                         |
| [**\_EndSample m**](cdrawimage-m-endsample.md)                        | Specifica l'ora di arresto dell'esempio più recente.                                                                              |
| [**\_HDC m**](cdrawimage-m-hdc.md)                                    | Handle per il contesto di dispositivo della finestra proprietaria.                                                                              |
| [**\_MemoryDC m**](cdrawimage-m-memorydc.md)                          | Handle per il contesto di dispositivo di memoria della finestra proprietaria.                                                                       |
| [**\_PaletteVersion m**](cdrawimage-m-paletteversion.md)              | Utilizzato per tenere traccia della modifica della tavolozza.                                                                                         |
| [**\_pBaseWindow m**](cdrawimage-m-pbasewindow.md)                    | Puntatore all'oggetto **CBaseWindow** proprietario.                                                                                   |
| [**\_pMediaType m**](cdrawimage-m-pmediatype.md)                      | Puntatore al tipo di supporto corrente.                                                                                              |
| [**\_sourceRect m**](cdrawimage-m-sourcerect.md)                      | Specifica il rettangolo di origine per il disegno.                                                                                     |
| [**\_StartSample m**](cdrawimage-m-startsample.md)                    | Specifica l'ora di inizio dell'esempio più recente.                                                                             |
| [**\_targetRect m**](cdrawimage-m-targetrect.md)                      | Specifica il rettangolo di destinazione per il disegno.                                                                                     |
| Metodi protetti                                                     | Descrizione                                                                                                                     |
| [**DisplaySampleTimes**](cdrawimage-displaysampletimes.md)           | Disegna i timestamp di un campione multimediale sulla parte superiore dell'immagine del video.                                                              |
| [**FastRender**](cdrawimage-fastrender.md)                           | Disegna l'immagine video usando le funzioni **BitBlt** o **StretchBlt** .                                                         |
| [**SetStretchMode**](cdrawimage-setstretchmode.md)                   | Calcola se l'immagine video deve essere allungata.                                                                           |
| [**SlowRender**](cdrawimage-slowrender.md)                           | Disegna l'immagine video usando le funzioni **SetDIBitsToDevice** o **StretchDIBits** .                                           |
| [**UpdateColourTable**](cdrawimage-updatecolourtable.md)             | Aggiorna la tabella dei colori con una nuova tavolozza.                                                                                     |
| Metodi pubblici                                                        | Descrizione                                                                                                                     |
| [**CDrawImage**](cdrawimage-cdrawimage.md)                           | Metodo del costruttore.                                                                                                             |
| [**DrawImage**](cdrawimage-drawimage.md)                             | Disegna un fotogramma video nella finestra del video.                                                                                        |
| [**DrawVideoImageHere**](cdrawimage-drawvideoimagehere.md)           | Disegna un'immagine da un campione multimediale a un contesto di dispositivo specificato.                                                               |
| [**GetPaletteVersion**](cdrawimage-getpaletteversion.md)             | Recupera la versione della tavolozza.                                                                                                  |
| [**GetSourceRect**](cdrawimage-getsourcerect.md)                     | Recupera il rettangolo di origine corrente.                                                                                         |
| [**GetTargetRect**](cdrawimage-gettargetrect.md)                     | Recupera il rettangolo di destinazione corrente.                                                                                    |
| [**IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) | Incrementa la versione della tavolozza.                                                                                                 |
| [**NotifyAllocator**](cdrawimage-notifyallocator.md)                 | Informa l' `CDrawImage` oggetto se l'allocatore per la connessione è un oggetto **CImageAllocator** .                       |
| [**NotifyEndDraw**](cdrawimage-notifyenddraw.md)                     | Non supportata.                                                                                                                  |
| [**NotifyMediaType**](cdrawimage-notifymediatype.md)                 | Notifica all'oggetto il tipo di supporto corrente.                                                                                  |
| [**NotifyStartDraw**](cdrawimage-notifystartdraw.md)                 | Non supportata.                                                                                                                  |
| [**ResetPaletteVersion**](cdrawimage-resetpaletteversion.md)         | Reimposta la versione della tavolozza.                                                                                                     |
| [**ScaleSourceRect**](cdrawimage-scalesourcerect.md)                 | Ridimensiona un rettangolo di origine specificato, se esiste una differenza tra la dimensione del video nativa e il formato del tipo di supporto. Virtuale. |
| [**SetDrawContext**](cdrawimage-setdrawcontext.md)                   | Imposta i contesti di dispositivo usati per il disegno.                                                                                      |
| [**SetSourceRect**](cdrawimage-setsourcerect.md)                     | Imposta il rettangolo di origine.                                                                                                      |
| [**SetTargetRect**](cdrawimage-settargetrect.md)                     | Imposta il rettangolo di destinazione.                                                                                                      |
| [**UsingImageAllocator**](cdrawimage-usingimageallocator.md)         | Indica se l'allocatore corrente è un oggetto [**CImageAllocator**](cimageallocator.md) .                                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




