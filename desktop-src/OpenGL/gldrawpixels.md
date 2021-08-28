---
title: Funzione glDrawPixels (Gl.h)
description: La funzione glDrawPixels scrive un blocco di pixel nel framebuffer.
ms.assetid: c4eda64f-a75e-4e6d-984d-af49414b94d8
keywords:
- Funzione glDrawPixels OpenGL
topic_type:
- apiref
api_name:
- glDrawPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832cfadb28d80b57366084297877ffadc1a6238c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480707"
---
# <a name="gldrawpixels-function"></a>Funzione glDrawPixels

La **funzione glDrawPixels** scrive un blocco di pixel nel framebuffer.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glDrawPixels(
         GLsizei width,
         GLsizei height,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*width* 
</dt> <dd>

Dimensione della larghezza del rettangolo in pixel che verrà scritto nel buffer frame.

</dd> <dt>

*height* 
</dt> <dd>

Dimensione dell'altezza del rettangolo in pixel che verrà scritto nel framebuffer.

</dd> <dt>

*format* 
</dt> <dd>

Formato dei dati pixel. Le costanti simboliche accettabili sono le seguenti.




| valore | Significato | 
|-------|---------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl><dt><strong>GL_COLOR_INDEX</strong></dt></dl> | Ogni pixel è un singolo valore, un indice di colore. <br /><ol><li>La <strong>funzione glDrawPixels</strong> converte ogni pixel in formato a virgola fissa, con un numero non specificato di bit a destra del punto binario, indipendentemente dal tipo di dati di memoria. I valori a virgola mobile vengono convertiti in valori a virgola fissa effettivi. La <strong>funzione glDrawPixels</strong> converte i dati di interi con segno e senza segno con tutti i bit frazionari impostati su zero. La funzione converte i dati bitmap in 0.0 o 1.0.</li><li>La <strong>funzione glDrawPixels</strong> sposta ogni indice a virgola fissa a sinistra di GL_INDEX_SHIFT bit e lo aggiunge a GL_INDEX_OFFSET. Se GL_INDEX_SHIFT è negativo, lo spostamento è a destra. In entrambi i casi, zero bit riempiono le posizioni di bit altrimenti non specificata nel risultato.</li><li>In modalità RGBA, <strong>glDrawPixels</strong> converte l'indice risultante in un pixel RGBA usando le tabelle GL_PIXEL_MAP_I_TO_R, GL_PIXEL_MAP_I_TO_G, GL_PIXEL_MAP_I_TO_B e GL_PIXEL_MAP_I_TO_A. Quando è in modalità color-index e GL_MAP_COLOR è true, l'indice viene sostituito con il valore a cui <strong>glDrawPixels</strong> fa riferimento nella tabella di GL_PIXEL_MAP_I_TO_I.</li><li>Indipendentemente dal fatto che la sostituzione di ricerca dell'indice sia stata eseguita o meno, la parte intera dell'indice è <strong>AND</strong>con 2<sup>b</sup> - 1, dove <em>b</em> è il numero di bit in un index buffer.</li><li>Gli indici o i colori RGBA risultanti vengono quindi convertiti in frammenti collegando la coordinata <em>z</em>della posizione raster corrente e le coordinate della trama a ogni pixel e quindi assegnando le coordinate delle finestre <em>x</em> e <em>y</em> al <em>frammento n</em>in modo che <em>x</em>? = <em>x</em><sub>r</sub>  +  <em>n</em> mod <em>width</em><br /><em>y</em>? = <em>y</em><sub>r</sub>  +  <em>n/width</em><br /> dove (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) è la posizione raster corrente.<br /></li><li>La <strong>funzione glDrawPixels</strong> considera questi frammenti di pixel esattamente come i frammenti generati dall'rasterizzazione di punti, linee o poligoni. Applica il mapping delle trame, il riempimento e tutte le operazioni sui frammenti prima di scrivere i frammenti nel framebuffer.</li></ol> | 
| <span id="GL_STENCIL_INDEX"></span><span id="gl_stencil_index"></span><dl><dt><strong>GL_STENCIL_INDEX</strong></dt></dl> | Ogni pixel è un singolo valore, un indice stencil. <br /><ol><li>La <strong>funzione glDrawPixels</strong> la converte in formato a virgola fissa, con un numero non specificato di bit a destra del punto binario, indipendentemente dal tipo di dati di memoria. I valori a virgola mobile vengono convertiti in valori a virgola fissa effettivi. La <strong>funzione glDrawPixels</strong> converte i dati di interi con segno e senza segno con tutti i bit frazionari impostati su zero. I dati bitmap vengono convertiti in 0.0 o 1.0.</li><li>La <strong>funzione glDrawPixels</strong> sposta ogni indice a virgola fissa a sinistra di GL_INDEX_SHIFT bit e lo aggiunge a GL_INDEX_OFFSET. Se GL_INDEX_SHIFT è negativo, lo spostamento è a destra. In entrambi i casi, zero bit riempiono le posizioni di bit altrimenti non specificata nel risultato.</li><li>Se GL_MAP_STENCIL è true, l'indice viene sostituito con il valore a cui <strong>glDrawPixels</strong> fa riferimento nella tabella di GL_PIXEL_MAP_S_TO_S.</li><li>Indipendentemente dal fatto che la sostituzione di ricerca dell'indice sia eseguita o meno, la parte intera dell'indice è <strong>quindi AND</strong>con 2<sup>b</sup> - 1, dove <em>b</em> è il numero di bit nel buffer degli stencil. Gli indici degli stencil risultanti vengono quindi <em></em>scritti nel buffer degli stencil in modo che l'eesimo indice sia scritto nella posizione <em>x</em>? = <em>x</em><sub>r</sub>  +  <em>n</em> mod <em>width</em><br /><em>y</em>? = <em>y</em><sub>r</sub>  +  <em>n/width</em><br /> dove (<em>x</em><sub>r</sub> , <em></em> y<sub>r</sub> ) è la posizione raster corrente. Solo il test di proprietà dei pixel, il test di scissor e la writemask degli stencil influiscono su queste scritture.<br /></li></ol> | 
| <span id="GL_DEPTH_COMPONENT"></span><span id="gl_depth_component"></span><dl><dt><strong>GL_DEPTH_COMPONENT</strong></dt></dl> | Ogni pixel è un componente a profondità singola. <br /><ol><li>La <strong>funzione glDrawPixels</strong> converte i dati a virgola mobile direttamente in un formato a virgola mobile interno con precisione non specificata. I dati di tipo Signed Integer vengono mappati in modo lineare al formato a virgola mobile interno in modo che il valore integer rappresentabile più positivo sia mappato a 1,0 e che il valore rappresentabile più negativo sia -1,0. Il mapping dei dati di un intero senza segno viene eseguito in modo analogo: il valore intero più grande viene mappato a 1,0 e zero esegue il mapping a 0,0.</li><li>La <strong>funzione glDrawPixels</strong> moltiplica il valore di profondità a virgola mobile risultante per GL_DEPTH_SCALE e lo aggiunge a GL_DEPTH_BIAS. Il risultato viene definito in base all'intervallo [0,1].</li><li>La <strong>funzione glDrawPixels</strong> converte i componenti di profondità risultanti in frammenti collegando il colore della posizione raster corrente o le coordinate di indice e trama a ogni pixel e assegnando le coordinate delle finestre <em>x</em> e <em>y</em> al <em>frammento n</em> in modo che <em>x</em>? = <em></em>x<sub>r</sub>  +  <em>n</em> mod <em>width</em><br /><em>y</em>? = <em>y</em><sub>r</sub>  +  <em>n/width</em><br /> dove ( <em></em> x<sub>r</sub> ,<em>y</em><sub>r</sub> ) è la posizione raster corrente.<br /></li><li>Questi frammenti di pixel vengono quindi trattati esattamente come i frammenti generati dall'rasterizzazione di punti, linee o poligoni. La <strong>funzione glDrawPixels</strong> applica il mapping delle trame, il riempimento e tutte le operazioni di frammento prima di scrivere i frammenti nel framebuffer.</li></ol> | 
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl><dt><strong>GL_RGBA</strong></dt></dl> | Ogni pixel è un gruppo di quattro componenti in questo ordine: rosso, verde, blu, alfa. <br /><ol><li>La <strong>funzione glDrawPixels</strong> converte i valori a virgola mobile direttamente in un formato a virgola mobile interno con precisione non specificata. I valori interi con segno vengono mappati in modo lineare al formato a virgola mobile interno in modo che il valore intero rappresentabile più positivo sia mappato a 1,0 e il valore rappresentabile più negativo a -1,0. Il mapping dei dati di un intero senza segno viene eseguito in modo analogo: il valore intero più grande viene mappato a 1,0 e zero esegue il mapping a 0,0.</li><li>La <strong>funzione glDrawPixels</strong> moltiplica i valori di colore a virgola mobile risultanti per GL_c_SCALE e li aggiunge a GL_c_BIAS, dove <em>c</em> è RED, GREEN, BLUE e ALPHA per i rispettivi componenti di colore. I risultati vengono definiti nell'intervallo [0,1].</li><li>Se GL_MAP_COLOR è true, <strong>glDrawPixels</strong> ridimensiona ogni componente colore in base alle dimensioni della tabella di ricerca GL_PIXEL_MAP_c_TO_c e quindi sostituisce il componente con il valore a cui fa riferimento nella tabella; <em>c</em> è rispettivamente R, G, B o A.</li><li>La <strong>funzione glDrawPixels</strong> converte i colori RGBA risultanti in frammenti collegando le coordinate z <em>della</em>posizione raster corrente e della trama a ogni pixel, quindi assegnando le coordinate delle finestre <em>x</em> e <em>y</em> al <em>frammento n</em>in modo che <em>x</em>? = <em>x</em><sub>r</sub>  +  <em>n</em> mod <em>width</em><br /><em>y</em>? = <em>y</em><sub>r</sub>  +  <em>n /width</em><br /> dove (<em>x</em><sub>r</sub> ,<em>y</em><sub>r</sub> ) è la posizione raster corrente.<br /></li><li>Questi frammenti di pixel vengono quindi trattati esattamente come i frammenti generati dall'rasterizzazione di punti, linee o poligoni. La <strong>funzione glDrawPixels</strong> applica il mapping delle trame, il riempimento e tutte le operazioni di frammento prima di scrivere i frammenti nel framebuffer.</li></ol> | 
| <span id="GL_RED"></span><span id="gl_red"></span><dl><dt><strong>GL_RED</strong></dt></dl> | Ogni pixel è un singolo componente rosso.<br /> La <strong>funzione glDrawPixels</strong> converte questo componente nel formato a virgola mobile interno allo stesso modo del componente rosso di un pixel RGBA, quindi lo converte in un pixel RGBA con verde e blu impostati su 0,0 e alfa impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.<br /> | 
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl><dt><strong>GL_GREEN</strong></dt></dl> | Ogni pixel è un singolo componente verde.<br /> La <strong>funzione glDrawPixels</strong> converte questo componente nel formato a virgola mobile interno allo stesso modo del componente verde di un pixel RGBA, quindi lo converte in un pixel RGBA con rosso e blu impostati su 0,0 e alfa impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.<br /> | 
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl><dt><strong>GL_BLUE</strong></dt></dl> | Ogni pixel è un singolo componente blu.<br /> La funzione <strong>glDrawPixels</strong> converte questo componente nel formato a virgola mobile interno allo stesso modo del componente blu di un pixel RGBA e quindi lo converte in un pixel RGBA con rosso e verde impostati su 0,0 e alfa impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.<br /> | 
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl><dt><strong>GL_ALPHA</strong></dt></dl> | Ogni pixel è un singolo componente alfa.<br /> La <strong>funzione glDrawPixels</strong> converte questo componente nel formato a virgola mobile interno allo stesso modo del componente alfa di un pixel RGBA e quindi lo converte in un pixel RGBA con rosso, verde e blu impostato su 0,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.<br /> | 
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl><dt><strong>GL_RGB</strong></dt></dl> | Ogni pixel è un gruppo di tre componenti in questo ordine: rosso, verde, blu. La <strong>funzione glDrawPixels</strong> converte ogni componente nel formato a virgola mobile interno nello stesso modo dei componenti rosso, verde e blu di un pixel RGBA. La tripla di colore viene convertita in un pixel RGBA con alfa impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come un pixel RGBA.<br /> | 
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl><dt><strong>GL_LUMINANCE</strong></dt></dl> | Ogni pixel è un singolo componente di luminance.<br /> La funzione <strong>glDrawPixels</strong> converte questo componente nel formato a virgola mobile interno nello stesso modo del componente rosso di un pixel RGBA e quindi lo converte in un pixel RGBA con rosso, verde e blu impostato sul valore di luminance convertito e alfa impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come un pixel RGBA.<br /> | 
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl><dt><strong>GL_LUMINANCE_ALPHA</strong></dt></dl> | Ogni pixel è un gruppo di due componenti nell'ordine seguente: luminance, alpha.<br /> La funzione <strong>glDrawPixels</strong> converte i due componenti nel formato a virgola mobile interno nello stesso modo del componente rosso di un pixel RGBA, quindi li converte in un pixel RGBA con rosso, verde e blu impostati sul valore di luminance convertito e alfa impostato sul valore alfa convertito. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come un pixel RGBA.<br /> | 
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl><dt><strong>GL_BGR_EXT</strong></dt></dl> | Ogni pixel è un gruppo di tre componenti nell'ordine seguente: blu, verde, rosso.<br /> GL_BGR_EXT un formato che corrisponde al layout di memoria Windows bitmap indipendenti dal dispositivo (DIB). Di conseguenza, le applicazioni possono usare gli stessi dati con Windows di funzione e chiamate di funzione pixel OpenGL.<br /> | 
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl><dt><strong>GL_BGRA_EXT</strong></dt></dl> | Ogni pixel è un gruppo di quattro componenti nell'ordine seguente: blu, verde, rosso, alfa.<br /> GL_BGRA_EXT un formato che corrisponde al layout di memoria Windows bitmap indipendenti dal dispositivo (DIB). Di conseguenza, le applicazioni possono usare gli stessi dati con Windows di funzione e chiamate di funzione pixel OpenGL.<br /> | 




 

</dd> <dt>

*type* 
</dt> <dd>

Tipo di dati per *i pixel.* Di seguito sono riportate le costanti simboliche accettate e i relativi significati.



| valore                                                                                                                                                                      | Significato                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**GL \_ UNSIGNED \_ BYTE**</dt> </dl>    | Intero senza segno a 8 bit<br/>                 |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**GL \_ BYTE**</dt> </dl>                                | Valore intero con segno a 8 bit<br/>                   |
| <span id="GL_BITMAP"></span><span id="gl_bitmap"></span><dl> <dt>**GL \_ BITMAP**</dt> </dl>                          | Bit singoli in interi senza segno a 8 bit<br/> |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**GL \_ UNSIGNED \_ SHORT**</dt> </dl> | Intero senza segno a 16 bit<br/>                |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**GL \_ SHORT**</dt> </dl>                             | Valore intero a 16 bit con segno<br/>                  |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL \_ UNSIGNED \_ INT**</dt> </dl>       | Intero senza segno a 32 bit<br/>                |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ INT**</dt> </dl>                                   | Intero a 32 bit<br/>                         |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ FLOAT**</dt> </dl>                             | Virgola mobile a precisione singola<br/>        |



 

</dd> <dt>

*Pixel* 
</dt> <dd>

Puntatore ai dati pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | La *larghezza o* *l'altezza* erano negative.<br/>                                                                                                                                          |
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | Il *formato o* il *tipo* non è un valore accettato. <br/>                                                                                                                             |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | *format* era GL \_ RED, GL \_ GREEN, GL \_ BLUE, GL \_ ALPHA, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ EXT, GL \_ BGRA \_ EXT, \_ GL LUMINANCE o GL LUMINANCE ALPHA e OpenGL era in modalità \_ \_ color-index.<br/> |
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *il tipo* era GL \_ BITMAP e il *formato* non era GL COLOR INDEX o GL \_ STENCIL \_ \_ \_ INDEX.<br/>                                                                                         |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | *il formato* era GL \_ STENCIL INDEX e non \_ esisteva alcun buffer di stencil.<br/>                                                                                                                  |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>                                                        |


## <a name="remarks"></a>Commenti

La **funzione glDrawPixels** legge i dati pixel dalla memoria e li scrive nel framebuffer rispetto alla posizione raster corrente. Usare [**glRasterPos per**](glrasterpos-functions.md) impostare la posizione raster corrente e [**usare glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con l'argomento GL CURRENT RASTER POSITION per \_ eseguire query sulla posizione \_ \_ raster.

Diversi parametri definiscono la codifica dei dati pixel in memoria e controllano l'elaborazione dei dati pixel prima di essere inseriti nel framebuffer. Questi parametri vengono impostati con quattro funzioni: [**glPixelStore**](glpixelstore-functions.md), [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md)e [**glPixelZoom**](glpixelzoom.md). Questo argomento descrive gli effetti su **glDrawPixels** di molti, ma non tutti, dei parametri specificati da queste quattro funzioni.

I dati  vengono letti dai pixel come sequenza di byte con o senza segno, short con o senza segno, interi con o senza segno o valori a virgola mobile e precisione singola, a seconda del tipo *.* Ognuno di questi byte, short, numeri interi o valori a virgola mobile viene interpretato come un componente di colore o profondità o un indice, a seconda del *formato*. Gli indici vengono sempre trattati singolarmente. I componenti di colore vengono considerati gruppi di uno, due, tre o quattro valori, sempre in base al *formato*. Sia i singoli indici che i gruppi di componenti vengono definiti pixel. Se *il tipo* è GL BITMAP, i dati devono essere byte senza segno e il formato deve essere GL COLOR INDEX o GL STENCIL \_  \_ \_ \_ \_ INDEX. Ogni byte senza segno viene considerato come otto pixel a 1 bit, con l'ordinamento dei bit determinato da GL \_ UNPACK \_ LSB \_ FIRST (vedere [**glPixelStore**](glpixelstore-functions.md)).

La *larghezza per* pixel di *altezza* viene letta dalla memoria, a partire dai pixel *di posizione.* Per impostazione predefinita, questi pixel vengono presi da  posizioni di memoria adiacenti, ad eccezione del fatto che dopo la lettura di tutti i pixel di larghezza, il puntatore di lettura viene avanzato al limite successivo di 4 byte. La **funzione glPixelStore** specifica l'allineamento di riga a 4 byte con l'argomento GL UNPACK ALIGNMENT ed è possibile \_ \_ impostarla su 1, 2, 4 o 8 byte. Altri parametri dell'archivio pixel specificano miglioramenti diversi del puntatore di lettura, sia prima della lettura del primo pixel che dopo la lettura di tutti *i* pixel di larghezza. La **funzione glPixelStore** opera su  ognuno dei pixel di larghezza per altezza letti dalla memoria nello stesso modo, in base ai valori di diversi parametri specificati da [**glPixelTransfer**](glpixeltransfer.md) e [**glPixelMap**](glpixelmap.md). I dettagli di queste operazioni, nonché il buffer di destinazione in cui vengono disegnati i pixel, sono specifici del formato dei pixel, come specificato dal *formato*.

La rasterizzazione descritta finora presuppone fattori di zoom pixel di 1,0. Se si usa [**glPixelZoom**](glpixelzoom.md) per modificare i fattori di zoom dei pixel *x* *e y,* i pixel vengono convertiti in frammenti come indicato di seguito. Se (*xr,yr*) è la posizione raster corrente e un pixel specificato si trova *nell'esima* colonna e m esima riga del rettangolo pixel, vengono generati frammenti per i pixel i cui centri si trova nel rettangolo con angoli in

(*x*<sub>r</sub>  +  *zoom*? *n*, *y*<sub>r</sub>  +  *zoom*<sub>y</sub> *m*)

(*x*<sub>r</sub>  +  *zoom*? (*n* + 1), *y*<sub>r</sub>  +  *zoom*<sub>y</sub> (*m* + 1))

dove *zoom*? è il valore di GL \_ ZOOM X e \_ *zoom*<sub>y</sub> è il valore di GL \_ ZOOM \_ Y.

Le funzioni seguenti recuperano informazioni correlate a **glDrawPixels**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ CURRENT \_ RASTER \_ POSITION

**glGet con** argomento GL \_ CURRENT \_ RASTER POSITION \_ \_ VALID

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPixelZoom**](glpixelzoom.md)
</dt> <dt>

[**glRasterPos**](glrasterpos-functions.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





