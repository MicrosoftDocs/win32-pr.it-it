---
description: La classe CBaseWindow è una classe di base per la gestione di Windows.
ms.assetid: 212d179e-5b5e-49fb-bf0a-a12e0317c96a
title: Classe CBaseWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 313f1b222f3b0096d3f5bf92c15e2097afb29848
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333893"
---
# <a name="cbasewindow-class"></a>Classe CBaseWindow

La `CBaseWindow` classe è una classe di base per la gestione di Windows. I renderer video possono usare questa classe per creare finestre video. Per usare questa classe, creare una classe derivata che erediti da `CBaseWindow` . Nella classe derivata:

-   Implementare il metodo virtuale pure [**CBaseWindow:: GetClassWindowStyles**](cbasewindow-getclasswindowstyles.md), che definisce gli stili della finestra.
-   Eseguire l'override del metodo [**CBaseWindow:: OnReceiveMessage**](cbasewindow-onreceivemessage.md) , che gestisce i messaggi della finestra.
-   Implementare un distruttore che chiama il metodo [**CBaseWindow::D onewithwindow**](cbasewindow-donewithwindow.md) .

Prima di usare un'istanza della classe derivata, chiamare il metodo [**CBaseWindow::P reparewindow**](cbasewindow-preparewindow.md) .



