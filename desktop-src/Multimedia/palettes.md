---
title: Tavolozze
description: Tavolozze
ms.assetid: ee048f9a-3036-40dc-a6d7-f612b9ef767c
keywords:
- DrawDib, tavolozze
- Funzione DrawDibRealize
- Funzione DrawDibDraw
- Funzione DrawDibSetPalette
- Funzione DrawDibGetPalette
- Funzione DrawDibChangePalette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db474a9e983c442f21fd479342ac8b0786719f36f1494e307154c6cc0a0bd50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893021"
---
# <a name="palettes"></a>Tavolozze

Le funzioni DrawDib richiedono che un'applicazione risponda a due messaggi orientati al riquadro: [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) e [**WM \_ PALETTECHANGED.**](/windows/desktop/gdi/wm-palettechanged) Se l'applicazione non supporta il riquadro, è necessario aggiungere un gestore per ognuno di questi messaggi. Per altre informazioni sull'elaborazione dei **messaggi WM \_ QUERYNEWPALETTE** e **WM \_ PALETTECHANGED,** vedere [Aggiunta di gestori](adding-palette-message-handlers.md)di messaggi del riquadro .

È possibile realizzare la tavolozza DrawDib corrente nel controller di dominio usando la [**funzione DrawDibRealize.**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) La tavolozza deve essere visualizzata in risposta al messaggio [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) o [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) oppure quando si prepara la visualizzazione di una sequenza di immagini tramite la [**funzione DrawDibDraw.**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw)

È possibile disegnare un'immagine mappata a un'altra tavolozza usando la [**funzione DrawDibSetPalette.**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) Questa funzione forza il controller di dominio DrawDib a usare la tavolozza specificata, che può influire sulla qualità dell'immagine. Ad esempio, un'applicazione che è in grado di riconoscere la tavolozza potrebbe aver realizzato una tavolozza e deve impedire a DrawDib di realizzare la propria tavolozza. L'applicazione può usare **DrawDibSetPalette** per inviare una notifica a DrawDib del riquadro da usare.

È possibile ottenere un handle del riquadro di primo piano corrente usando la [**funzione DrawDibGetPalette.**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetpalette) Se l'applicazione usa il riquadro di primo piano corrente, non ha l'uso esclusivo del riquadro e un'altra applicazione può invalidare l'handle della tavolozza. L'applicazione non deve liberare il riquadro al termine dell'uso. La liberazione del riquadro potrebbe invalidare l'handle del riquadro per un'altra applicazione.

È possibile preparare DrawDib per ricevere nuovi valori di colore per la tavolozza usando la [**funzione DrawDibChangePalette.**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette) Nel codice seguente **DrawDibChangePalette** si assegnano nuovi valori per la tabella dei colori della tavolozza. Se il flag **DDF \_ ANIMATE** non è impostato nel controller di dominio DrawDib quando si chiama **DrawDibChangePalette,** è possibile applicare le modifiche al riquadro usando [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) per realizzare il riquadro. È quindi possibile usare [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) per ridisegnare l'immagine. Se il flag **DDF \_ ANIMATE** è impostato nel controller di dominio DrawDib, è possibile animare la tavolozza e i colori della bitmap visualizzata usando **DrawDibDraw** o **DrawDibRealize**. È possibile aggiornare il flag **DDF \_ ANIMATE** usando le [**funzioni DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend) [**e DrawDibBegin.**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)

> [!Note]  
> Se si libera la tavolozza DrawDib mentre è selezionata da un controller di dominio, un errore GDI (Graphics Device Interface) può verificarsi quando il controller di dominio usa la tavolozza. L'applicazione deve invece usare [**DrawDibSetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) per modificare il controller di dominio DrawDib in modo da usare il riquadro predefinito o un'altra tavolozza.

 

Le [**funzioni DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend), [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose)e [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) possono liberare la tavolozza DrawDib. Tuttavia, queste funzioni devono essere usate solo quando il riquadro non è stato selezionato dal controller di dominio. La funzione DrawDibDraw può anche liberare la tavolozza quando usa lo stesso controller di dominio DrawDib, ma specifica parametri di disegno diversi (*lpbi,* *dxDst,* *dyDst,* *dxSrc* o *dySrc*) o un formato diverso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering delle immagini](image-rendering.md)
</dt> </dl>

 

 