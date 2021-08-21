---
title: Funzione glCopyPixels (Gl.h)
description: La funzione glCopyPixels copia i pixel nel framebuffer.
ms.assetid: c4055928-7b8b-4d0f-94f3-e3b9c0503308
keywords:
- Funzione glCopyPixels OpenGL
topic_type:
- apiref
api_name:
- glCopyPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff31d347e0ab6bedce29898c40451976e3a38990adebc7ae2396878bf726ce1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061825"
---
# <a name="glcopypixels-function"></a>Funzione glCopyPixels

La **funzione glCopyPixels** copia i pixel nel framebuffer.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glCopyPixels(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLenum  type
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*x* 
</dt> <dd>

Coordinata del piano x della finestra dell'angolo inferiore sinistro dell'area rettangolare di pixel da copiare.

</dd> <dt>

*y* 
</dt> <dd>

Coordinata del piano y della finestra dell'angolo inferiore sinistro dell'area rettangolare dei pixel da copiare.

</dd> <dt>

*width* 
</dt> <dd>

Dimensione della larghezza dell'area rettangolare dei pixel da copiare. Deve essere non negativo.

</dd> <dt>

*height* 
</dt> <dd>

Dimensione dell'altezza dell'area rettangolare dei pixel da copiare. Deve essere non negativo.

</dd> <dt>

*type* 
</dt> <dd>

Specifica se **glCopyPixels** deve copiare valori di colore, valori di profondità o valori di stencil. Le costanti simboliche accettabili sono .



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
<td><span id="GL_COLOR"></span><span id="gl_color"></span><dl> <dt><strong>GL_COLOR</strong></dt> </dl></td>
<td>La <strong>funzione glCopyPixels</strong> legge gli indici o i colori RGBA dal buffer attualmente specificato come buffer di origine di lettura (vedere <a href="glreadbuffer.md"><strong>glReadBuffer</strong></a>). <br/> Se OpenGL è in modalità indice colori:<br/>
<ol>
<li>Ogni indice letto da questo buffer viene convertito in un formato a virgola fissa con un numero non specificato di bit a destra del punto binario.</li>
<li>Ogni indice viene spostato a sinistra di GL_INDEX_SHIFT bit e aggiunto a GL_INDEX_OFFSET. Se GL_INDEX_SHIFT è negativo, lo spostamento è a destra. In entrambi i casi, zero bit riempiono le posizioni di bit altrimenti non specifiche nel risultato.<br/></li>
<li>Se GL_MAP_COLOR è true, l'indice viene sostituito con il valore a cui fa riferimento nella tabella di ricerca GL_PIXEL_MAP_I_TO_I.</li>
<li>Indipendentemente dal fatto che la sostituzione di ricerca dell'indice sia eseguita o meno, la parte intera dell'indice è quindi <strong>AND</strong>ed con 2<em><sup>b</sup></em> 1, dove <em>b</em> è il numero di bit in un oggetto color-index buffer.</li>
</ol>
Se OpenGL è in modalità RGBA:<br/>
<ol>
<li>I componenti rosso, verde, blu e alfa di ogni pixel letto vengono convertiti in un formato a virgola mobile interno con precisione non specificata.</li>
<li>La conversione esegue il mapping del valore del componente rappresentabile più grande a 1,0 e del valore del componente zero a 0,0.</li>
<li>I valori di colore a virgola mobile risultanti vengono quindi moltiplicati per GL_c_SCALE e aggiunti a GL_c_BIAS, dove <em>c</em> è RED, GREEN, BLUE e ALPHA per i rispettivi componenti di colore.</li>
<li>I risultati sono ancorati all'intervallo [0,1].</li>
<li>Se GL_MAP_COLOR è true, ogni componente di colore viene ridimensionato in base alle dimensioni della tabella di ricerca GL_PIXEL_MAP_c_TO_c e quindi sostituito dal valore a cui fa riferimento in tale tabella; <em>c</em> è rispettivamente R, G, B o A. Gli indici o i colori RGBA risultanti vengono quindi convertiti in frammenti collegando la posizione raster <em>corrente</em>z -coordinate e coordinate trama a ogni pixel e quindi assegnando le coordinate della finestra (<em>x</em><sub>r</sub> i, y r j ), dove ( x r , y r ) è la posizione raster corrente e il pixel era il pixel nella posizione i nella + riga <em>j.</em> <em></em><sub></sub> <em></em><sub></sub> + <em></em><em></em><sub></sub> <em></em> Questi frammenti di pixel vengono quindi trattati esattamente come i frammenti generati dalla rasterizzazione di punti, linee o poligoni. Il mapping delle trame, la nebbia e tutte le operazioni sui frammenti vengono applicati prima che i frammenti siano scritti nel framebuffer.<br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_DEPTH"></span><span id="gl_depth"></span><dl> <dt><strong>GL_DEPTH</strong></dt> </dl></td>
<td>I valori di profondità vengono letti dal buffer di profondità e convertiti direttamente in un formato a virgola mobile interno con precisione non specificata. Il valore di profondità a virgola mobile risultante viene quindi moltiplicato per GL_DEPTH_SCALE e aggiunto alla GL_DEPTH_BIAS. Il risultato è ancorato all'intervallo [0,1]. <br/> I componenti di profondità risultanti vengono quindi convertiti in frammenti collegando il colore della posizione raster corrente o l'indice dei colori e le coordinate della trama a ogni pixel, quindi assegnando le coordinate della finestra (<em>x</em><sub>r</sub> i, y r j ), dove ( x r , y r ) è la posizione raster corrente e il pixel era il pixel nella posizione i nella + riga <em>j.</em> <em></em><sub></sub> <em></em><sub></sub> + <em></em><em></em><sub></sub> <em></em> Questi frammenti di pixel vengono quindi trattati esattamente come i frammenti generati dalla rasterizzazione di punti, linee o poligoni. Il mapping delle trame, la nebbia e tutte le operazioni sui frammenti vengono applicati prima che i frammenti siano scritti nel framebuffer.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_STENCIL"></span><span id="gl_stencil"></span><dl> <dt><strong>GL_STENCIL</strong></dt> </dl></td>
<td>Gli indici degli stencil vengono letti dal buffer degli stencil e convertiti in un formato a virgola fissa interno con un numero non specificato di bit a destra del punto binario. Ogni indice a virgola fissa viene quindi spostato a sinistra di GL_INDEX_SHIFT bit e aggiunto a GL_INDEX_OFFSET. Se GL_INDEX_SHIFT è negativo, lo spostamento è a destra. In entrambi i casi, zero bit riempiono le posizioni di bit altrimenti non specifiche nel risultato. Se GL_MAP_STENCIL è true, l'indice viene sostituito con il valore a cui fa riferimento nella tabella di ricerca GL_PIXEL_MAP_S_TO_S. Indipendentemente dal fatto che la sostituzione di ricerca dell'indice sia eseguita o meno, la parte intera dell'indice è <strong>quindi AND</strong>ed con 2<sup>b</sup> 1, dove b è il numero di bit nel - buffer di stencil. <em></em> Gli indici degli stencil risultanti vengono quindi scritti nel buffer degli stencil in modo che l'indice letto dalla posizione <em>i</em> della riga <em>j</em> sia scritto nella posizione (<em>x</em><sub>r</sub> + <em>i</em>, <em>y</em><sub>r</sub> + <em>j</em>), dove (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) è la posizione raster corrente. Solo il test di proprietà dei pixel, il test della forbice e la maschera di scrittura dello stencil influiscono su queste scritture.<br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *type* non è un valore accettato.<br/>                                                                                          |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | La *larghezza o* l'altezza erano negative.<br/>                                                                                     |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | *il tipo* è GL \_ DEPTH e non è presente alcun buffer di profondità.<br/>                                                                        |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | *Il tipo* era GL \_ STENCIL e non era presente alcun buffer di stencil.<br/>                                                                    |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glCopyPixels** copia un rettangolo di pixel allineato allo schermo dalla posizione framebuffer specificata in un'area relativa alla posizione raster corrente. L'operazione è ben definita solo se l'intera area di origine pixel si trova all'interno della parte esposta della finestra. I risultati delle copie dall'esterno della finestra o dalle aree della finestra non esposte sono dipendenti dall'hardware e non definiti.

I *parametri x* e *y* specificano le coordinate della finestra dell'angolo inferiore sinistro dell'area rettangolare da copiare. I *parametri width* e *height* specificano le dimensioni dell'area rettangolare da copiare. Sia *la larghezza* che *l'altezza* devono essere non neghevoli.

Diversi parametri controllano l'elaborazione dei dati pixel durante la copia. Questi parametri vengono impostati con tre funzioni: [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md)e [**glPixelZoom**](glpixelzoom.md). Questo argomento descrive gli effetti su **glCopyPixels** della maggior parte, ma non di tutti, dei parametri specificati da queste tre funzioni.

La **funzione glCopyPixels** copia i valori da ogni pixel con l'angolo inferiore sinistro in (*x*  +  *i*, *y*  +  *j*) per 0 = *larghezza i* e  <   0 = *altezza j*  <  . Questo pixel viene detto pixel *i* nella *riga j.* I pixel vengono copiati in ordine di riga dalla riga più bassa alla riga più alta, da sinistra a destra in ogni riga.

Il *parametro type* specifica se i dati relativi a colore, profondità o stencil devono essere copiati.

La rasterizzazione descritta finora presuppone fattori di zoom pixel di 1,0. Se si usa [**glPixelZoom**](glpixelzoom.md) per modificare i fattori di zoom dei pixel *x* *e y,* i pixel vengono convertiti in frammenti come indicato di seguito. Se (*x*<sub>r</sub> , *y*<sub>r</sub> ) è la posizione raster corrente e un determinato pixel si trova nella posizione *i* nella riga *j* del rettangolo di pixel di origine, vengono generati frammenti per i pixel i cui centri si trova nel rettangolo con angoli in corrispondenza di

(*x*<sub>r</sub>  +  *zoom*? i, y <sub>r</sub>  +  *zoom*<sub>y</sub> *j*)

e

(*x*<sub>r</sub>  +  *zoom*? (*i* + 1), *y*<sub>r</sub>  +  *zoom*<sub>y</sub> (*j* + 1))

dove *zoom*? è il valore di GL \_ ZOOM X e \_ *zoom*<sub>y</sub> è il valore di GL \_ ZOOM \_ Y.

Le modalità specificate [**da glPixelStore**](glpixelstore-functions.md) non hanno alcun effetto sul funzionamento di **glCopyPixels**.

Le funzioni seguenti recuperano informazioni correlate a **glCopyPixels**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ CURRENT \_ RASTER \_ POSITION

**glGet con** argomento GL \_ CURRENT \_ RASTER POSITION \_ \_ VALID

Per copiare il pixel di colore nell'angolo inferiore sinistro della finestra nella posizione raster corrente, usare

**glCopyPixels**( 0, 0, 1, 1, GL \_ COLOR );

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
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

[**glReadBuffer**](glreadbuffer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





