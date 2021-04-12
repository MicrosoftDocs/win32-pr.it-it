---
title: Uso del colore in Direct2D
description: Uso del colore in Direct2D
ms.assetid: 74b1f12c-b1de-4df1-85ba-0cf7a0009499
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb195a4ad0bdd9ff32f1123a8a57ff2ce0aadbde
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337062"
---
# <a name="using-color-in-direct2d"></a>Uso del colore in Direct2D

Direct2D utilizza il modello di colore RGB, in cui i colori sono formati combinando valori diversi di rosso, verde e blu. Un quarto componente, alfa, misura la trasparenza di un pixel. In Direct2D ognuno di questi componenti è un valore a virgola mobile con un intervallo di \[ 0,0 1,0 \] . Per i tre componenti colore, il valore misura l'intensità del colore. Per il componente alfa, 0,0 significa completamente trasparente e 1,0 significa completamente opaco. La tabella seguente mostra i colori derivanti da diverse combinazioni di intensità del 100%.



| Red | Green | Blu | Color   |
|-----|-------|------|---------|
| 0   | 0     | 0    | Black   |
| 1   | 0     | 0    | Rosso     |
| 0   | 1     | 0    | Green   |
| 0   | 0     | 1    | Blu    |
| 0   | 1     | 1    | azzurro    |
| 1   | 0     | 1    | Fucsia |
| 1   | 1     | 0    | Giallo  |
| 1   | 1     | 1    | White   |



 

![immagine che mostra i colori RGB.](images/graphics13.png)

I valori dei colori compresi tra 0 e 1 generano diverse sfumature di questi colori puri. Direct2D utilizza la struttura [**d2d1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) per rappresentare i colori. Il codice seguente, ad esempio, specifica il magenta.


```C++
    // Initialize a magenta color.

    D2D1_COLOR_F clr;
    clr.r = 1;
    clr.g = 0;
    clr.b = 1;
    clr.a = 1;  // Opaque.
```



È anche possibile specificare un colore usando la classe [**D2D1:: ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) , che deriva dalla struttura [**d2d1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) .


```C++
    // Equivalent to the previous example.

    D2D1::ColorF clr(1, 0, 1, 1);
```



## <a name="alpha-blending"></a>Fusione alfa

La fusione alfa crea aree traslucidi combinando il colore di primo piano con il colore di sfondo, usando la formula seguente.

<dl> Color = AF * CF + (1-AF) * CB  
</dl>

dove *CB* è il colore di sfondo, *CF* è il colore di primo piano e *AF* è il valore alfa del colore di primo piano. Questa formula viene applicata a coppie a ogni componente colore. Si supponga, ad esempio, che il colore di primo piano sia **(r = 1,0, g = 0,4, b = 0,0)**, con **Alpha = 0,6**, e che il colore di sfondo sia **(r = 0,0, g = 0,5, b = 1,0)**. Il colore alfa Blend risultante è:

R = (1,0 * 0,6 + 0 * 0,4) =. 6   
G = (0,4 * 0,6 + 0,5 * 0,4) =. 44  
B = (0 * 0,6 + 1,0 * 0,4) =. 40  

La figura seguente mostra il risultato di questa operazione di fusione.

![immagine che mostra la fusione alfa.](images/graphics15.png)

## <a name="pixel-formats"></a>Formati pixel

La struttura [**d2d1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) non descrive il modo in cui un pixel viene rappresentato in memoria. Nella maggior parte dei casi non è rilevante. Direct2D gestisce tutti i dettagli interni della conversione delle informazioni sui colori in pixel. Tuttavia, potrebbe essere necessario conoscerne il formato pixel se si utilizza direttamente una bitmap in memoria o se si combina Direct2D con Direct3D o GDI.

L'enumerazione di [**\_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) definisce un elenco di formati pixel. L'elenco è piuttosto lungo, ma solo alcuni di essi sono rilevanti per Direct2D. Gli altri vengono usati da Direct3D.



