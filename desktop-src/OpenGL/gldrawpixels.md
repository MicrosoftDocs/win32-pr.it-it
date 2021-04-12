---
title: funzione glDrawPixels (GL. h)
description: La funzione glDrawPixels scrive un blocco di pixel nel framebuffer.
ms.assetid: c4eda64f-a75e-4e6d-984d-af49414b94d8
keywords:
- funzione glDrawPixels OpenGL
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
ms.openlocfilehash: e25adc8ad28791086020a37d3a30651e169bfd07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119306"
---
# <a name="gldrawpixels-function"></a>glDrawPixels (funzione)

La funzione **glDrawPixels** scrive un blocco di pixel nel framebuffer.

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

Dimensione della larghezza del rettangolo pixel che verrà scritto nel framebuffer.

</dd> <dt>

*height* 
</dt> <dd>

Dimensione dell'altezza del rettangolo pixel che verrà scritto nel framebuffer.

</dd> <dt>

*format* 
</dt> <dd>

Formato dei dati pixel. Di seguito sono riportate le costanti simboliche accettabili.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt><strong>GL_COLOR_INDEX</strong></dt> </dl></td>
<td>Ogni pixel è un singolo valore, ovvero un indice colori. <br/>
<ol>
<li>La funzione <strong>glDrawPixels</strong> converte ogni pixel in formato a virgola fissa, con un numero di bit non specificato a destra del punto binario, indipendentemente dal tipo di dati della memoria. I valori a virgola mobile vengono convertiti in valori a virgola fissa true. La funzione <strong>glDrawPixels</strong> converte i dati firmati e unsigned integer con tutti i bit della frazione impostati su zero. La funzione converte i dati bitmap in 0,0 o 1,0.</li>
<li>La funzione <strong>glDrawPixels</strong> sposta ogni indice a virgola fissa lasciato da GL_INDEX_SHIFT bit e lo aggiunge al GL_INDEX_OFFSET. Se GL_INDEX_SHIFT è negativo, lo spostamento è a destra. In entrambi i casi, i bit a zero riempiono i percorsi di bit non specificati nel risultato.</li>
<li>In modalità RGBA, <strong>glDrawPixels</strong> converte l'indice risultante in un pixel RGBA usando le tabelle GL_PIXEL_MAP_I_TO_R, GL_PIXEL_MAP_I_TO_G, GL_PIXEL_MAP_I_TO_B e GL_PIXEL_MAP_I_TO_A. Quando si usa la modalità di indicizzazione dei colori e GL_MAP_COLOR è true, l'indice viene sostituito con il valore che <strong>glDrawPixels</strong> fa riferimento nella tabella di ricerca GL_PIXEL_MAP_I_TO_I.</li>
<li>Se la sostituzione della ricerca dell'indice viene eseguita o meno, la parte intera dell'indice è <strong>e</strong>ed è con 2<sup>b</sup> - 1, dove <em>b</em> è il numero di bit in un buffer di indice dei colori.</li>
<li>Gli indici o i colori RGBA risultanti vengono quindi convertiti in frammenti associando <em>la posizione raster</em>corrente e le coordinate di trama a ogni pixel e assegnando quindi le coordinate della finestra <em>x</em> e <em>y</em> al frammento <em>n</em>, in modo tale che <em>x</em>? = <em>larghezza</em> <em>x</em><sub>r</sub> + <em>n</em> mod<br/> <em>y</em>? = <em>y</em><sub>r</sub> + <em>n/Larghezza</em><br/> dove (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) è la posizione raster corrente.<br/></li>
<li>La funzione <strong>glDrawPixels</strong> considera questi frammenti di pixel esattamente come i frammenti generati da punti, linee o poligoni rasterizzati. Applica il mapping di trama, la nebbia e tutte le operazioni del frammento prima di scrivere i frammenti sul framebuffer.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_STENCIL_INDEX"></span><span id="gl_stencil_index"></span><dl> <dt><strong>GL_STENCIL_INDEX</strong></dt> </dl></td>
<td>Ogni pixel è un singolo valore, ovvero un indice di stencil. <br/>
<ol>
<li>La funzione <strong>glDrawPixels</strong> lo converte in formato a virgola fissa, con un numero di bit non specificato a destra del punto binario, indipendentemente dal tipo di dati della memoria. I valori a virgola mobile vengono convertiti in valori a virgola fissa true. La funzione <strong>glDrawPixels</strong> converte i dati firmati e unsigned integer con tutti i bit della frazione impostati su zero. I dati bitmap vengono convertiti in 0,0 o 1,0.</li>
<li>La funzione <strong>glDrawPixels</strong> sposta ogni indice a virgola fissa lasciato da GL_INDEX_SHIFT bit e lo aggiunge al GL_INDEX_OFFSET. Se GL_INDEX_SHIFT è negativo, lo spostamento è a destra. In entrambi i casi, i bit a zero riempiono i percorsi di bit non specificati nel risultato.</li>
<li>Se GL_MAP_STENCIL è true, l'indice viene sostituito con il valore che <strong>glDrawPixels</strong> fa riferimento alla tabella di ricerca GL_PIXEL_MAP_S_TO_S.</li>
<li>Se la sostituzione della ricerca dell'indice viene eseguita o meno, la parte integer dell'indice è quindi <strong>e</strong>ed è con 2<sup>b</sup> - 1, dove <em>b</em> è il numero di bit nel buffer dello stencil. Gli indici degli stencil risultanti vengono quindi scritti nel buffer dello stencil in modo che l'indice <em>n</em>venga scritto nella posizione <em>x</em>? = <em>larghezza</em> <em>x</em><sub>r</sub> + <em>n</em> mod<br/> <em>y</em>? = <em>y</em><sub>r</sub> + <em>n/Larghezza</em><br/> dove (<em>x</em><sub>r</sub> , <em></em> y<sub>r</sub> ) è la posizione raster corrente. Solo il test di proprietà dei pixel, il test a forbice e lo stencil writemask influiscono su queste Scritture.<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span id="GL_DEPTH_COMPONENT"></span><span id="gl_depth_component"></span><dl> <dt><strong>GL_DEPTH_COMPONENT</strong></dt> </dl></td>
<td>Ogni pixel è un componente a profondità singola. <br/>
<ol>
<li>La funzione <strong>glDrawPixels</strong> converte i dati a virgola mobile direttamente in un formato a virgola mobile interno con precisione non specificata. Per i dati Signed Integer viene eseguito il mapping lineare al formato a virgola mobile interno, in modo che il valore integer rappresentabile più positivo sia mappato a 1,0 e che il valore rappresentabile più negativo sia mappato a-1,0. Viene eseguito il mapping dei dati integer senza segno in modo analogo: il valore integer più grande viene mappato a 1,0 e zero viene mappato a 0,0.</li>
<li>La funzione <strong>glDrawPixels</strong> moltiplica il valore di profondità a virgola mobile risultante per GL_DEPTH_SCALE e lo aggiunge al GL_DEPTH_BIAS. Il risultato viene bloccato nell'intervallo [0, 1].</li>
<li>La funzione <strong>glDrawPixels</strong> converte i componenti di profondità risultanti in frammenti associando il colore della posizione raster corrente o l'indice dei colori e le coordinate di trama a ogni pixel, quindi assegnando le coordinate della finestra <em>x</em> e <em>y</em> al frammento <em>n</em> in modo tale che <em>x</em>? = <em></em><em>larghezza</em> x<sub>r</sub> + <em>n</em> mod<br/> <em>y</em>? = <em>y</em><sub>r</sub> + <em>n/Larghezza</em><br/> dove ( <em></em> x<sub>r</sub> ,<em>y</em><sub>r</sub> ) è la posizione raster corrente.<br/></li>
<li>Questi frammenti di pixel vengono quindi trattati come i frammenti generati dalla rasterizzazione di punti, linee o poligoni. La funzione <strong>glDrawPixels</strong> applica il mapping di trama, la nebbia e tutte le operazioni di frammento prima di scrivere i frammenti sul framebuffer.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt><strong>GL_RGBA</strong></dt> </dl></td>
<td>Ogni pixel è un gruppo di quattro componenti in questo ordine: rosso, verde, blu, alfa. <br/>
<ol>
<li>La funzione <strong>glDrawPixels</strong> converte i valori a virgola mobile direttamente in un formato a virgola mobile interno con precisione non specificata. I valori Signed Integer vengono mappati in modo lineare al formato a virgola mobile interno, in modo che il valore integer rappresentabile più positivo sia mappato a 1,0 e il valore rappresentativo più negativo sia mappato a-1,0. Viene eseguito il mapping dei dati integer senza segno in modo analogo: il valore integer più grande viene mappato a 1,0 e zero viene mappato a 0,0.</li>
<li>La funzione <strong>glDrawPixels</strong> moltiplica i valori dei colori a virgola mobile risultanti per GL_c_SCALE e li aggiunge a GL_c_BIAS, dove <em>c</em> è rosso, verde, blu e alfa per i rispettivi componenti di colore. I risultati vengono fissati nell'intervallo [0, 1].</li>
<li>Se GL_MAP_COLOR è true, <strong>glDrawPixels</strong> ridimensiona ogni componente del colore in base alla dimensione della tabella di ricerca GL_PIXEL_MAP_c_TO_c, quindi sostituisce il componente in base al valore a cui fa riferimento nella tabella. <em>c</em> è rispettivamente R, G, B o A.</li>
<li>La funzione <strong>glDrawPixels</strong> converte i colori RGBA risultanti in frammenti associando <em>la posizione raster</em>corrente e le coordinate della trama a ogni pixel, quindi assegnando le coordinate della finestra <em>x</em> e <em>y</em> al frammento <em>n</em>, ad esempio <em>x</em>? = <em>larghezza</em> <em>x</em><sub>r</sub> + <em>n</em> mod<br/> <em>y</em>? = /width <em>y</em><sub>r</sub> + <em>n</em><br/> dove (<em>x</em><sub>r</sub> ,<em>y</em><sub>r</sub> ) è la posizione raster corrente.<br/></li>
<li>Questi frammenti di pixel vengono quindi trattati come i frammenti generati dalla rasterizzazione di punti, linee o poligoni. La funzione <strong>glDrawPixels</strong> applica il mapping di trama, la nebbia e tutte le operazioni di frammento prima di scrivere i frammenti sul framebuffer.</li>
</ol></td>
</tr>
<tr class="odd">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <dt><strong>GL_RED</strong></dt> </dl></td>
<td>Ogni pixel è un singolo componente rosso.<br/> La funzione <strong>glDrawPixels</strong> converte il componente nel formato a virgola mobile interno nello stesso modo in cui il componente rosso di un pixel RGBA è e quindi lo converte in un pixel RGBA con verde e blu impostato su 0,0 e Alpha impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt><strong>GL_GREEN</strong></dt> </dl></td>
<td>Ogni pixel è un singolo componente verde.<br/> La funzione <strong>glDrawPixels</strong> converte il componente nel formato a virgola mobile interno nello stesso modo in cui il componente verde di un pixel RGBA è e quindi lo converte in un pixel RGBA con il rosso e il blu impostati su 0,0 e Alpha impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt><strong>GL_BLUE</strong></dt> </dl></td>
<td>Ogni pixel è un singolo componente blu.<br/> La funzione <strong>glDrawPixels</strong> converte il componente nel formato a virgola mobile interno nello stesso modo in cui il componente blu di un pixel RGBA è e quindi lo converte in un pixel RGBA con rosso e verde impostato su 0,0 e Alpha impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt><strong>GL_ALPHA</strong></dt> </dl></td>
<td>Ogni pixel è un singolo componente alfa.<br/> La funzione <strong>glDrawPixels</strong> converte il componente nel formato a virgola mobile interno nello stesso modo in cui il componente alfa di un pixel RGBA è e quindi lo converte in un pixel RGBA con rosso, verde e blu impostato su 0,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt><strong>GL_RGB</strong></dt> </dl></td>
<td>Ogni pixel è un gruppo di tre componenti in questo ordine: rosso, verde, blu. La funzione <strong>glDrawPixels</strong> converte ogni componente nel formato a virgola mobile interno nello stesso modo in cui i componenti rosso, verde e blu di un pixel RGBA sono. Il colore triple viene convertito in un pixel RGBA con Alpha impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt><strong>GL_LUMINANCE</strong></dt> </dl></td>
<td>Ogni pixel è un singolo componente di luminanza.<br/> La funzione <strong>glDrawPixels</strong> converte il componente nel formato a virgola mobile interno nello stesso modo in cui il componente rosso di un pixel RGBA è e quindi lo converte in un pixel RGBA con rosso, verde e blu impostato sul valore di luminanza convertito e Alpha impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt><strong>GL_LUMINANCE_ALPHA</strong></dt> </dl></td>
<td>Ogni pixel è un gruppo di due componenti in questo ordine: luminanza, alfa.<br/> La funzione <strong>glDrawPixels</strong> converte i due componenti nel formato a virgola mobile interno nello stesso modo in cui il componente rosso di un pixel RGBA è e quindi li converte in un pixel RGBA con rosso, verde e blu impostati sul valore di luminanza convertito e Alpha impostato sul valore alfa convertito. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt><strong>GL_BGR_EXT</strong></dt> </dl></td>
<td>Ogni pixel è un gruppo di tre componenti in questo ordine: blu, verde, rosso.<br/> GL_BGR_EXT fornisce un formato corrispondente al layout di memoria delle bitmap indipendenti dal dispositivo (DIB) Windows. Quindi, le applicazioni possono usare gli stessi dati con le chiamate di funzione di Windows e le chiamate di funzione pixel OpenGL.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt><strong>GL_BGRA_EXT</strong></dt> </dl></td>
<td>Ogni pixel è un gruppo di quattro componenti in questo ordine: blu, verde, rosso, alfa.<br/> GL_BGRA_EXT fornisce un formato corrispondente al layout di memoria delle bitmap indipendenti dal dispositivo (DIB) Windows. Quindi, le applicazioni possono usare gli stessi dati con le chiamate di funzione di Windows e le chiamate di funzione pixel OpenGL.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*type* 
</dt> <dd>

