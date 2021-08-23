---
title: Uso del colore in Direct2D
description: Uso del colore in Direct2D
ms.assetid: 74b1f12c-b1de-4df1-85ba-0cf7a0009499
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe6ded6d181ebcbca402161fe6af0b8fb8dd65f7d082632474136a9bd1ff551
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631536"
---
# <a name="using-color-in-direct2d"></a>Uso del colore in Direct2D

Direct2D usa il modello di colore RGB, in cui i colori vengono formati combinando valori diversi di rosso, verde e blu. Un quarto componente, alfa, misura la trasparenza di un pixel. In Direct2D ognuno di questi componenti è un valore a virgola mobile con un intervallo \[ di 0,0 1,0. \] Per i tre componenti di colore, il valore misura l'intensità del colore. Per il componente alfa, 0,0 significa completamente trasparente e 1,0 significa completamente opaco. La tabella seguente illustra i colori risultanti da varie combinazioni di intensità del 100%.



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



 

![immagine che mostra i colori rgb.](images/graphics13.png)

I valori dei colori compresi tra 0 e 1 comportano sfumature diverse di questi colori puri. Direct2D usa la [**struttura COLOR \_ \_ F D2D1**](/windows/desktop/Direct2D/d2d1-color-f) per rappresentare i colori. Ad esempio, il codice seguente specifica magenta.


```C++
    // Initialize a magenta color.

    D2D1_COLOR_F clr;
    clr.r = 1;
    clr.g = 0;
    clr.b = 1;
    clr.a = 1;  // Opaque.
```



È anche possibile specificare un colore usando la [**classe D2D1::ColorF,**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) che deriva dalla [**struttura COLOR \_ \_ F D2D1.**](/windows/desktop/Direct2D/d2d1-color-f)


```C++
    // Equivalent to the previous example.

    D2D1::ColorF clr(1, 0, 1, 1);
```



## <a name="alpha-blending"></a>Fusione alfa

La fusione alfa crea aree traslucidi combinando il colore di primo piano con il colore di sfondo, usando la formula seguente.

<dl> color = af * Cf + (1 - af) * Cb  
</dl>

dove *Cb* è il colore di sfondo, *Cf* è il colore di primo piano e *af* è il valore alfa del colore di primo piano. Questa formula viene applicata pairwise a ogni componente del colore. Si supponga, ad esempio, che il colore di primo piano sia **(R = 1,0, G = 0,4, B = 0,0)**, con **alfa = 0,6** e che il colore di sfondo sia **(R = 0,0, G = 0,5, B = 1,0)**. Il colore con alpha blended risultante è:

R = (1,0 * 0,6 + 0 * 0,4) = .6   
G = (0,4 * 0,6 + 0,5 * 0,4) = .44  
B = (0 * 0,6 + 1,0 * 0,4) = .40  

L'immagine seguente mostra il risultato di questa operazione di fusione.

![immagine che mostra la fusione alfa.](images/graphics15.png)

## <a name="pixel-formats"></a>Formati pixel

La [**struttura COLOR \_ \_ F D2D1**](/windows/desktop/Direct2D/d2d1-color-f) non descrive il modo in cui un pixel viene rappresentato in memoria. Nella maggior parte dei casi, questo non è importante. Direct2D gestisce tutti i dettagli interni della traduzione delle informazioni sui colori in pixel. Potrebbe tuttavia essere necessario conoscere il formato pixel se si lavora direttamente con una bitmap in memoria o se si combina Direct2D con Direct3D o GDI.

