---
title: Funzione glColorSubTableEXT (Gl.h)
description: La funzione glColorSubTableEXT specifica una parte della tavolozza della trama di destinazione da sostituire.
ms.assetid: 21430245-f837-4c7a-944f-b44482254b12
keywords:
- Funzione glColorSubTableEXT OpenGL
topic_type:
- apiref
api_name:
- glColorSubTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d99b8dcef2ef21b4d75eb5262d2e3ecffa3804fa8e7a4889ae5dcbf8d68f018
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081681"
---
# <a name="glcolorsubtableext-function"></a>Funzione glColorSubTableEXT

La **funzione glColorSubTableEXT** specifica una parte della tavolozza della trama di destinazione da sostituire.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glColorSubTableEXT(
         GLenum  target,
         GLsizei start,
         GLsizei count,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Trama con tavolozza di destinazione che deve essere modificata. Deve essere TEXTURE \_ 1D o TEXTURE \_ 2D.

</dd> <dt>

*start* 
</dt> <dd>

Voce iniziale dell'indice del riquadro da modificare.

</dd> <dt>

*count* 
</dt> <dd>

Numero di voci dell'indice del riquadro da modificare a partire *dall'inizio.* Il *parametro count* determina l'intervallo di voci dell'indice del riquadro che vengono modificate.

</dd> <dt>

*format* 
</dt> <dd>

Formato dei dati pixel. Vengono accettate le costanti simboliche seguenti.



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
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt><strong>GL_RGBA</strong></dt> </dl></td>
<td>Ogni pixel è un gruppo di quattro componenti nell'ordine seguente: rosso, verde, blu, alfa. Il formato RGBA viene determinato in questo modo: <br/>
<ol>
<li>La <strong>funzione glColorSubTableEXT</strong> converte i valori a virgola mobile direttamente in un formato interno con precisione non specificata. I valori integer con segno vengono mappati in modo lineare al formato interno in modo che il valore intero rappresentabile più positivo sia mappato a 1,0 e il valore rappresentabile più negativo sia mappato a -1,0. I dati integer senza segno vengono mappati in modo analogo: il valore intero più grande viene mappato a 1,0 e zero viene mappato a 0,0.</li>
<li>La <strong>funzione glColorSubTableEXT</strong> moltiplica i valori di colore risultanti per GL_c_SCALE e li aggiunge a GL_c_BIAS, dove <em>c</em> è RED, GREEN, BLUE e ALPHA per i rispettivi componenti di colore. I risultati sono ancorati all'intervallo [0,1].</li>
<li>Se GL_MAP_COLOR è <strong>TRUE,</strong> <strong>glColorSubTableEXT</strong> ridimensiona ogni componente di colore in base alle dimensioni della tabella di ricerca GL_PIXEL_MAP_c_TO_c, quindi sostituisce il componente con il valore a cui fa riferimento nella tabella; <em>c</em> è rispettivamente R, G, B o A.</li>
<li>La funzione <strong>glColorSubTableEXT</strong> converte i colori RGBA risultanti in frammenti associando la posizione raster <em>corrente z</em>-coordinate e le coordinate di trama a ogni pixel, quindi assegnando le coordinate della finestra <em>x</em> e <em>y</em> al <em>frammento n</em>in modo che<em>x</em>? = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em><br/> <em>y</em>? = <em>y</em><sub>r</sub> +<em>n/width</em><br/> dove (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) è la posizione raster corrente.<br/></li>
<li>Questi frammenti di pixel vengono quindi trattati esattamente come i frammenti generati dalla rasterizzazione di punti, linee o poligoni. La <strong>funzione glColorSubTableEXT</strong> applica il mapping delle trame, la nebbia e tutte le operazioni sui frammenti prima di scrivere i frammenti nel framebuffer.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <dt><strong>GL_RED</strong></dt> </dl></td>
<td>Ogni pixel è un singolo componente rosso.<br/> La funzione <strong>glColorSubTableEXT</strong> converte questo componente nel formato interno nello stesso modo in cui si trova il componente rosso di un pixel RGBA, quindi lo converte in un pixel RGBA con verde e blu impostato su 0,0 e alfa impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come un pixel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt><strong>GL_GREEN</strong></dt> </dl></td>
<td>Ogni pixel è un singolo componente verde.<br/> La funzione <strong>glColorSubTableEXT</strong> converte questo componente nel formato interno nello stesso modo del componente verde di un pixel RGBA e quindi lo converte in un pixel RGBA con rosso e blu impostato su 0,0 e alfa impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come un pixel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt><strong>GL_BLUE</strong></dt> </dl></td>
<td>Ogni pixel è un singolo componente blu.<br/> La funzione <strong>glColorSubTableEXT</strong> converte questo componente nel formato interno nello stesso modo del componente blu di un pixel RGBA e quindi lo converte in un pixel RGBA con rosso e verde impostato su 0,0 e alfa impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come un pixel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt><strong>GL_ALPHA</strong></dt> </dl></td>
<td>Ogni pixel è un singolo componente alfa.<br/> La funzione <strong>glColorSubTableEXT</strong> converte questo componente nel formato interno nello stesso modo del componente alfa di un pixel RGBA e quindi lo converte in un pixel RGBA con rosso, verde e blu impostato su 0,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come un pixel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt><strong>GL_RGB</strong></dt> </dl></td>
<td>Ogni pixel è un gruppo di tre componenti nell'ordine seguente: rosso, verde, blu.<br/> La <strong>funzione glColorSubTableEXT</strong> converte ogni componente nel formato interno nello stesso modo in cui sono i componenti rosso, verde e blu di un pixel RGBA. La tripla di colore viene convertita in un pixel RGBA con alfa impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come un pixel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt><strong>GL_BGR_EXT</strong></dt> </dl></td>
<td>Ogni pixel è un gruppo di tre componenti nell'ordine seguente: blu, verde, rosso.<br/> GL_BGR_EXT un formato che corrisponde al layout di memoria Windows bitmap indipendenti dal dispositivo (DIB). Di conseguenza, le applicazioni possono usare gli stessi dati con Windows di funzione e chiamate di funzione pixel OpenGL.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt><strong>GL_BGRA_EXT</strong></dt> </dl></td>
<td>Ogni pixel è un gruppo di quattro componenti nell'ordine seguente: blu, verde, rosso, alfa.<br/> GL_BGRA_EXT un formato che corrisponde al layout di memoria Windows bitmap indipendenti dal dispositivo (DIB). Di conseguenza, le applicazioni possono usare gli stessi dati con Windows di funzione e chiamate di funzione pixel OpenGL.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*type* 
</dt> <dd>

Tipo di dati per *i dati*. Vengono accettate le costanti simboliche seguenti: GL \_ UNSIGNED \_ BYTE, GL \_ BYTE, GL \_ UNSIGNED \_ SHORT, GL \_ SHORT, GL \_ UNSIGNED \_ INT, GL \_ INT e GL \_ FLOAT.

Nella tabella seguente viene riepilogato il significato delle costanti valide per il *parametro di* tipo.



| Valore                                                                                                                                                                      | Significato                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**GL \_ UNSIGNED \_ BYTE**</dt> </dl>    | Intero senza segno a 8 bit<br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**GL \_ BYTE**</dt> </dl>                                | Valore intero con segno a 8 bit<br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**GL \_ UNSIGNED \_ SHORT**</dt> </dl> | Intero senza segno a 16 bit<br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**GL \_ SHORT**</dt> </dl>                             | Valore intero a 16 bit con segno<br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL \_ UNSIGNED \_ INT**</dt> </dl>       | Intero senza segno a 32 bit<br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ INT**</dt> </dl>                                   | Intero a 32 bit<br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ FLOAT**</dt> </dl>                             | Valore a virgola mobile e precisione singola<br/> |



 

</dd> <dt>

*data* 
</dt> <dd>

Puntatore ai dati della trama con tavolozza. I dati vengono considerati come singoli pixel di una voce della tavolozza di trame 1D per una voce del riquadro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                              | Significato                                                                                                                               |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl> | *start* o *count* è un numero intero non valido.<br/>                                                                                 |
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>  | *target*, *format* o *type* non è un valore accettato.<br/>                                                                    |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glColorSubTableEXT** specifica parti della tavolozza della trama di destinazione corrente da sostituire. A [**differenza di glColorTableEXT,**](glcolortableext.md)non è possibile specificare il *parametro di destinazione* come tavolozza della trama proxy.

> [!Note]  
> La **funzione glColorSubTableEXT** è una funzione di estensione che non fa parte della libreria OpenGL standard, ma fa parte dell'estensione della trama con tavolozza GL \_ \_ EXT. \_ Per verificare se l'implementazione di OpenGL supporta **glColorSubTableEXT,** chiamare [**glGetString**](glgetstring.md)(GL \_ EXTENSIONS). Se restituisce una trama con tavolozza GL \_ \_ \_ EXT, **glColorSubTableEXT** è supportato. Per ottenere l'indirizzo della funzione di una funzione di estensione, [**chiamare wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                      |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Gl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorTableEXT**](glcolortableext.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetColorTableEXT**](glgetcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





