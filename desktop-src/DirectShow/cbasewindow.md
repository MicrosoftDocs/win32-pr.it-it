---
description: La classe CBaseWindow è una classe di base per la gestione delle finestre.
ms.assetid: 212d179e-5b5e-49fb-bf0a-a12e0317c96a
title: Classe CBaseWindow (Winutil.h)
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
ms.openlocfilehash: 60d2a3004343df7846d4bf600690bc6a1e45b46111f91828c7de31219a751308
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657194"
---
# <a name="cbasewindow-class"></a>Classe CBaseWindow

La `CBaseWindow` classe è una classe di base per la gestione delle finestre. I renderer video possono usare questa classe per creare finestre video. Per usare questa classe, creare una classe derivata che eredita da `CBaseWindow` . Nella classe derivata:

-   Implementare il metodo virtuale [**puro CBaseWindow::GetClassWindowStyles**](cbasewindow-getclasswindowstyles.md), che definisce gli stili della finestra.
-   Eseguire [**l'override del metodo CBaseWindow::OnReceiveMessage,**](cbasewindow-onreceivemessage.md) che gestisce i messaggi della finestra.
-   Implementare un distruttore che chiama il [**metodo CBaseWindow::D oneWithWindow.**](cbasewindow-donewithwindow.md)

Prima di usare un'istanza della classe derivata, chiamare il [**metodo CBaseWindow::P repareWindow.**](cbasewindow-preparewindow.md)



| Variabili membro protette                                           | Descrizione                                                                    |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**m \_ hInstance**](cbasewindow-m-hinstance.md)                      | Handle per l'istanza del modulo.                                                 |
| [**m \_ hwnd**](cbasewindow-m-hwnd.md)                                | Handle per la finestra dell'oggetto.                                                 |
| [**m \_ hdc**](cbasewindow-m-hdc.md)                                  | Handle per il contesto di dispositivo della finestra.                                         |
| [**m \_ Width**](cbasewindow-m-width.md)                              | Larghezza dell'area client, in pixel.                                           |
| [**m \_ Height**](cbasewindow-m-height.md)                            | Altezza dell'area client, in pixel.                                          |
| [**m \_ bActivated**](cbasewindow-m-bactivated.md)                    | Flag che specifica se la finestra è stata attivata.                     |
| [**m \_ pClassName**](cbasewindow-m-pclassname.md)                    | Stringa statica che contiene il nome della classe della finestra.                      |
| [**m \_ ClassStyles**](cbasewindow-m-classstyles.md)                  | Stili di classe per la finestra.                                                   |
| [**m \_ WindowStyles**](cbasewindow-m-windowstyles.md)                | Stili di finestra per la finestra.                                                  |
| [**m \_ WindowStylesEx**](cbasewindow-m-windowstylesex.md)            | Stili di finestra estesi per la finestra.                                         |
| [**m \_ ShowStageMessage**](cbasewindow-m-showstagemessage.md)        | Messaggio privato che porta la finestra in primo piano.                      |
| [**m \_ ShowStageTop**](cbasewindow-m-showstagetop.md)                | Messaggio privato che imposta lo stile della finestra su WS \_ EX \_ TOPMOST.                 |
| [**m \_ RealizePalette**](cbasewindow-m-realizepalette.md)            | Messaggio privato che realizza la tavolozza.                                     |
| [**m \_ MemoryDC**](cbasewindow-m-memorydc.md)                        | Handle per il contesto di dispositivo di memoria.                                           |
| [**m \_ hPalette**](cbasewindow-m-hpalette.md)                        | Handle per la tavolozza della finestra.                                                |
| [**m \_ bNoRealize**](cbasewindow-m-bnorealize.md)                    | Flag che specifica se la finestra deve realizzare la tavolozza.             |
| [**m \_ bBackground**](cbasewindow-m-bbackground.md)                  | Flag che specifica se la tavolozza deve essere una tavolozza di sfondo.        |
| [**m \_ bRealizing**](cbasewindow-m-brealizing.md)                    | Flag che specifica se è in corso la creazione di una nuova tavolozza.                   |
| [**m \_ WindowLock**](cbasewindow-m-windowlock.md)                    | Sezione critica, per serializzare l'accesso all'oggetto .                           |
| [**m \_ bDoGetDC**](cbasewindow-m-bdogetdc.md)                        | Flag che specifica se recuperare il contesto di dispositivo.                    |
| [**m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md)        | Flag che specifica se la finestra pubblica o invia il messaggio di distruzione. |
| Metodi protetti                                                    | Descrizione                                                                    |
| [**OnPaletteChange**](cbasewindow-onpalettechange.md)               | Gestisce i messaggi di modifica della tavolozza. Virtuale.                                      |
| Metodi pubblici                                                       | Descrizione                                                                    |
| [**Finestra CBase**](cbasewindow-cbasewindow.md)                       | Metodo del costruttore.                                                            |
| [**DoneWithWindow**](cbasewindow-donewithwindow.md)                 | Elimina la finestra. Virtuale.                                                  |
| [**PrepareWindow**](cbasewindow-preparewindow.md)                   | Crea la finestra. Virtuale.                                                   |
| [**InactivateWindow**](cbasewindow-inactivatewindow.md)             | Disattiva la finestra. Virtuale.                                               |
| [**ActivateWindow**](cbasewindow-activatewindow.md)                 | Ridimensiona la finestra in base ai requisiti della classe derivata. Virtuale.  |
| [**OnSize**](cbasewindow-onsize.md)                                 | Gestisce i messaggi \_ WM SIZE. Virtuale.                                            |
| [**OnClose**](cbasewindow-onclose.md)                               | Gestisce i messaggi WM \_ CLOSE. Virtuale.                                           |
| [**GetDefaultRect**](cbasewindow-getdefaultrect.md)                 | Recupera le dimensioni predefinite dell'area client. Virtuale.                        |
| [**UninitialiseWindow**](cbasewindow-uninitialisewindow.md)         | Rilascia le risorse della finestra. Virtuale.                                      |
| [**InitialiseWindow**](cbasewindow-initialisewindow.md)             | Inizializza la finestra. Virtuale.                                               |
| [**CompleteConnect**](cbasewindow-completeconnect.md)               | Notifica alla finestra che il pin di input del renderer è stato connesso.          |
| [**DoCreateWindow**](cbasewindow-docreatewindow.md)                 | Crea la finestra.                                                            |
| [**PerformanceAlignWindow**](cbasewindow-performancealignwindow.md) | Allinea la finestra a un limite **DWORD,** per ottenere prestazioni ottimali.            |
| [**DoShowWindow**](cbasewindow-doshowwindow.md)                     | Imposta lo stato di visualizzazione della finestra.                                                  |
| [**PaintWindow**](cbasewindow-paintwindow.md)                       | Determina il ridisegno della finestra.                                             |
| [**DoSetWindowForeground**](cbasewindow-dosetwindowforeground.md)   | Porta la finestra in primo piano.                                           |
| [**SetPalette**](cbasewindow-setpalette.md)                         | Installa un riquadro per la finestra. Virtuale.                                    |
| [**SetRealize**](cbasewindow-setrealize.md)                         | Specifica se la finestra realizza i palette.                                |
| [**DoRealisePalette**](cbasewindow-dorealisepalette.md)             | Realizza il riquadro corrente della finestra. Virtuale.                                |
| [**PossiblyEatMessage**](cbasewindow-possiblyeatmessage.md)         | Consente a una classe derivata di inoltrare messaggi a un'altra finestra. Virtuale.        |
| [**GetWindowWidth**](cbasewindow-getwindowwidth.md)                 | Recupera la larghezza corrente della finestra.                                     |
| [**GetWindowHeight**](cbasewindow-getwindowheight.md)               | Recupera l'altezza corrente della finestra.                                    |
| [**GetWindowHWND**](cbasewindow-getwindowhwnd.md)                   | Recupera un handle per la finestra.                                              |
| [**GetMemoryHDC**](cbasewindow-getmemoryhdc.md)                     | Recupera un handle per il contesto di dispositivo di memoria.                               |
| [**GetWindowHDC**](cbasewindow-getwindowhdc.md)                     | Recupera un handle per il contesto di dispositivo della finestra.                             |
| [**OnReceiveMessage**](cbasewindow-onreceivemessage.md)             | Gestisce i messaggi della finestra. Virtuale.                                              |
| [**UnsetPalette**](cbasewindow-unsetpalette.md)                     | Elimina il riquadro corrente della finestra e ripristina il riquadro di sistema predefinito.  |
| Metodi virtuali puri                                                 | Descrizione                                                                    |
| [**GetClassWindowStyles**](cbasewindow-getclasswindowstyles.md)     | Recupera gli stili di classe della finestra e gli stili della finestra.                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




