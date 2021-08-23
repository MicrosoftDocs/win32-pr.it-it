---
description: La classe CBaseControlWindow implementa l'interfaccia IVideoWindow e controlla l'accesso esterno al filtro associato.
ms.assetid: 3657ba24-ffaa-491f-9eb3-f9913d5d421a
title: Classe CBaseControlWindow
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow
api_type:
- COM
api_location: ''
ms.openlocfilehash: 500706531d7e7a934681dabe3bcd00b7de0d80e42b8bbf27a5456a8fd4415f21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017235"
---
# <a name="cbasecontrolwindow-class"></a>Classe CBaseControlWindow

![Gerarchia di classi cbasecontrolwindow](images/wctrl01.png)

La **classe CBaseControlWindow** implementa l'interfaccia [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e controlla l'accesso esterno al filtro associato. È necessario sincronizzare **l'oggetto CBaseControlWindow** con il filtro passando un puntatore a un oggetto di sincronizzazione della sezione critica. La **classe CBaseControlWindow** fornisce diversi metodi che restituiscono le impostazioni delle proprietà senza gestire questa sezione critica. Ad esempio, la chiamata [**a CBaseControlWindow::get \_ AutoShow**](cbasecontrolwindow-get-autoshow.md) per recuperare il valore del membro dati **m \_ bAutoShow** blocca la sezione critica. È tuttavia possibile che il filtro abbia già una sezione critica interna bloccata, che potrebbe violare la gerarchia di blocco del filtro. Al contrario, la chiamata alla funzione membro [**CBaseControlWindow::IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) restituisce il valore richiesto senza influire sulla sezione critica.

Tutti i metodi [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) implementati da **CBaseControlWindow** richiedono che il filtro sia connesso correttamente con il filtro upstream. Per questo motivo, gli oggetti classe richiedono un pin di sincronizzazione, che viene impostato chiamando il metodo [**CBaseControlWindow::SetControlWindowPin.**](cbasecontrolwindow-setcontrolwindowpin.md) Ogni volta che **chiami un metodo IVideoWindow,** l'oggetto **CBaseControlWindow** verifica che il pin sia ancora connesso.



