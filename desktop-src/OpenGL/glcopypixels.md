---
title: Funzione glCopyPixels (Gl.h)
description: La funzione glCopyPixels copia i pixel nel buffer frame.
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
ms.openlocfilehash: 43c399b4ce63f84c41bcb2d65140356ac20a6ddd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479447"
---
# <a name="glcopypixels-function"></a>Funzione glCopyPixels

La **funzione glCopyPixels** copia i pixel nel buffer frame.

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

Coordinata del piano y della finestra dell'angolo inferiore sinistro dell'area rettangolare di pixel da copiare.

</dd> <dt>

*width* 
</dt> <dd>

Dimensione della larghezza dell'area rettangolare di pixel da copiare. Deve essere non negativo.

</dd> <dt>

*height* 
</dt> <dd>

Dimensione dell'altezza dell'area rettangolare di pixel da copiare. Deve essere non negativo.

</dd> <dt>

*type* 
</dt> <dd>

Specifica se **glCopyPixels** deve copiare i valori dei colori, dei valori di profondità o degli stencil. Le costanti simboliche accettabili sono .




| valore | Significato | 
|-------|---------|
| <span id="GL_COLOR"></span><span id="gl_color"></span><dl><dt><strong>GL_COLOR</strong></dt></dl> | La <strong>funzione glCopyPixels</strong> legge gli indici o i colori RGBA dal buffer attualmente specificato come buffer di origine di lettura (vedere <a href="glreadbuffer.md"><strong>glReadBuffer).</strong></a> <br /> Se OpenGL è in modalità color-index:<br /><ol><li>Ogni indice letto da questo buffer viene convertito in un formato a virgola fissa con un numero non specificato di bit a destra del punto binario.</li><li>Ogni indice viene spostato a sinistra di GL_INDEX_SHIFT bit e aggiunto a GL_INDEX_OFFSET. Se GL_INDEX_SHIFT è negativo, lo spostamento è a destra. In entrambi i casi, zero bit riempiono le posizioni di bit altrimenti non specificata nel risultato.<br /></li><li>Se GL_MAP_COLOR è true, l'indice viene sostituito con il valore a cui fa riferimento nella tabella di GL_PIXEL_MAP_I_TO_I.</li><li>Se la sostituzione di ricerca dell'indice viene eseguita o meno, la parte intera dell'indice è quindi <strong>AND</strong>ed con 2<em><sup>b</sup></em> 1, dove <em>b</em> è il numero di bit in un index buffer.</li></ol>Se OpenGL è in modalità RGBA:<br /><ol><li>I componenti rosso, verde, blu e alfa di ogni pixel letto vengono convertiti in un formato a virgola mobile interno con precisione non specificata.</li><li>La conversione esegue il mapping del valore del componente rappresentabile più grande a 1,0 e del valore del componente da zero a 0,0.</li><li>I valori di colore a virgola mobile risultanti vengono quindi moltiplicati per GL_c_SCALE e aggiunti a GL_c_BIAS, dove c è <em>RED,</em> GREEN, BLUE e ALPHA per i rispettivi componenti di colore.</li><li>I risultati vengono definiti nell'intervallo [0,1].</li><li>Se GL_MAP_COLOR è true, ogni componente colore viene ridimensionato in base alle dimensioni della tabella di ricerca GL_PIXEL_MAP_c_TO_c e quindi sostituito dal valore a cui fa riferimento nella tabella; <em>c</em> è rispettivamente R, G, B o A. Gli indici o i colori RGBA risultanti vengono quindi convertiti in frammenti collegando la coordinata <em>z</em>corrente della posizione raster e della trama a ogni pixel e quindi assegnando le coordinate della finestra (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub>j ), dove ( x r , y r ) è la posizione raster corrente e il pixel è il pixel nella posizione i nella riga  +  <em></em> <em></em><sub></sub> <em>j.</em> <em></em><sub></sub> <em></em> Questi frammenti di pixel vengono quindi trattati esattamente come i frammenti generati dall'rasterizzazione di punti, linee o poligoni. Il mapping di trame, il riempimento e tutte le operazioni sui frammenti vengono applicati prima che i frammenti siano scritti nel framebuffer.<br /></li></ol> | 
| <span id="GL_DEPTH"></span><span id="gl_depth"></span><dl><dt><strong>GL_DEPTH</strong></dt></dl> | I valori di profondità vengono letti dal buffer di profondità e convertiti direttamente in un formato a virgola mobile interno con precisione non specificata. Il valore di profondità a virgola mobile risultante viene quindi moltiplicato per GL_DEPTH_SCALE e aggiunto a GL_DEPTH_BIAS. Il risultato viene definito in base all'intervallo [0,1]. <br /> I componenti di profondità risultanti vengono quindi convertiti in frammenti collegando il colore della posizione raster corrente o l'indice dei colori e le coordinate della trama a ogni pixel, quindi assegnando le coordinate della finestra (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub>j ), dove ( x r , y r ) è la posizione raster corrente e il pixel è il pixel nella posizione i nella  +  <em></em>riga<em></em><sub></sub> <em></em><sub></sub> <em>j.</em> <em></em> Questi frammenti di pixel vengono quindi trattati esattamente come i frammenti generati dall'rasterizzazione di punti, linee o poligoni. Il mapping di trame, il riempimento e tutte le operazioni sui frammenti vengono applicati prima che i frammenti siano scritti nel framebuffer.<br /> | 
| <span id="GL_STENCIL"></span><span id="gl_stencil"></span><dl><dt><strong>GL_STENCIL</strong></dt></dl> | Gli indici degli stencil vengono letti dal buffer degli stencil e convertiti in un formato a virgola fissa interno con un numero non specificato di bit a destra del punto binario. Ogni indice a virgola fissa viene quindi spostato a sinistra di GL_INDEX_SHIFT bit e aggiunto a GL_INDEX_OFFSET. Se GL_INDEX_SHIFT è negativo, lo spostamento è a destra. In entrambi i casi, zero bit riempiono le posizioni di bit altrimenti non specificata nel risultato. Se GL_MAP_STENCIL è true, l'indice viene sostituito con il valore a cui fa riferimento nella tabella di GL_PIXEL_MAP_S_TO_S. Indipendentemente dal fatto che la sostituzione di ricerca dell'indice sia eseguita o meno, la parte intera dell'indice è <strong>quindi AND</strong>con 2<sup>b</sup> - 1, dove <em>b</em> è il numero di bit nel buffer degli stencil. Gli indici degli stencil risultanti vengono quindi scritti nel buffer degli stencil in modo che l'indice letto dalla posizione <em>i</em> della riga <em>j</em> sia scritto nella posizione (<em>x</em><sub>r</sub>  +  <em>i</em>, <em>y</em><sub>r</sub>j ), dove ( x r , y r ) è la posizione  +  <em></em>raster corrente.<em></em><sub></sub> <em></em><sub></sub> Solo il test di proprietà dei pixel, il test di scissor e la maschera di scrittura degli stencil influiscono su queste scritture.<br /> | 




 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *il* tipo non è un valore accettato.<br/>                                                                                          |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | Larghezza *o* altezza è negativa.<br/>                                                                                     |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | *Il tipo* è GL \_ DEPTH e non è presente alcun buffer di profondità.<br/>                                                                        |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | *Il tipo* era GL \_ STENCIL e non era presente alcun buffer stencil.<br/>                                                                    |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glCopyPixels** copia un rettangolo di pixel allineato allo schermo dalla posizione framebuffer specificata in un'area relativa alla posizione raster corrente. L'operazione è ben definita solo se l'intera area di origine pixel si trova all'interno della parte esposta della finestra. I risultati delle copie dall'esterno della finestra o dalle aree della finestra non esposte dipendono dall'hardware e non sono definiti.

