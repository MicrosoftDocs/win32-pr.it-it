---
title: funzione glGetColorTableEXT (GL. h)
description: La funzione glGetColorTableEXT ottiene i dati della tabella dei colori della tavolozza della trama di destinazione corrente.
ms.assetid: 9169c4e1-a22e-48fe-bd45-4549c1a10ff0
keywords:
- funzione glGetColorTableEXT OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811dc53b32c937970fbef8d87fa9a2ef4eb8b978
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302761"
---
# <a name="glgetcolortableext-function"></a>glGetColorTableEXT (funzione)

La funzione **glGetColorTableEXT** ottiene i dati della tabella dei colori della tavolozza della trama di destinazione corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGetColorTableEXT(
         GLenum target,
         GLenum format,
         GLenum type,
   const GLvoid *data
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Trama di destinazione per la quale è stata modificata la tavolozza. Deve essere una trama \_ 1D o trama \_ 2D.

</dd> <dt>

*format* 
</dt> <dd>

Formato dei dati pixel. Vengono accettate le seguenti costanti simboliche.



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
<li>La funzione <strong>glGetColorTableEXT</strong> converte i valori a virgola mobile direttamente in un formato interno con precisione non specificata. Per i valori integer con segno viene eseguito il mapping lineare al formato interno, in modo che il valore integer rappresentabile più positivo sia mappato a 1,0 e che il valore integer rappresentabile più negativo sia mappato a-1,0. Viene eseguito il mapping dei dati integer senza segno in modo analogo: il valore integer più grande viene mappato a 1,0 e zero viene mappato a 0,0.</li>
<li>La funzione <strong>glGetColorTableEXT</strong> moltiplica i valori di colore risultanti per GL_c_SCALE e li aggiunge a GL_c_BIAS, dove <em>c</em> è rosso, verde, blu e alfa per i rispettivi componenti di colore. I risultati vengono fissati nell'intervallo [0, 1].</li>
<li>Se GL_MAP_COLOR è <strong>true</strong>, <strong>glGetColorTableEXT</strong> ridimensiona ogni componente del colore in base alla dimensione della tabella di ricerca GL_PIXEL_MAP_c_TO_c, quindi sostituisce il componente in base al valore a cui fa riferimento nella tabella. <em>c</em> è rispettivamente R, G, B o A.</li>
<li>La funzione <strong>glGetColorTableEXT</strong> converte i colori RGBA risultanti in frammenti associando la posizione raster corrente della coordinata z e le coordinate di trama a ogni pixel, quindi assegnando le coordinate della finestra <em>x</em> e <em>y</em> al frammento <em>n</em>, ad esempio <em>x</em>? = <em>larghezza</em> <em>x</em><sub>r</sub> + <em>n</em> mod<br/> <em>y</em>? = <em>y</em><sub>r</sub> + <em>n/Larghezza</em><br/> dove (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) è la posizione raster corrente.<br/></li>
<li>Questi frammenti di pixel vengono quindi trattati come i frammenti generati dalla rasterizzazione di punti, linee o poligoni. La funzione <strong>glGetColorTableEXT</strong> applica il mapping di trama, la nebbia e tutte le operazioni di frammento prima di scrivere i frammenti sul framebuffer.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <dt><strong>GL_RED</strong></dt> </dl></td>
<td>Ogni pixel è un singolo componente rosso.<br/> La funzione <strong>glGetColorTableEXT</strong> converte il componente nel formato interno nello stesso modo in cui il componente rosso di un pixel RGBA è, quindi lo converte in un pixel RGBA con il verde e il blu impostati su 0,0 e Alpha impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt><strong>GL_GREEN</strong></dt> </dl></td>
<td>Ogni pixel è un singolo componente verde.<br/> La funzione <strong>glGetColorTableEXT</strong> converte il componente nel formato interno nello stesso modo in cui il componente verde di un pixel RGBA è e quindi lo converte in un pixel RGBA con il rosso e il blu impostati su 0,0 e Alpha impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt><strong>GL_BLUE</strong></dt> </dl></td>
<td>Ogni pixel è un singolo componente blu.<br/> La funzione <strong>glGetColorTableEXT</strong> converte il componente nel formato interno nello stesso modo in cui il componente blu di un pixel RGBA è e quindi lo converte in un pixel RGBA con rosso e verde impostato su 0,0 e Alpha impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt><strong>GL_ALPHA</strong></dt> </dl></td>
<td>Ogni pixel è un singolo componente alfa.<br/> La funzione <strong>glGetColorTableEXT</strong> converte il componente nel formato interno nello stesso modo in cui il componente alfa di un pixel RGBA è e quindi lo converte in un pixel RGBA con rosso, verde e blu impostato su 0,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt><strong>GL_RGB</strong></dt> </dl></td>
<td>Ogni pixel è un gruppo di tre componenti in questo ordine: rosso, verde, blu.<br/> La funzione <strong>glGetColorTableEXT</strong> converte ogni componente nel formato interno nello stesso modo in cui i componenti rosso, verde e blu di un pixel RGBA sono. Il colore triple viene convertito in un pixel RGBA con Alpha impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt><strong>GL_BGR_EXT</strong></dt> </dl></td>
<td>Ogni pixel è un gruppo di tre componenti in questo ordine: blu, verde, rosso.<br/> GL_BGR_EXT fornisce un formato corrispondente al layout di memoria delle bitmap (DIB) indipendenti dal dispositivo di Microsoft Windows. Quindi, le applicazioni possono usare gli stessi dati con le chiamate di funzione di Windows e le chiamate di funzione pixel OpenGL.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt><strong>GL_BGRA_EXT</strong></dt> </dl></td>
<td>Ogni pixel è un gruppo di quattro componenti in questo ordine: blu, verde, rosso, alfa.<br/> GL_BGRA_EXT fornisce un formato corrispondente al layout di memoria delle bitmap indipendenti dal dispositivo (DIB) Windows. In questo modo, le applicazioni possono usare gli stessi dati con le chiamate di funzione di Windows e le chiamate di funzione pixel OpenGL.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*type* 
</dt> <dd>

Tipo di dati per i *dati*. Di seguito sono riportate le costanti simboliche accettate e i relativi significati.



| Valore                                                                                                                                                                      | Significato                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**\_byte senza segno GL \_**</dt> </dl>    | Intero senza segno a 8 bit<br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**\_byte GL**</dt> </dl>                                | Valore intero con segno a 8 bit<br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**\_short senza segno GL \_**</dt> </dl> | Intero senza segno a 16 bit<br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**\_short GL**</dt> </dl>                             | Valore intero a 16 bit con segno<br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL \_ senza segno \_ int**</dt> </dl>       | Intero senza segno a 32 bit<br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ int**</dt> </dl>                                   | Intero a 32 bit<br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ float**</dt> </dl>                             | Valore a virgola mobile e precisione singola<br/> |



 

</dd> <dt>

*data* 
</dt> <dd>

Punta alla posizione in cui devono essere archiviate le informazioni sulla tabella dei colori restituite. Ogni voce della tabella dei colori viene archiviata come se fosse un singolo pixel di una trama da 1 a D. Poiché tutte le trame hanno una tavolozza predefinita, **glGetColorTableEXT** restituisce sempre le informazioni della tavolozza anche se i dati della trama non sono in un formato con tavolozza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | la *destinazione*, il *formato* o il *tipo* non è un valore accettato.<br/>                                                                   |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glGetColorTableEXT** ottiene i dati effettivi della tabella dei colori specificati da [**glColorTableEXT**](glcolortableext.md) e [**glColorSubTableEXT**](glcolorsubtableext.md).

La funzione **glGetColorTableEXT** è una funzione di estensione che non fa parte della libreria OpenGL standard, ma fa parte dell'estensione di trama di GL \_ ext con \_ tavolozza \_ . Per verificare se l'implementazione di OpenGL supporta **glGetColorTableEXT**, chiamare [**glGetString**](glgetstring.md)(GL \_ Extensions). Se restituisce \_ \_ la trama della tavolozza GL ext \_ , **glGetColorTableEXT** è supportato. Per ottenere l'indirizzo della funzione di una funzione di estensione, chiamare [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                      |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>GL. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glColorSubTableEXT**](glcolorsubtableext.md)
</dt> <dt>

[**glColorTableEXT**](glcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





