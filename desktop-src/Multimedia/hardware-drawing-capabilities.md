---
title: Funzionalità di disegno hardware
description: Funzionalità di disegno hardware
ms.assetid: 3a26de73-cb9e-41a0-8c33-a7cca7d6058e
keywords:
- Gestione compressione video (VCM), disegno
- VCM (Video Compression Manager), disegno
- ICGetInfo (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba7d3af8beb7c4ac676e421fe10d427322470d14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044815"
---
# <a name="hardware-drawing-capabilities"></a>Funzionalità di disegno hardware

Alcuni renderer possono disegnare direttamente su hardware video quando decomprimeno i fotogrammi video. Questi renderer restituiscono il \_ flag di traccia VIDCF in risposta alla funzione [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) . Quando si usa questo tipo di renderer, l'applicazione non deve gestire i dati decompressi. Consente al renderer di conservare i dati decompressi per il disegno.

Se l'applicazione utilizza un renderer con funzionalità di disegno, deve gestire le attività seguenti:

-   Selezionare un renderer.
-   Specificare i formati di immagine.
-   Inizializzare il renderer.
-   Creare i dati.
-   Parametri di disegno del controllo.

## <a name="renderer-selection"></a>Selezione renderer

La macro [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) apre un renderer che può creare immagini con il formato specificato. Restituisce un handle di un renderer se ha esito positivo oppure zero in caso contrario. Questa macro usa la funzione [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) per aprire il renderer.

## <a name="specifying-image-formats"></a>Specifica di formati di immagine

Poiché non è necessario che l'applicazione disegni i dati decompressi, non richiede un formato di output specifico. Tuttavia, deve verificare che il renderer possa creare usando il formato di input usando il messaggio di [**\_ \_ query di estrazione ICM**](icm-draw-query.md) (oppure usare la macro [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) ). Questo messaggio non può determinare se un renderer può creare una bitmap. Se l'applicazione deve determinare se il renderer è in grado di creare la bitmap, utilizzare questo messaggio con la funzione [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) .

L'applicazione può avere un renderer che suggerisce un formato di input tramite la funzione [**ICDrawSuggestFormat**](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat) . Questa funzione viene utilizzata quando un renderer separa le funzionalità di disegno dalle funzionalità di decompressione. La maggior parte delle applicazioni che utilizzano le funzioni di disegno non dovrà determinare il formato di output.

## <a name="renderer-initialization"></a>Inizializzazione del renderer

La funzione [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) Inizializza un renderer e ne indica la destinazione del disegno. Questa funzione può inoltre eseguire le attività seguenti:

-   Determinare se il renderer supporta un formato di input specifico.
-   Consente di specificare se l'operazione di disegno occupa una finestra o l'intera schermata.
-   Consente di specificare la parte dell'immagine da visualizzare utilizzando il rettangolo di origine.
-   Definire la velocità di riproduzione della sequenza di immagini.

Alcuni renderer memorizzano nel buffer i dati compressi per operare in modo più efficiente. L'applicazione può inviare il [**messaggio \_ GETBUFFERSWANTED MCI**](icm-getbufferswanted.md) (oppure usare la macro [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) ) per determinare il numero di buffer richiesti dal renderer. L'applicazione deve precaricare questi buffer e inviarli al renderer prima del disegno.

## <a name="drawing-the-data"></a>Disegno dei dati

È possibile utilizzare la funzione [**ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) per decomprimere i dati per il disegno. Il renderer, tuttavia, non avvia il disegno dei dati fino a quando l'applicazione non invia il messaggio di [**\_ \_ avvio di disegno ICM**](icm-draw-start.md) (o usa la macro [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) ). Quando l'applicazione chiama questa funzione, il renderer inizia a creare i frame alla velocità specificata dal parametro *dwRate* diviso per il parametro *dwScale* . questi parametri sono stati specificati quando l'applicazione ha inizializzato il renderer tramite la funzione [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) . Il disegno continua fino a quando l'applicazione non invia il messaggio di [**\_ \_ arresto di disegno ICM**](icm-draw-stop.md) (o usa la macro [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) ).

> [!Note]  
> Se un renderer memorizza nel buffer i dati prima del disegno, l'applicazione non deve usare la macro **ICDrawStart** fino a quando non ha inviato il numero di frame restituiti dal renderer per la macro **ICGetBuffersWanted** .

 

Il parametro *ltime* di [**ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) specifica l'ora in cui creare un frame. Il renderer divide questo Integer per la scala temporale specificata con [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) per ottenere il tempo effettivo. I tempi per le funzioni **ICDraw** sono relativi a **ICDrawStart**. **ICDrawStart** imposta l'orologio su zero. Se, ad esempio, l'applicazione specifica 1000 per la scala temporale e 75 per *ltime*, il renderer disegna il frame 75 millisecondi nella sequenza.

## <a name="controlling-drawing-parameters"></a>Controllo dei parametri di disegno

È possibile monitorare l'orologio di un renderer inviando il messaggio di [**\_ \_ tempo di richiamo di ICM**](icm-draw-gettime.md) (o usare la macro [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) ) ed è possibile impostare l'orologio di un renderer che può creare dati inviando il messaggio di [**\_ \_ tempo**](icm-draw-settime.md) di indicizzazione ICM (o usare la macro [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) ).

Per modificare la posizione corrente durante il disegno di un renderer, l'applicazione può inviare il messaggio della [**\_ \_ finestra di disegno ICM**](icm-draw-window.md) (o usare la macro [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) ) per riposizionare la finestra. Le applicazioni in genere usano questo messaggio ogni volta che viene modificata la finestra.

Se la finestra di riproduzione ottiene un messaggio della tavolozza di realizzo, l'applicazione deve inviare il messaggio di [**\_ progetto \_ MCI**](icm-draw-realize.md) (o usare la macro [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) ) per fare in modo che il renderer realizzi nuovamente la tavolozza per la riproduzione. Le applicazioni possono modificare la tavolozza inviando il messaggio di [**\_ \_ CHANGEPALETTE**](icm-draw-changepalette.md) (o usare la macro [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) ) e ottenere la tavolozza corrente inviando il messaggio per la [**\_ \_ \_ tavolozza di estrazione di ICM**](icm-draw-get-palette.md) .

Per alcuni renderer è necessario indicare in modo specifico di visualizzare i frame passati. Se si invia il messaggio [**\_ \_ RENDERBUFFER**](icm-draw-renderbuffer.md) (o si usa la macro [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) ), i renderer devono disegnare il frame.

 

 




