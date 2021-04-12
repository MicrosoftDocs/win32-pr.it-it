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
ms.openlocfilehash: e2e5962eb9d175bfbbeadd149a547f0d36fbf49f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482212"
---
# <a name="cbasecontrolvideo-class"></a>Classe CBaseControlVideo

![gerarchia di classi cbasecontrolvideo](images/wctrl02.png)

La classe **CBaseControlVideo** implementa l'interfaccia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) e controlla le proprietà video di una finestra video generica. In genere, un oggetto **CBaseControlVideo** è un renderer video che disegna video in una finestra sullo schermo.

Molte funzioni membro **CBaseControlVideo** richiedono solo che il renderer video sia connesso a un grafico di filtro. Se non è connessa, le funzioni membro restituiscono **VFW \_ E \_ non sono \_ connesse**. Le proprietà impostate su un renderer video permangono tra le connessioni successive e le disconnessioni. Tutte le applicazioni devono assicurarsi che reimpostino le proprietà del renderer prima di avviare una presentazione.

Quando si lavora con video, l'applicazione può selezionare una parte del video da usare. Questa parte è il rettangolo di origine controllato dall'oggetto **CBaseControlVideo** . **CBaseControlVideo** consente all'applicazione di impostare e recuperare il rettangolo di origine. Tutti i rettangoli utilizzati da **CBaseControlVideo** utilizzano i valori di larghezza e altezza anziché i valori a destra e in basso. Quando non è stato impostato alcun rettangolo di origine, le proprietà del rettangolo di origine restituiscono le dimensioni complete del video nativo.



