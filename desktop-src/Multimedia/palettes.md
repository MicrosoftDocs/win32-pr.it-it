---
title: Tavolozze
description: Tavolozze
ms.assetid: ee048f9a-3036-40dc-a6d7-f612b9ef767c
keywords:
- DrawDib, tavolozze
- DrawDibRealize (funzione)
- DrawDibDraw (funzione)
- DrawDibSetPalette (funzione)
- DrawDibGetPalette (funzione)
- DrawDibChangePalette (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5935831d8996c424a386f86082282f9cf7c1c12
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963039"
---
# <a name="palettes"></a>Tavolozze

Le funzioni DrawDib richiedono che un'applicazione risponda a due messaggi orientati alla tavolozza: [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) e [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged). Se l'applicazione non è compatibile con le tavolozze, sarà necessario aggiungere un gestore per ognuno di questi messaggi. Per ulteriori informazioni sull'elaborazione dei messaggi **WM \_ QUERYNEWPALETTE** e **WM \_ PALETTECHANGED** , vedere [aggiunta di gestori di messaggi tavolozza](adding-palette-message-handlers.md).

È possibile realizzare la tavolozza DrawDib corrente per il controller di dominio usando la funzione [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) . È necessario realizzare la tavolozza in risposta al messaggio [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) o [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) oppure quando si prepara la visualizzazione di una sequenza di immagini tramite la funzione [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) .

È possibile creare un'immagine mappata a un'altra tavolozza usando la funzione [**DrawDibSetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) . Questa funzione forza il controller di dominio DrawDib a usare la tavolozza specificata, che può influire sulla qualità dell'immagine. Ad esempio, un'applicazione che è in grado di riconoscere la tavolozza potrebbe avere realizzato una tavolozza ed è necessario impedire a DrawDib di realizzare la propria tavolozza. L'applicazione può usare **DrawDibSetPalette** per notificare a DrawDib la tavolozza da usare.

È possibile ottenere un handle della tavolozza di primo piano corrente usando la funzione [**DrawDibGetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetpalette) . Se l'applicazione usa la tavolozza di primo piano corrente, non ha un utilizzo esclusivo della tavolozza e un'altra applicazione può invalidare l'handle della tavolozza. Quando si termina l'uso, l'applicazione non deve liberare la tavolozza. La possibilità di liberare la tavolozza potrebbe invalidare l'handle della tavolozza per un'altra applicazione.

È possibile preparare DrawDib per ricevere nuovi valori di colore per la tavolozza usando la funzione [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette) . Nel codice seguente **DrawDibChangePalette** vengono assegnati nuovi valori per la tabella dei colori della tavolozza. Se il flag **DDF \_ animate** non è impostato nel controller di dominio DrawDib quando si chiama **DrawDibChangePalette**, è possibile applicare le modifiche della tavolozza usando [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) per realizzare la tavolozza. È quindi possibile usare [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) per ricreare l'immagine. Se nel controller di dominio DrawDib è impostato il flag **DDF \_ animate** , è possibile animare la tavolozza e i colori della bitmap visualizzata utilizzando **DrawDibDraw** o **DrawDibRealize**. È possibile aggiornare il flag **DDF \_ animate** usando le funzioni [**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend) e [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) .

> [!Note]  
> Se si libera la tavolozza DrawDib mentre è selezionata da un controller di dominio, è possibile che venga generato un errore GDI (Graphics Device Interface) quando il controller di dominio usa la tavolozza. Al contrario, l'applicazione deve usare [**DrawDibSetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) per modificare il controller di dominio DrawDib per usare la tavolozza predefinita o un'altra tavolozza.

 

Le funzioni [**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend), [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose)e [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) possono liberare la tavolozza DrawDib. Queste funzioni, tuttavia, devono essere utilizzate solo quando la tavolozza non è stata selezionata dal controller di dominio. La funzione DrawDibDraw può anche liberare la tavolozza quando usa lo stesso controller di dominio DrawDib, ma specifica parametri di disegno diversi (*lpbi*, *dxDst*, *dyDst*, *dxSrc* o *dySrc*) o un formato diverso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering di immagini](image-rendering.md)
</dt> </dl>

 

 