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
ms.openlocfilehash: c4b53cc5ce1b209cc7de9d68648b68096e5c4911
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225441"
---
# <a name="cbasecontrolwindow-class"></a>Classe CBaseControlWindow

![gerarchia di classi CBaseControlWindow](images/wctrl01.png)

La classe **CBaseControlWindow** implementa l'interfaccia [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e controlla l'accesso esterno al filtro associato. È necessario sincronizzare l'oggetto **CBaseControlWindow** con il filtro passandogli un puntatore a un oggetto di sincronizzazione della sezione critica. La classe **CBaseControlWindow** fornisce un numero di metodi che restituiscono le impostazioni delle proprietà senza gestire questa sezione critica. Ad esempio, la chiamata a [**CBaseControlWindow:: Get \_ AutoShow**](cbasecontrolwindow-get-autoshow.md) per recuperare il valore del membro dati **m \_ bAutoShow** blocca la sezione critica. È tuttavia possibile che nel filtro sia già presente una sezione critica interna bloccata, che potrebbe violare la gerarchia di blocco del filtro. Al contrario, la chiamata della funzione membro [**CBaseControlWindow:: IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) restituisce il valore richiesto senza influire sulla sezione critica.

Tutti i metodi [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) implementati da **CBaseControlWindow** richiedono che il filtro sia connesso correttamente con il filtro upstream. Per questo motivo, gli oggetti classe richiedono un pin di sincronizzazione, che è possibile impostare chiamando il metodo [**CBaseControlWindow:: SetControlWindowPin**](cbasecontrolwindow-setcontrolwindowpin.md) . Ogni volta che si chiama un metodo **IVideoWindow** , l'oggetto **CBaseControlWindow** verifica che il pin sia ancora connesso.