| Membri dati protetti                                                                   | Descrizione                                                                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| \_pFilter m                                                                               | Puntatore a un filtro multimediale proprietario.                                                              |
| \_pInterfaceLock m                                                                        | Sezione critica definita esternamente.                                                            |
| \_pPin m                                                                                  | Controllo dei tipi di supporto per la connessione.                                                      |
| Funzioni di membro                                                                         | Descrizione                                                                                     |
| [**CBaseControlVideo**](cbasecontrolvideo-cbasecontrolvideo.md)                         | Costruisce un oggetto **CBaseControlVideo** .                                                      |
| [**CopyImage**](cbasecontrolvideo-copyimage.md)                                         | Crea una copia di memoria di un'immagine video.                                                         |
| [**GetImageSize**](cbasecontrolvideo-getimagesize.md)                                   | Recupera le informazioni sulle dimensioni dell'immagine video.                                                         |
| [**SetControlVideoPin**](cbasecontrolvideo-setcontrolvideopin.md)                       | Imposta il pin con il quale l'oggetto deve essere sincronizzato.                                         |
| Funzioni membro sottoponibili a override                                                             | Descrizione                                                                                     |
| [**CheckSourceRect**](cbasecontrolvideo-checksourcerect.md)                             | Determina se un rettangolo di origine è valido.                                                      |
| [**CheckTargetRect**](cbasecontrolvideo-checktargetrect.md)                             | Determina se un rettangolo di destinazione è valido.                                                      |
| [**GetSourceRect**](cbasecontrolvideo-getsourcerect.md)                                 | Recupera il rettangolo del video di origine corrente (virtuale puro).                                    |
| [**GetStaticImage**](cbasecontrolvideo-getstaticimage.md)                               | Restituisce l'immagine corrente in un buffer di memoria (virtuale puro).                                    |
| [**GetTargetRect**](cbasecontrolvideo-gettargetrect.md)                                 | Recupera il rettangolo del video di destinazione corrente (virtuale puro).                                    |
| [**GetVideoFormat**](cbasecontrolvideo-getvideoformat.md)                               | Recupera la struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) contenente il formato video. |
| [**IsDefaultSourceRect**](cbasecontrolvideo-isdefaultsourcerect.md)                     | Determina se il renderer usa il rettangolo di origine predefinito (puro virtuale).                |
| [**IsDefaultTargetRect**](cbasecontrolvideo-isdefaulttargetrect.md)                     | Determina se il renderer usa il rettangolo di destinazione predefinito (virtuale puro).                |
| [**OnUpdateRectangles**](cbasecontrolvideo-onupdaterectangles.md)                       | Chiamato quando viene modificato il rettangolo di origine o di destinazione.                                             |
| [**OnVideoSizeChange**](cbasecontrolvideo-onvideosizechange.md)                         | Supera \_ \_ le dimensioni del video EC \_ modificate nell'applicazione.                                             |
| [**SetDefaultSourceRect**](cbasecontrolvideo-setdefaultsourcerect.md)                   | Imposta il rettangolo del video di origine predefinito (puro virtuale).                                         |
| [**SetDefaultTargetRect**](cbasecontrolvideo-setdefaulttargetrect.md)                   | Imposta il rettangolo del video di destinazione predefinito (virtuale puro).                                         |
| [**SetSourceRect**](cbasecontrolvideo-setsourcerect.md)                                 | Imposta il rettangolo del video di origine corrente (puro virtuale).                                         |
| [**SetTargetRect**](cbasecontrolvideo-settargetrect.md)                                 | Imposta il rettangolo di destinazione corrente (virtuale puro).                                               |
| Metodi IBasicVideo                                                                      | Descrizione                                                                                     |
| [**ottenere \_ AvgTimePerFrame**](cbasecontrolvideo-get-avgtimeperframe.md)                    | Recupera un tempo medio approssimativo per fotogramma.                                                |
| [**ottenere \_ BitErrorRate**](cbasecontrolvideo-get-biterrorrate.md)                          | Recupera una frequenza di errori approssimativa di bit.                                                        |
| [**ottenere la \_ velocità in bit**](cbasecontrolvideo-get-bitrate.md)                                    | Recupera una velocità in bit approssimativa per il video.                                                |
| [**GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md)                             | Recupera un rendering della memoria dell'immagine corrente.                                              |
| [**ottenere \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md)                | Recupera l'altezza del rettangolo di destinazione corrente.                                           |
| [**ottenere \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md)                    | Recupera la coordinata sinistra del rettangolo di destinazione corrente.                                  |
| [**GetDestinationPosition**](cbasecontrolvideo-getdestinationposition.md)               | Recupera la posizione di destinazione corrente.                                                     |
| [**ottenere \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md)                      | Recupera la coordinata superiore del rettangolo di destinazione corrente.                                   |
| [**ottenere \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)                  | Recupera la larghezza del rettangolo di destinazione corrente.                                            |
| [**ottenere \_ SourceHeight**](cbasecontrolvideo-get-sourceheight.md)                          | Recupera l'altezza del rettangolo di origine corrente.                                                |
| [**ottenere \_ SourceLeft**](cbasecontrolvideo-get-sourceleft.md)                              | Recupera la coordinata sinistra del rettangolo di origine corrente.                                       |
| [**GetSourcePosition**](cbasecontrolvideo-getsourceposition.md)                         | Recupera la posizione di origine corrente.                                                          |
| [**ottenere \_ SourceTop**](cbasecontrolvideo-get-sourcetop.md)                                | Recupera la coordinata superiore del rettangolo di origine corrente.                                        |
| [**ottenere \_ SourceWidth**](cbasecontrolvideo-get-sourcewidth.md)                            | Recupera la larghezza del rettangolo di origine corrente.                                                 |
| [**ottenere \_ VideoHeight**](cbasecontrolvideo-get-videoheight.md)                            | Recupera l'altezza del video nativo.                                                              |
| [**GetVideoPaletteEntries**](cbasecontrolvideo-getvideopaletteentries.md)               | Recupera un intervallo di voci della tavolozza per il video.                                             |
| [**GetVideoSize**](cbasecontrolvideo-getvideosize.md)                                   | Recupera la larghezza e l'altezza del video nativo.                                             |
| [**ottenere \_ VideoWidth**](cbasecontrolvideo-get-videowidth.md)                              | Recupera la larghezza del video nativa.                                                               |
| [**IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md)         | Determina se il renderer utilizza la finestra di destinazione predefinita.                             |
| [**IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md)                   | Determina se il renderer utilizza la finestra di origine predefinita.                                  |
| [**Inserisci \_ DestinationHeight**](cbasecontrolvideo-put-destinationheight.md)                | Imposta l'altezza del rettangolo di destinazione.                                                        |
| [**Inserisci \_ DestinationLeft**](cbasecontrolvideo-put-destinationleft.md)                    | Imposta la coordinata sinistra del rettangolo di destinazione.                                               |
| [**Inserisci \_ DestinationTop**](cbasecontrolvideo-put-destinationtop.md)                      | Imposta la coordinata superiore del rettangolo di destinazione.                                                |
| [**Inserisci \_ DestinationWidth**](cbasecontrolvideo-put-destinationwidth.md)                  | Imposta la larghezza del rettangolo di destinazione.                                                         |
| [**Inserisci \_ SourceHeight**](cbasecontrolvideo-put-sourceheight.md)                          | Imposta l'altezza del rettangolo di origine.                                                             |
| [**Inserisci \_ SourceLeft**](cbasecontrolvideo-put-sourceleft.md)                              | Imposta la coordinata sinistra del rettangolo di origine.                                                    |
| [**Inserisci \_ SourceTop**](cbasecontrolvideo-put-sourcetop.md)                                | Imposta la coordinata superiore del rettangolo di origine.                                                     |
| [**Inserisci \_ SourceWidth**](cbasecontrolvideo-put-sourcewidth.md)                            | Imposta la larghezza del rettangolo di origine.                                                              |
| [**SetDefaultDestinationPosition**](cbasecontrolvideo-setdefaultdestinationposition.md) | Imposta di nuovo la posizione di destinazione predefinita.                                                    |
| [**SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md)           | Imposta di nuovo la posizione di origine predefinita.                                                         |
| [**SetDestinationPosition**](cbasecontrolvideo-setdestinationposition.md)               | Imposta la posizione del rettangolo di destinazione.                                                        |
| [**SetSourcePosition**](cbasecontrolvideo-setsourceposition.md)                         | Imposta la posizione del rettangolo di origine.                                                             |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi base di DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 