Tipo di dati per *pixel*. Di seguito sono riportate le costanti simboliche accettate e i relativi significati.



| Valore                                                                                                                                                                      | Significato                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**\_byte senza segno GL \_**</dt> </dl>    | Intero senza segno a 8 bit<br/>                 |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**\_byte GL**</dt> </dl>                                | Valore intero con segno a 8 bit<br/>                   |
| <span id="GL_BITMAP"></span><span id="gl_bitmap"></span><dl> <dt>**\_bitmap GL**</dt> </dl>                          | Bit singoli negli interi senza segno a 8 bit<br/> |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**\_short senza segno GL \_**</dt> </dl> | Intero senza segno a 16 bit<br/>                |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**\_short GL**</dt> </dl>                             | Valore intero a 16 bit con segno<br/>                  |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL \_ senza segno \_ int**</dt> </dl>       | Intero senza segno a 32 bit<br/>                |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ int**</dt> </dl>                                   | Intero a 32 bit<br/>                         |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ float**</dt> </dl>                             | Virgola mobile a precisione singola<br/>        |



 

</dd> <dt>

*pixel* 
</dt> <dd>

Puntatore ai dati pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | La *larghezza* o l' *altezza* è negativa.<br/>                                                                                                                                          |
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | Il *formato* o il *tipo* non è un valore accettato. <br/>                                                                                                                             |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | il *formato* era GL \_ Red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ Luminance o GL \_ Luminance \_ Alpha, mentre OpenGL era in modalità di indice a colori.<br/> |
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | il *tipo* era \_ una bitmap GL e il *formato* non era GL \_ Color \_ index o GL \_ stencil \_ index.<br/>                                                                                         |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | il *formato* è l' \_ indice dello stencil GL e non \_ esiste alcun buffer dello stencil.<br/>                                                                                                                  |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>                                                        |