| Variabili membro protette                                           | Descrizione                                                                    |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**\_HINSTANCE m**](cbasewindow-m-hinstance.md)                      | Handle per l'istanza del modulo.                                                 |
| [**\_HWND m**](cbasewindow-m-hwnd.md)                                | Handle per la finestra dell'oggetto.                                                 |
| [**\_HDC m**](cbasewindow-m-hdc.md)                                  | Handle per il contesto di dispositivo della finestra.                                         |
| [**\_larghezza m**](cbasewindow-m-width.md)                              | Larghezza dell'area client in pixel.                                           |
| [**\_altezza m**](cbasewindow-m-height.md)                            | Altezza dell'area client in pixel.                                          |
| [**\_bActivated m**](cbasewindow-m-bactivated.md)                    | Flag che specifica se la finestra è stata attivata.                     |
| [**\_pClassName m**](cbasewindow-m-pclassname.md)                    | Stringa statica che contiene il nome della classe della finestra.                      |
| [**\_ClassStyles m**](cbasewindow-m-classstyles.md)                  | Stili della classe per la finestra.                                                   |
| [**\_WindowStyles m**](cbasewindow-m-windowstyles.md)                | Stili di finestra per la finestra.                                                  |
| [**\_WindowStylesEx m**](cbasewindow-m-windowstylesex.md)            | Stili di finestra estesi per la finestra.                                         |
| [**\_ShowStageMessage m**](cbasewindow-m-showstagemessage.md)        | Messaggio privato che consente di portare la finestra in primo piano.                      |
| [**\_ShowStageTop m**](cbasewindow-m-showstagetop.md)                | Messaggio privato che imposta lo stile della finestra su WS ex in primo piano \_ \_ .                 |
| [**\_RealizePalette m**](cbasewindow-m-realizepalette.md)            | Messaggio privato che realizza la tavolozza.                                     |
| [**\_MemoryDC m**](cbasewindow-m-memorydc.md)                        | Handle per il contesto di dispositivo di memoria.                                           |
| [**\_hPalette m**](cbasewindow-m-hpalette.md)                        | Handle per la tavolozza della finestra.                                                |
| [**\_bNoRealize m**](cbasewindow-m-bnorealize.md)                    | Flag che specifica se la finestra deve realizzare la propria tavolozza.             |
| [**\_bBackground m**](cbasewindow-m-bbackground.md)                  | Flag che specifica se la tavolozza deve essere una tavolozza di sfondo.        |
| [**\_bRealizing m**](cbasewindow-m-brealizing.md)                    | Flag che specifica se è in corso la realizzazione di una nuova tavolozza.                   |
| [**\_WindowLock m**](cbasewindow-m-windowlock.md)                    | Sezione critica, per serializzare l'accesso all'oggetto.                           |
| [**\_bDoGetDC m**](cbasewindow-m-bdogetdc.md)                        | Flag che specifica se recuperare il contesto di dispositivo.                    |
| [**\_bDoPostToDestroy m**](cbasewindow-m-bdoposttodestroy.md)        | Flag che specifica se la finestra Invia o invia il messaggio di distruzione. |
| Metodi protetti                                                    | Descrizione                                                                    |
| [**OnPaletteChange**](cbasewindow-onpalettechange.md)               | Gestisce i messaggi di modifica della tavolozza. Virtuale.                                      |
| Metodi pubblici                                                       | Descrizione                                                                    |
| [**CBaseWindow**](cbasewindow-cbasewindow.md)                       | Metodo del costruttore.                                                            |
| [**DoneWithWindow**](cbasewindow-donewithwindow.md)                 | Elimina definitivamente la finestra. Virtuale.                                                  |
| [**PrepareWindow**](cbasewindow-preparewindow.md)                   | Crea la finestra. Virtuale.                                                   |
| [**InactivateWindow**](cbasewindow-inactivatewindow.md)             | Disattiva la finestra. Virtuale.                                               |
| [**ActivateWindow**](cbasewindow-activatewindow.md)                 | Ridimensiona la finestra in base ai requisiti della classe derivata. Virtuale.  |
| [**OnSize**](cbasewindow-onsize.md)                                 | Gestisce \_ i messaggi di dimensioni WM. Virtuale.                                            |
| [**OnClose**](cbasewindow-onclose.md)                               | Gestisce \_ i messaggi di chiusura WM. Virtuale.                                           |
| [**GetDefaultRect**](cbasewindow-getdefaultrect.md)                 | Recupera le dimensioni predefinite dell'area client. Virtuale.                        |
| [**UninitialiseWindow**](cbasewindow-uninitialisewindow.md)         | Rilascia le risorse della finestra. Virtuale.                                      |
| [**InitialiseWindow**](cbasewindow-initialisewindow.md)             | Inizializza la finestra. Virtuale.                                               |
| [**CompleteConnect**](cbasewindow-completeconnect.md)               | Notifica alla finestra che il pin di input del renderer è stato connesso.          |
| [**DoCreateWindow**](cbasewindow-docreatewindow.md)                 | Crea la finestra.                                                            |
| [**PerformanceAlignWindow**](cbasewindow-performancealignwindow.md) | Allinea la finestra a un limite **DWORD** , per ottenere le prestazioni massime.            |
| [**DoShowWindow**](cbasewindow-doshowwindow.md)                     | Imposta lo stato di visualizzazione della finestra.                                                  |
| [**PaintWindow**](cbasewindow-paintwindow.md)                       | Consente di ridisegnare la finestra.                                             |
| [**DoSetWindowForeground**](cbasewindow-dosetwindowforeground.md)   | Consente di portare la finestra in primo piano.                                           |
| [**SetPalette**](cbasewindow-setpalette.md)                         | Installa una tavolozza per la finestra. Virtuale.                                    |
| [**Rendi conto**](cbasewindow-setrealize.md)                         | Specifica se la finestra realizza le tavolozze.                                |
| [**DoRealisePalette**](cbasewindow-dorealisepalette.md)             | Realizza la tavolozza corrente della finestra. Virtuale.                                |
| [**PossiblyEatMessage**](cbasewindow-possiblyeatmessage.md)         | Consente a una classe derivata di inviare messaggi a un'altra finestra. Virtuale.        |
| [**GetWindowWidth**](cbasewindow-getwindowwidth.md)                 | Recupera la larghezza corrente della finestra.                                     |
| [**GetWindowHeight**](cbasewindow-getwindowheight.md)               | Recupera l'altezza corrente della finestra.                                    |
| [**GetWindowHWND**](cbasewindow-getwindowhwnd.md)                   | Recupera un handle per la finestra.                                              |
| [**GetMemoryHDC**](cbasewindow-getmemoryhdc.md)                     | Recupera un handle per il contesto di dispositivo di memoria.                               |
| [**GetWindowHDC**](cbasewindow-getwindowhdc.md)                     | Recupera un handle per il contesto di dispositivo della finestra.                             |
| [**OnReceiveMessage**](cbasewindow-onreceivemessage.md)             | Gestisce i messaggi della finestra. Virtuale.                                              |
| [**UnsetPalette**](cbasewindow-unsetpalette.md)                     | Elimina la tavolozza corrente della finestra e ripristina la tavolozza di sistema predefinita.  |
| Metodi virtuali puri                                                 | Descrizione                                                                    |
| [**GetClassWindowStyles**](cbasewindow-getclasswindowstyles.md)     | Recupera gli stili di classe e di finestra della finestra.                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