| Membri dati protetti                                                     | Descrizione                                                                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| \_bAutoShow m                                                               | Risultato quando lo stato cambia.                                                                                                              |
| \_bCursorHidden m                                                           | Determinazione dell'eventuale visualizzazione o dell'occultamento del cursore.                                                                                 |
| \_BorderColour m                                                            | Colore del bordo della finestra corrente.                                                                                                         |
| \_hwndDrain m                                                               | Handle di finestra a cui vengono inviati i messaggi ricevuti.                                                                                        |
| \_hwndOwner m                                                               | Finestra proprietaria.                                                                                                                              |
| \_pFilter m                                                                 | Puntatore al filtro supporti proprietario.                                                                                                         |
| \_pInterfaceLock m                                                          | Sezione critica definita esternamente.                                                                                                        |
| \_pPin m                                                                    | Controllo dei tipi di supporto per la connessione.                                                                                                  |
| Funzioni di membro                                                           | Descrizione                                                                                                                                 |
| [**CBaseControlWindow**](cbasecontrolwindow-cbasecontrolwindow.md)        | Costruisce un oggetto **CBaseControlWindow** .                                                                                                 |
| [**DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md)            | Recupera gli stili tipici o estesi della finestra.                                                                                     |
| [**DoSetWindowStyle**](cbasecontrolwindow-dosetwindowstyle.md)            | Imposta gli stili di finestra tipici o estesi.                                                                                                 |
| [**GetBorderColour**](cbasecontrolwindow-getbordercolour.md)              | Recupera il colore del bordo corrente. Si tratta di una funzione membro helper.                                                                       |
| [**GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md)                | Recupera la finestra proprietaria. Si tratta di una funzione membro helper.                                                                              |
| [**IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md)          | Recupera informazioni sull'eventuale visualizzazione automatica della finestra video quando il filtro di rendering viene sospeso o eseguito.                        |
| [**IsCursorHidden**](cbasecontrolwindow-iscursorhidden.md)                | Recupera lo stato corrente del membro dati **m \_ bCursorHidden** senza bloccare la sezione critica. Si tratta di una funzione membro helper. |
| [**PossiblyEatMessage**](cbasecontrolwindow-possiblyeatmessage.md)        | Distribuisce i messaggi alla finestra padre.                                                                                                  |
| [**SetControlWindowPin**](cbasecontrolwindow-setcontrolwindowpin.md)      | Notifica all'oggetto il pin a cui si applica.                                                                                         |
| Metodi IVideoWindow                                                       | Descrizione                                                                                                                                 |
| [**ottenere la \_ visualizzazione**](cbasecontrolwindow-get-autoshow.md)                   | Recupera l'impostazione corrente del flag di visualizzazione.                                                                                                |
| [**ottenere \_ BackgroundPalette**](cbasecontrolwindow-get-backgroundpalette.md) | Recupera la tavolozza realizzata nel flag di sfondo.                                                                                      |
| [**ottenere \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md)             | Recupera il colore del bordo corrente.                                                                                                         |
| [**ottenere la \_ didascalia**](cbasecontrolwindow-get-caption.md)                     | Recupera la didascalia della finestra corrente.                                                                                                       |
| [**ottenere \_ FullScreenMode**](cbasecontrolwindow-get-fullscreenmode.md)      | Recupera la modalità a schermo intero corrente.                                                                                                     |
| [**Ottieni \_ altezza**](cbasecontrolwindow-get-height.md)                       | Recupera l'altezza della finestra corrente.                                                                                                        |
| [**\_lascia**](cbasecontrolwindow-get-left.md)                           | Recupera la coordinata corrente della finestra a sinistra.                                                                                               |
| [**GetMaxIdealImageSize**](cbasecontrolwindow-getmaxidealimagesize.md)    | Recupera le dimensioni massime dell'immagine ideale.                                                                                              |
| [**ottenere \_ MessageDrain**](cbasecontrolwindow-get-messagedrain.md)           | Recupera lo svuotamento del messaggio corrente.                                                                                                        |
| [**GetMinIdealImageSize**](cbasecontrolwindow-getminidealimagesize.md)    | Recupera le dimensioni minime dell'immagine ideale.                                                                                              |
| [**Ottieni \_ proprietario**](cbasecontrolwindow-get-owner.md)                         | Recupera l'handle della finestra padre.                                                                                                         |
| [**GetRestorePosition**](cbasecontrolwindow-getrestoreposition.md)        | Recupera la posizione in cui verrà ripristinata la finestra quando viene ingrandita o ridotta a icona.                                                    |
| [**Ottieni \_ Top**](cbasecontrolwindow-get-top.md)                             | Recupera la coordinata y della parte superiore della finestra.                                                                                       |
| [**Leggi \_ visibile**](cbasecontrolwindow-get-visible.md)                     | Recupera l'impostazione di visibilità corrente della finestra.                                                                                     |
| [**Ottieni \_ larghezza**](cbasecontrolwindow-get-width.md)                         | Recupera la larghezza della finestra.                                                                                                          |
| [**GetWindowPosition**](cbasecontrolwindow-getwindowposition.md)          | Recupera le coordinate della finestra corrente.                                                                                                   |
| [**ottenere \_ WindowState**](cbasecontrolwindow-get-windowstate.md)             | Recupera lo stato corrente della finestra.                                                                                                  |
| [**ottenere \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md)             | Recupera gli stili della finestra standard.                                                                                                       |
| [**ottenere \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md)         | Recupera gli stili della finestra estesa.                                                                                                       |
| [**HideCursor**](cbasecontrolwindow-hidecursor.md)                        | Nasconde o Visualizza il cursore.                                                                                                               |
| [**IsCursorHidden**](cbasecontrolwindow-iscursorhidden.md)                | Recupera lo stato corrente del membro dati **m \_ bCursorHidden** .                                                                        |
| [**NotifyOwnerMessage**](cbasecontrolwindow-notifyownermessage.md)        | Passa i messaggi inviati alle finestre proprietarie.                                                                                         |
| [**Inserisci \_ AutoShow**](cbasecontrolwindow-put-autoshow.md)                   | Imposta la proprietà AutoShow.                                                                                                                 |
| [**Inserisci \_ BackgroundPalette**](cbasecontrolwindow-put-backgroundpalette.md) | Imposta un flag per realizzare la tavolozza in background.                                                                                       |
| [**Inserisci \_ BorderColor**](cbasecontrolwindow-put-bordercolor.md)             | Imposta il colore del bordo corrente.                                                                                                              |
| [**Inserisci \_ didascalia**](cbasecontrolwindow-put-caption.md)                     | Imposta la didascalia della finestra corrente.                                                                                                            |
| [**Inserisci \_ FullScreenMode**](cbasecontrolwindow-put-fullscreenmode.md)      | Imposta la modalità a schermo intero.                                                                                                                  |
| [**\_altezza put**](cbasecontrolwindow-put-height.md)                       | Imposta l'altezza corrente della finestra.                                                                                                             |
| [**Inserisci a \_ sinistra**](cbasecontrolwindow-put-left.md)                           | Imposta la coordinata sinistra della finestra.                                                                                                    |
| [**Inserisci \_ MessageDrain**](cbasecontrolwindow-put-messagedrain.md)           | Imposta la finestra di svuotamento del messaggio.                                                                                                              |
| [**Inserisci \_ proprietario**](cbasecontrolwindow-put-owner.md)                         | Imposta l'handle della finestra padre di Microsoft Win32.                                                                                              |
| [**Inserisci in \_ alto**](cbasecontrolwindow-put-top.md)                             | Imposta la posizione per la parte superiore della finestra.                                                                                                |
| [**Inserisci \_ visibile**](cbasecontrolwindow-put-visible.md)                     | Nasconde o Mostra la finestra.                                                                                                                  |
| [**Inserisci \_ larghezza**](cbasecontrolwindow-put-width.md)                         | Imposta la larghezza della finestra.                                                                                                               |
| [**Inserisci \_ WindowState**](cbasecontrolwindow-put-windowstate.md)             | Imposta lo stato della finestra.                                                                                                               |
| [**Inserisci \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md)             | Imposta gli stili della finestra standard.                                                                                                            |
| [**Inserisci \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md)         | Imposta gli stili della finestra estesa.                                                                                                            |
| [**SetWindowForeground**](cbasecontrolwindow-setwindowforeground.md)      | Imposta la finestra in primo piano.                                                                                                          |
| [**SetWindowPosition**](cbasecontrolwindow-setwindowposition.md)          | Imposta la posizione della finestra.                                                                                                                   |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi base di DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 