I *parametri x* e *y* specificano le coordinate della finestra dell'angolo inferiore sinistro dell'area rettangolare da copiare. I *parametri width* e *height* specificano le dimensioni dell'area rettangolare da copiare. Sia *la larghezza* che *l'altezza* devono essere non ergative.

Diversi parametri controllano l'elaborazione dei dati pixel durante la copia. Questi parametri vengono impostati con tre funzioni: [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md)e [**glPixelZoom**](glpixelzoom.md). Questo argomento descrive gli effetti su **glCopyPixels** per la maggior parte dei parametri specificati da queste tre funzioni, ma non tutti.

La **funzione glCopyPixels** copia i valori da ogni pixel con l'angolo inferiore sinistro in (*x* i , y j ) per 0 = larghezza i e  +     +     <   0 = *altezza j*  <  . Questo pixel è detto pixel *i* nella *riga j.* I pixel vengono copiati in ordine di riga dalla riga più bassa alla più alta, da sinistra a destra in ogni riga.

Il *parametro* type specifica se i dati relativi a colore, profondità o stencil devono essere copiati.

La rasterizzazione descritta finora presuppone fattori di zoom in pixel di 1,0. Se si usa [**glPixelZoom**](glpixelzoom.md) per modificare i fattori di zoom in pixel *x* e *y,* i pixel vengono convertiti in frammenti come indicato di seguito. Se (*x*<sub>r</sub> , *y*<sub>r</sub> ) è la posizione raster corrente e un determinato pixel si trova nella posizione *i* nella riga *j* del rettangolo di pixel di origine, vengono generati frammenti per i pixel i cui centri si trova nel rettangolo con angoli in corrispondenza di

(*x*<sub>r</sub>  +  *zoom*? i, y <sub>r</sub>  +  *zoom*<sub>y</sub> *j*)

e

(*x*<sub>r</sub>  +  *zoom*? (*i* + 1), *y*<sub>r</sub>  +  *zoom*<sub>y</sub> (*j* + 1))

where *zoom*? è il valore di GL \_ ZOOM X e \_ *zoom*<sub>y</sub> è il valore di GL \_ ZOOM \_ Y.

Le modalità specificate [**da glPixelStore**](glpixelstore-functions.md) non hanno alcun effetto sul funzionamento di **glCopyPixels.**

Le funzioni seguenti recuperano informazioni correlate **a glCopyPixels:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ CURRENT \_ RASTER \_ POSITION

**glGet** con argomento GL \_ CURRENT \_ RASTER \_ POSITION \_ VALID

Per copiare il pixel del colore nell'angolo inferiore sinistro della finestra nella posizione raster corrente, usare

**glCopyPixels**( 0, 0, 1, 1, GL \_ COLOR );

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

 

 