## <a name="remarks"></a>Commenti

La funzione **glDrawPixels** legge i dati dei pixel dalla memoria e li scrive nel framebuffer rispetto alla posizione raster corrente. Usare [**glRasterPos**](glrasterpos-functions.md) per impostare la posizione raster corrente e usare [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con l'argomento GL \_ Current \_ raster \_ position per eseguire una query sulla posizione raster.

Diversi parametri definiscono la codifica dei dati pixel in memoria e controllano l'elaborazione dei dati pixel prima che vengano inseriti nel framebuffer. Questi parametri vengono impostati con quattro funzioni: [**glPixelStore**](glpixelstore-functions.md), [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md)e [**glPixelZoom**](glpixelzoom.md). Questo argomento descrive gli effetti sui **glDrawPixels** di molti, ma non tutti, dei parametri specificati da queste quattro funzioni.

I dati vengono letti da *pixel* come sequenza di byte firmati o senza segno, short con segno o senza segno, interi con segno o senza segno o valori a virgola mobile a precisione singola, a seconda del *tipo*. Ognuno di questi byte, short, interi o valori a virgola mobile viene interpretato come un componente di colore o profondità o un indice, a seconda del *formato*. Gli indici vengono sempre trattati singolarmente. I componenti dei colori vengono considerati come gruppi di uno, due, tre o quattro valori, in base al *formato*. Sia i singoli indici che i gruppi di componenti vengono definiti pixel. Se il *tipo* è una \_ bitmap GL, i dati devono essere byte senza segno e il *formato* deve essere GL \_ Color \_ index o GL \_ stencil \_ index. Ogni byte senza segno viene considerato come pixel a 8 1 bit, con l'ordine dei bit determinato da GL \_ depack \_ LSB \_ First (vedere [**glPixelStore**](glpixelstore-functions.md)).

La *larghezza* in pixel di *altezza* viene letta dalla memoria, a partire dalla posizione *pixel*. Per impostazione predefinita, questi pixel vengono ricavati dalle posizioni di memoria adiacenti, ad eccezione del fatto che dopo la lettura di tutti i pixel di *larghezza* , il puntatore di lettura viene spostato al limite successivo di 4 byte. La funzione **glPixelStore** specifica l'allineamento a 4 byte della riga con argomento GL \_ decomprimere l' \_ allineamento ed è possibile impostarlo su 1, 2, 4 o 8 byte. Altri parametri dell'archivio pixel specificano avanzamenti del puntatore di lettura diversi, prima che venga letto il primo pixel e dopo la lettura di tutti i pixel di *larghezza* . La funzione **glPixelStore** opera su ognuno dei pixel di *larghezza per altezza* che legge dalla memoria nello stesso modo, in base ai valori di diversi parametri specificati da [**glPixelTransfer**](glpixeltransfer.md) e [**glPixelMap**](glpixelmap.md). I dettagli di queste operazioni, così come il buffer di destinazione in cui vengono disegnati i pixel, sono specifici del formato dei pixel, come specificato dal *formato*.

La rasterizzazione descritta fino a questo punto presuppone i fattori di zoom pixel di 1,0. Se si usa [**glPixelZoom**](glpixelzoom.md) per modificare i fattori di zoom *x* e *y* pixel, i pixel vengono convertiti in frammenti come indicato di seguito. Se (*XR, yr*) è la posizione raster corrente e un pixel specificato si trova nella colonna *n* e *m* della riga del rettangolo pixel, verranno generati frammenti per i pixel i cui centri si trovano nel rettangolo con angoli

(*x*<sub>r</sub>  +  *Zoom*? *n*, *y*<sub>r</sub>  +  *Zoom*<sub>y</sub> *m*)

(*x*<sub>r</sub>  +  *Zoom*? (*n* + 1), *y*<sub>r</sub>  +  *Zoom*<sub>y</sub> (*m* + 1))

dove *Zoom*? è il valore di GL \_ Zoom \_ X e *Zoom*<sub>y</sub> è il valore di GL \_ Zoom \_ y.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glDrawPixels**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ raster \_ position

**glGet** con argomento GL \_ Current \_ raster \_ position \_ valido

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
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

[**Remo**](glend.md)
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

 

 