| Formato pixel                                                                                                                           | Descrizione                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>**\_Formato DXGI \_ B8G8R8A8 \_ UNORM**<br/> | Si tratta del formato pixel più comune. Tutti i componenti pixel (rosso, verde, blu e alfa) sono interi senza segno a 8 bit. I componenti sono disposti nell'ordine *BGRA* in memoria. (Vedere la figura seguente).<br/>                                          |
| <span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>**\_Formato DXGI \_ R8G8B8A8 \_ UNORM**<br/> | I componenti pixel sono interi senza segno a 8 bit nell'ordine *RGBA* . In altre parole, i componenti rosso e blu vengono scambiati rispetto al **formato DXGI \_ \_ B8G8R8A8 \_ UNORM**. Questo formato è supportato solo per i dispositivi hardware.<br/>                             |
| <span id="DXGI_FORMAT_A8_UNORM"></span><span id="dxgi_format_a8_unorm"></span>**\_Formato DXGI \_ a8 \_ UNORM**<br/>                   | Questo formato contiene un componente Alpha a 8 bit, senza componenti RGB. È utile per la creazione di maschere di opacità. Per altre informazioni sull'uso delle maschere di opacità in Direct2D, vedere [Cenni preliminari sulle destinazioni di rendering a8 compatibili](/windows/desktop/Direct2D/compatible-a8-rendertargets).<br/> |



 

Nella figura seguente viene illustrato il layout dei pixel BGRA.

![diagramma che mostra il layout del pixel BGRA.](images/graphics14.png)

Per ottenere il formato pixel di una destinazione di rendering, chiamare [**ID2D1RenderTarget:: GetPixelFormat**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelformat). Il formato pixel potrebbe non corrispondere alla risoluzione dello schermo. Ad esempio, la visualizzazione potrebbe essere impostata su un colore a 16 bit, anche se la destinazione di rendering usa il colore a 32 bit.

### <a name="alpha-mode"></a>Modalità Alpha

Una destinazione di rendering dispone inoltre di una modalità Alpha, che definisce il modo in cui vengono gestiti i valori alfa.



| Modalità Alpha                           | Descrizione                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ Ignora modalità Alpha \_ d2d1**        | Non viene eseguita alcuna fusione alfa. I valori alfa vengono ignorati.                                                                                                                                                                                                                                                                          |
| **D2D1 \_ \_ modalità Alpha \_ lineare**      | Alfa dritto. I componenti dei colori del pixel rappresentano l'intensità del colore prima della fusione alfa.                                                                                                                                                                                                                           |
| **\_Modalità d2d1 \_ alfa \_ premoltiplicata** | Alfa premoltiplicato. I componenti dei colori del pixel rappresentano l'intensità del colore moltiplicata per il valore alfa. Questo formato è più efficiente per eseguire il rendering rispetto alla scala Alpha, perché il termine (AF CF) della formula di fusione alfa è già calcolato. Tuttavia, questo formato non è appropriato per l'archiviazione in un file di immagine. |



 

Di seguito è riportato un esempio della differenza tra Alpha lineare e alfa premoltiplicato. Si supponga che il colore desiderato sia rosso puro (100% di intensità) con 50% Alfa. Come tipo Direct2D, questo colore viene rappresentato come (1, 0, 0, 0,5). Se si usa un Alpha lineare e si presuppongano componenti di colore a 8 bit, il componente rosso del pixel è 0xFF. Utilizzando l'alfa premoltiplicato, il componente rosso viene ridimensionato del 50% in modo da essere uguale a 0x80.

Il tipo di dati [**d2d1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) rappresenta sempre i colori utilizzando l'alfa lineare. Se necessario, Direct2D converte i pixel in formato alfa premoltiplicato.

Se si è certi che il programma non eseguirà alcuna fusione alfa, creare la destinazione di rendering con la modalità **d2d1 \_ Alpha \_ \_ Ignore** la modalità Alpha. Questa modalità può migliorare le prestazioni, perché Direct2D può ignorare i calcoli alfa. Per ulteriori informazioni, vedere [miglioramento delle prestazioni delle applicazioni Direct2D](/windows/desktop/Direct2D/improving-direct2d-performance).

## <a name="next"></a>Prossima

[Applicazione di trasformazioni in Direct2D](applying-transforms-in-direct2d.md)

 

