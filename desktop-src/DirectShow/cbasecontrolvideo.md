---
description: La classe CBaseControlVideo implementa l'interfaccia IBasicVideo e controlla le proprietà video di una finestra video generica. In genere, un oggetto CBaseControlVideo è un renderer video che disegna video in una finestra sullo schermo.
ms.assetid: 16fc1b0a-e5b5-4f33-ac2b-5acff61bab81
title: Classe CBaseControlVideo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3d8e6f7c881cc62f9124a58cb168bb3b2123d5f8e3c99b1d86b6aed0f87e2aaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697946"
---
# <a name="cbasecontrolvideo-class"></a>Classe CBaseControlVideo

![Gerarchia di classi cbasecontrolvideo](images/wctrl02.png)

La **classe CBaseControlVideo** implementa [**l'interfaccia IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) e controlla le proprietà video di una finestra video generica. In genere, **un oggetto CBaseControlVideo** è un renderer video che disegna video in una finestra sullo schermo.

Molte **funzioni membro CBaseControlVideo** richiedono solo che il renderer video sia connesso a un grafo di filtro. Se non è connesso, le funzioni membro restituiranno **VFW \_ E \_ NOT \_ CONNECTED**. Le proprietà impostate in un renderer video vengono mantenute tra connessioni successive e disconnessioni. Tutte le applicazioni devono assicurarsi di reimpostare le proprietà del renderer prima di avviare una presentazione.

Quando si usa il video, l'applicazione può selezionare una parte del video da usare. Questa parte è il rettangolo di origine controllato **dall'oggetto CBaseControlVideo.** **CBaseControlVideo** consente all'applicazione di impostare e recuperare il rettangolo di origine. Tutti i rettangoli **utilizzati da CBaseControlVideo** utilizzano i valori di larghezza e altezza anziché i valori destro e inferiore. Quando non è stato impostato alcun rettangolo di origine, le proprietà del rettangolo di origine restituiscono le dimensioni complete del video nativo.



| Membri dati protetti                                                                   | Descrizione                                                                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| m \_ pFilter                                                                               | Puntatore a un filtro multimediale proprietario.                                                              |
| m \_ pInterfaceLock                                                                        | Sezione critica definita esternamente.                                                            |
| m \_ pPin                                                                                  | Controllo dei tipi di supporti per la connessione.                                                      |
| Funzioni di membro                                                                         | Descrizione                                                                                     |
| [**CBaseControlVideo**](cbasecontrolvideo-cbasecontrolvideo.md)                         | Costruisce un **oggetto CBaseControlVideo.**                                                      |
| [**CopyImage**](cbasecontrolvideo-copyimage.md)                                         | Crea una copia di memoria di un'immagine video.                                                         |
| [**GetImageSize**](cbasecontrolvideo-getimagesize.md)                                   | Recupera le informazioni sulle dimensioni dell'immagine video.                                                         |
| [**SetControlVideoPin**](cbasecontrolvideo-setcontrolvideopin.md)                       | Imposta il segnaposto con cui l'oggetto deve essere sincronizzato.                                         |
| Funzioni membro sottoponibili a override                                                             | Descrizione                                                                                     |
| [**CheckSourceRect**](cbasecontrolvideo-checksourcerect.md)                             | Determina se un rettangolo di origine è valido.                                                      |
| [**CheckTargetRect**](cbasecontrolvideo-checktargetrect.md)                             | Determina se un rettangolo di destinazione è valido.                                                      |
| [**GetSourceRect**](cbasecontrolvideo-getsourcerect.md)                                 | Recupera il rettangolo video di origine corrente (virtuale puro).                                    |
| [**GetStaticImage**](cbasecontrolvideo-getstaticimage.md)                               | Restituisce l'immagine corrente in un buffer di memoria (virtuale puro).                                    |
| [**GetTargetRect**](cbasecontrolvideo-gettargetrect.md)                                 | Recupera il rettangolo video di destinazione corrente (virtuale puro).                                    |
| [**GetVideoFormat**](cbasecontrolvideo-getvideoformat.md)                               | Recupera la struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) contenente il formato video. |
| [**IsDefaultSourceRect**](cbasecontrolvideo-isdefaultsourcerect.md)                     | Determina se il renderer usa il rettangolo di origine predefinito (virtuale puro).                |
| [**IsDefaultTargetRect**](cbasecontrolvideo-isdefaulttargetrect.md)                     | Determina se il renderer usa il rettangolo di destinazione predefinito (virtuale puro).                |
| [**OnUpdateRectangles**](cbasecontrolvideo-onupdaterectangles.md)                       | Chiamato quando cambia il rettangolo di origine o di destinazione.                                             |
| [**OnVideoSizeChange**](cbasecontrolvideo-onvideosizechange.md)                         | Passa EC \_ VIDEO \_ SIZE CHANGED \_ all'applicazione.                                             |
| [**SetDefaultSourceRect**](cbasecontrolvideo-setdefaultsourcerect.md)                   | Imposta il rettangolo video di origine predefinito (virtuale puro).                                         |
| [**SetDefaultTargetRect**](cbasecontrolvideo-setdefaulttargetrect.md)                   | Imposta il rettangolo video di destinazione predefinito (virtuale puro).                                         |
| [**SetSourceRect**](cbasecontrolvideo-setsourcerect.md)                                 | Imposta il rettangolo video di origine corrente (virtuale puro).                                         |
| [**SetTargetRect**](cbasecontrolvideo-settargetrect.md)                                 | Imposta il rettangolo di destinazione corrente (virtuale puro).                                               |
| Metodi di IBasicVideo                                                                      | Descrizione                                                                                     |
| [**get \_ AvgTimePerFrame**](cbasecontrolvideo-get-avgtimeperframe.md)                    | Recupera un tempo medio approssimativo per ogni fotogramma.                                                |
| [**get \_ BitErrorRate**](cbasecontrolvideo-get-biterrorrate.md)                          | Recupera una frequenza di errore in bit approssimativa.                                                        |
| [**get \_ BitRate**](cbasecontrolvideo-get-bitrate.md)                                    | Recupera una velocità in bit approssimativa per il video.                                                |
| [**GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md)                             | Recupera un rendering in memoria dell'immagine corrente.                                              |
| [**get \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md)                | Recupera l'altezza del rettangolo di destinazione corrente.                                           |
| [**get \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md)                    | Recupera la coordinata sinistra del rettangolo di destinazione corrente.                                  |
| [**GetDestinationPosition**](cbasecontrolvideo-getdestinationposition.md)               | Recupera la posizione di destinazione corrente.                                                     |
| [**get \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md)                      | Recupera la coordinata superiore del rettangolo di destinazione corrente.                                   |
| [**get \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)                  | Recupera la larghezza del rettangolo di destinazione corrente.                                            |
| [**get \_ SourceHeight**](cbasecontrolvideo-get-sourceheight.md)                          | Recupera l'altezza del rettangolo di origine corrente.                                                |
| [**get \_ SourceLeft**](cbasecontrolvideo-get-sourceleft.md)                              | Recupera la coordinata sinistra del rettangolo di origine corrente.                                       |
| [**GetSourcePosition**](cbasecontrolvideo-getsourceposition.md)                         | Recupera la posizione di origine corrente.                                                          |
| [**get \_ SourceTop**](cbasecontrolvideo-get-sourcetop.md)                                | Recupera la coordinata superiore del rettangolo di origine corrente.                                        |
| [**get \_ SourceWidth**](cbasecontrolvideo-get-sourcewidth.md)                            | Recupera la larghezza del rettangolo di origine corrente.                                                 |
| [**ottenere \_ VideoHeight**](cbasecontrolvideo-get-videoheight.md)                            | Recupera l'altezza del video nativo.                                                              |
| [**GetVideoPaletteEntries**](cbasecontrolvideo-getvideopaletteentries.md)               | Recupera un intervallo di voci della tavolozza per il video.                                             |
| [**GetVideoSize**](cbasecontrolvideo-getvideosize.md)                                   | Recupera la larghezza e l'altezza del video nativo.                                             |
| [**ottenere \_ VideoWidth**](cbasecontrolvideo-get-videowidth.md)                              | Recupera la larghezza nativa del video.                                                               |
| [**IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md)         | Determina se il renderer usa la finestra di destinazione predefinita.                             |
| [**IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md)                   | Determina se il renderer usa la finestra di origine predefinita.                                  |
| [**put \_ DestinationHeight**](cbasecontrolvideo-put-destinationheight.md)                | Imposta l'altezza del rettangolo di destinazione.                                                        |
| [**put \_ DestinationLeft**](cbasecontrolvideo-put-destinationleft.md)                    | Imposta la coordinata sinistra del rettangolo di destinazione.                                               |
| [**put \_ DestinationTop**](cbasecontrolvideo-put-destinationtop.md)                      | Imposta la coordinata superiore del rettangolo di destinazione.                                                |
| [**put \_ DestinationWidth**](cbasecontrolvideo-put-destinationwidth.md)                  | Imposta la larghezza del rettangolo di destinazione.                                                         |
| [**put \_ SourceHeight**](cbasecontrolvideo-put-sourceheight.md)                          | Imposta l'altezza del rettangolo di origine.                                                             |
| [**put \_ SourceLeft**](cbasecontrolvideo-put-sourceleft.md)                              | Imposta la coordinata sinistra del rettangolo di origine.                                                    |
| [**put \_ SourceTop**](cbasecontrolvideo-put-sourcetop.md)                                | Imposta la coordinata superiore del rettangolo di origine.                                                     |
| [**put \_ SourceWidth**](cbasecontrolvideo-put-sourcewidth.md)                            | Imposta la larghezza del rettangolo di origine.                                                              |
| [**SetDefaultDestinationPosition**](cbasecontrolvideo-setdefaultdestinationposition.md) | Imposta di nuovo la posizione di destinazione predefinita.                                                    |
| [**SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md)           | Imposta di nuovo la posizione di origine predefinita.                                                         |
| [**SetDestinationPosition**](cbasecontrolvideo-setdestinationposition.md)               | Imposta la posizione del rettangolo di destinazione.                                                        |
| [**SetSourcePosition**](cbasecontrolvideo-setsourceposition.md)                         | Imposta la posizione del rettangolo di origine.                                                             |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Classi di base](directshow-base-classes.md)
</dt> </dl>

 

 