| Membri dati protetti                                                     | Descrizione                                                                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| m \_ bAutoShow                                                               | Risultato quando lo stato cambia.                                                                                                              |
| m \_ bCursorHidden                                                           | Determina se il cursore è visualizzato o nascosto.                                                                                 |
| m \_ BorderColour                                                            | Colore del bordo della finestra corrente.                                                                                                         |
| m \_ hwndDrain                                                               | Handle di finestra in cui vengono inviati i messaggi ricevuti.                                                                                        |
| m \_ hwndOwner                                                               | Finestra proprietaria.                                                                                                                              |
| m \_ pFilter                                                                 | Puntatore al filtro multimediale proprietario.                                                                                                         |
| m \_ pInterfaceLock                                                          | Sezione critica definita esternamente.                                                                                                        |
| m \_ pPin                                                                    | Controllo dei tipi di supporti per la connessione.                                                                                                  |
| Funzioni di membro                                                           | Descrizione                                                                                                                                 |
| [**CBaseControlWindow**](cbasecontrolwindow-cbasecontrolwindow.md)        | Costruisce un **oggetto CBaseControlWindow.**                                                                                                 |
| [**DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md)            | Recupera gli stili di finestra tipici o estesi.                                                                                     |
| [**DoSetWindowStyle**](cbasecontrolwindow-dosetwindowstyle.md)            | Imposta gli stili di finestra tipici o estesi.                                                                                                 |
| [**GetBorderColour**](cbasecontrolwindow-getbordercolour.md)              | Recupera il colore del bordo corrente. Si tratta di una funzione membro helper.                                                                       |
| [**GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md)                | Recupera la finestra proprietaria. Si tratta di una funzione membro helper.                                                                              |
| [**IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md)          | Recupera informazioni sulla visualizzazione automatica della finestra video quando il filtro di rendering viene sospeso o eseguito.                        |
| [**IsCursorHidden**](cbasecontrolwindow-iscursorhidden.md)                | Recupera lo stato corrente del membro dati **m \_ bCursorHidden** senza bloccare la sezione critica. Si tratta di una funzione membro helper. |
| [**PossiblyEatMessage**](cbasecontrolwindow-possiblyeatmessage.md)        | Distribuisce i messaggi nella finestra padre.                                                                                                  |
| [**SetControlWindowPin**](cbasecontrolwindow-setcontrolwindowpin.md)      | Notifica all'oggetto il pin a cui si applica.                                                                                         |
| Metodi IVideoWindow                                                       | Descrizione                                                                                                                                 |
| [**get \_ AutoShow**](cbasecontrolwindow-get-autoshow.md)                   | Recupera l'impostazione corrente del flag AutoShow.                                                                                                |
| [**get \_ BackgroundPalette**](cbasecontrolwindow-get-backgroundpalette.md) | Recupera la tavolozza realizzato nel flag di sfondo.                                                                                      |
| [**get \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md)             | Recupera il colore del bordo corrente.                                                                                                         |
| [**Get \_ Caption**](cbasecontrolwindow-get-caption.md)                     | Recupera la didascalia della finestra corrente.                                                                                                       |
| [**get \_ FullScreenMode**](cbasecontrolwindow-get-fullscreenmode.md)      | Recupera la modalità schermo intero corrente.                                                                                                     |
| [**get \_ Height**](cbasecontrolwindow-get-height.md)                       | Recupera l'altezza della finestra corrente.                                                                                                        |
| [**get \_ Left**](cbasecontrolwindow-get-left.md)                           | Recupera la coordinata corrente della finestra sinistra.                                                                                               |
| [**GetMaxIdealImageSize**](cbasecontrolwindow-getmaxidealimagesize.md)    | Recupera le dimensioni massime dell'immagine ideale.                                                                                              |
| [**get \_ MessageDrain**](cbasecontrolwindow-get-messagedrain.md)           | Recupera lo svuotamento dei messaggi corrente.                                                                                                        |
| [**GetMinIdealImageSize**](cbasecontrolwindow-getminidealimagesize.md)    | Recupera le dimensioni minime dell'immagine ideale.                                                                                              |
| [**get \_ Owner**](cbasecontrolwindow-get-owner.md)                         | Recupera l'handle della finestra padre.                                                                                                         |
| [**GetRestorePosition**](cbasecontrolwindow-getrestoreposition.md)        | Recupera la posizione in cui verrà ripristinata la finestra quando viene ingrandita o ridotta a icona.                                                    |
| [**get \_ Top**](cbasecontrolwindow-get-top.md)                             | Recupera la coordinata y per la parte superiore della finestra.                                                                                       |
| [**get \_ Visible**](cbasecontrolwindow-get-visible.md)                     | Recupera l'impostazione di visibilità corrente della finestra.                                                                                     |
| [**get \_ Width**](cbasecontrolwindow-get-width.md)                         | Recupera la larghezza della finestra.                                                                                                          |
| [**GetWindowPosition**](cbasecontrolwindow-getwindowposition.md)          | Recupera le coordinate della finestra corrente.                                                                                                   |
| [**get \_ WindowState**](cbasecontrolwindow-get-windowstate.md)             | Recupera lo stato corrente della finestra.                                                                                                  |
| [**get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md)             | Recupera gli stili di finestra standard.                                                                                                       |
| [**get \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md)         | Recupera gli stili di finestra estesi.                                                                                                       |
| [**HideCursor**](cbasecontrolwindow-hidecursor.md)                        | Nasconde o visualizza il cursore.                                                                                                               |
| [**IsCursorHidden**](cbasecontrolwindow-iscursorhidden.md)                | Recupera lo stato corrente del membro **\_ dati m bCursorHidden.**                                                                        |
| [**NotifyOwnerMessage**](cbasecontrolwindow-notifyownermessage.md)        | Passa i messaggi inviati alle finestre proprietarie.                                                                                         |
| [**put \_ AutoShow**](cbasecontrolwindow-put-autoshow.md)                   | Imposta la proprietà AutoShow.                                                                                                                 |
| [**put \_ BackgroundPalette**](cbasecontrolwindow-put-backgroundpalette.md) | Imposta un flag per realizzare la tavolozza sullo sfondo.                                                                                       |
| [**put \_ BorderColor**](cbasecontrolwindow-put-bordercolor.md)             | Imposta il colore del bordo corrente.                                                                                                              |
| [**Put \_ Caption**](cbasecontrolwindow-put-caption.md)                     | Imposta la didascalia della finestra corrente.                                                                                                            |
| [**put \_ FullScreenMode**](cbasecontrolwindow-put-fullscreenmode.md)      | Imposta la modalità schermo intero.                                                                                                                  |
| [**put \_ Height**](cbasecontrolwindow-put-height.md)                       | Imposta l'altezza della finestra corrente.                                                                                                             |
| [**put \_ Left**](cbasecontrolwindow-put-left.md)                           | Imposta la coordinata sinistra per la finestra.                                                                                                    |
| [**put \_ MessageDrain**](cbasecontrolwindow-put-messagedrain.md)           | Imposta la finestra di svuotamento dei messaggi.                                                                                                              |
| [**put \_ Owner**](cbasecontrolwindow-put-owner.md)                         | Imposta l'handle della finestra padre Microsoft Win32.                                                                                              |
| [**put \_ Top**](cbasecontrolwindow-put-top.md)                             | Imposta la posizione per la parte superiore della finestra.                                                                                                |
| [**put \_ Visible**](cbasecontrolwindow-put-visible.md)                     | Nasconde o mostra la finestra.                                                                                                                  |
| [**Put \_ Width**](cbasecontrolwindow-put-width.md)                         | Imposta la larghezza della finestra.                                                                                                               |
| [**put \_ WindowState**](cbasecontrolwindow-put-windowstate.md)             | Imposta lo stato della finestra.                                                                                                               |
| [**put \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md)             | Imposta gli stili di finestra standard.                                                                                                            |
| [**put \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md)         | Imposta gli stili di finestra estesi.                                                                                                            |
| [**SetWindowForeground**](cbasecontrolwindow-setwindowforeground.md)      | Imposta la finestra in primo piano.                                                                                                          |
| [**SetWindowPosition**](cbasecontrolwindow-setwindowposition.md)          | Imposta la posizione della finestra.                                                                                                                   |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Classi di base](directshow-base-classes.md)
</dt> </dl>

 

 