[**L'enumerazione DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) definisce un elenco di formati di pixel. L'elenco è piuttosto lungo, ma solo alcuni di essi sono rilevanti per Direct2D. Gli altri vengono usati da Direct3D.



| Formato pixel                                                                                                                           | Descrizione                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>**FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM**<br/> | Si tratta del formato pixel più comune. Tutti i componenti pixel (rosso, verde, blu e alfa) sono interi senza segno a 8 bit. I componenti vengono disposti in *ordine BGRA* in memoria. Vedere la figura seguente.<br/>                                          |
| <span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>**FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM**<br/> | I componenti pixel sono interi senza segno a 8 bit, in *ordine RGBA.* In altre parole, i componenti rosso e blu vengono scambiati rispetto a **DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM.** Questo formato è supportato solo per i dispositivi hardware.<br/>                             |
| <span id="DXGI_FORMAT_A8_UNORM"></span><span id="dxgi_format_a8_unorm"></span>**FORMATO DXGI \_ \_ A8 \_ UNORM**<br/>                   | Questo formato contiene un componente alfa a 8 bit, senza componenti RGB. È utile per la creazione di maschere di opacità. Per altre informazioni sull'uso delle maschere di opacità in Direct2D, vedere [Cenni preliminari sulle destinazioni di rendering A8 compatibili.](/windows/desktop/Direct2D/compatible-a8-rendertargets)<br/> |



 

La figura seguente mostra il layout in pixel BGRA.

![diagramma che mostra il layout bgra pixel.](images/graphics14.png)

Per ottenere il formato pixel di una destinazione di rendering, chiamare [**ID2D1RenderTarget::GetPixelFormat**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelformat). Il formato pixel potrebbe non corrispondere alla risoluzione dello schermo. Ad esempio, la visualizzazione potrebbe essere impostata su un colore a 16 bit, anche se la destinazione di rendering usa il colore a 32 bit.

### <a name="alpha-mode"></a>Modalità alfa

Una destinazione di rendering ha anche una modalità alfa, che definisce la modalità di trattamento dei valori alfa.



| Modalità alfa                           | Descrizione                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MODALITÀ ALFA D2D1 \_ \_ \_ IGNORE**        | Non viene eseguita alcuna fusione alfa. I valori alfa vengono ignorati.                                                                                                                                                                                                                                                                          |
| **D2D1 \_ ALPHA \_ MODE \_ STRAIGHT**      | Alfa diritta. I componenti di colore del pixel rappresentano l'intensità del colore prima della fusione alfa.                                                                                                                                                                                                                           |
| **\_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_** | Alfa premoltilied. I componenti di colore del pixel rappresentano l'intensità del colore moltiplicata per il valore alfa. Questo formato è più efficiente per il rendering rispetto al valore alfa diritto, perché il termine (af Cf) della formula di fusione alfa è pre-calcolato. Tuttavia, questo formato non è appropriato per l'archiviazione in un file di immagine. |



 

Di seguito è riportato un esempio della differenza tra alfa diritto e alfa premoltilied. Si supponga che il colore desiderato sia rosso puro (intensità 100%) con 50% alfa. Come tipo Direct2D, questo colore viene rappresentato come (1, 0, 0, 0,5). Usando l'alfa diritto e presupponendo componenti a colori a 8 bit, il componente rosso del pixel viene 0xFF. Usando il valore alfa premoltilied, il componente rosso viene ridimensionato del 50% in modo che sia uguale 0x80.

Il [**tipo di dati D2D1 COLOR \_ \_ F**](/windows/desktop/Direct2D/d2d1-color-f) rappresenta sempre i colori usando alfa diritto. Direct2D converte i pixel nel formato alfa premoltilied, se necessario.

Se si sa che il programma non eseguirà alcuna fusione alfa, creare la destinazione di rendering con la modalità alfa **D2D1 \_ ALPHA \_ MODE \_ IGNORE.** Questa modalità può migliorare le prestazioni, perché Direct2D può ignorare i calcoli alfa. Per altre informazioni, vedere [Miglioramento delle prestazioni delle applicazioni Direct2D.](/windows/desktop/Direct2D/improving-direct2d-performance)

## <a name="next"></a>Prossima

[Applicazione di trasformazioni in Direct2D](applying-transforms-in-direct2d.md)

 

