---
title: funzione glColorTableEXT (GL. h)
description: La funzione glColorTableEXT specifica il formato e le dimensioni di una tavolozza per le trame con tavolozza di destinazione.
ms.assetid: f3d7b1a1-97a5-47ef-a0ca-5e58acb86bb4
keywords:
- funzione glColorTableEXT OpenGL
topic_type:
- apiref
api_name:
- glColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0d5fd5c848e787f480e3e1893b9b25e4bbd3de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742210"
---
# <a name="glcolortableext-function"></a>glColorTableEXT (funzione)

La funzione **glColorTableEXT** specifica il formato e le dimensioni di una tavolozza per le trame con tavolozza di destinazione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glColorTableEXT(
         GLenum  target,
         GLenum  internalFormat,
         GLsizei width,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Trama di destinazione per la quale è stata modificata la tavolozza. Deve essere una trama \_ 1D, una trama \_ 2D, una \_ trama proxy \_ 1D o una trama del proxy \_ \_ 2D.

</dd> <dt>

*internalFormat* 
</dt> <dd>

Il formato interno e la risoluzione della tavolozza. Questo parametro può assumere uno dei seguenti valori simbolici.



| Costante       | Formato di base | Bit R | Bit G | Bit B | Bit |
|----------------|-------------|--------|--------|--------|--------|
| GL \_ R3 \_ G3 \_ B2 | GL \_ RGB     | 3      | 3      | 2      |        |
| \_RGB4 GL       | GL \_ RGB     | 4      | 4      | 4      |        |
| \_RGB5 GL       | GL \_ RGB     | 5      | 5      | 5      |        |
| \_RGB8 GL       | GL \_ RGB     | 8      | 8      | 8      |        |
| \_RGB10 GL      | GL \_ RGB     | 10     | 10     | 10     |        |
| \_RGB12 GL      | GL \_ RGB     | 12     | 12     | 12     |        |
| \_Rgb16 GL      | GL \_ RGB     | 16     | 16     | 16     |        |
| \_RGBA2 GL      | \_RGBA GL    | 2      | 2      | 2      | 2      |
| \_RGBA4 GL      | \_RGBA GL    | 4      | 4      | 4      | 4      |
| GL \_ RGB5 \_ a1   | \_RGBA GL    | 5      | 5      | 5      | 1      |
| \_Rgba8 GL      | \_RGBA GL    | 8      | 8      | 8      | 8      |
| GL \_ RG10 \_ a2   | \_RGBA GL    | 10     | 10     | 10     | 2      |
| \_RGB12 GL      | \_RGBA GL    | 12     | 12     | 12     | 12     |
| \_RGBA16 GL     | \_RGBA GL    | 16     | 16     | 16     | 16     |



 

</dd> <dt>

*width* 
</dt> <dd>

Dimensione della tavolozza. Deve essere 2n = 1 per alcuni numeri interi *n*.

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
<td>Ogni pixel è un gruppo di quattro componenti in questo ordine: rosso, verde, blu, alfa. Il formato RGBA viene determinato in questo modo: <br/>
<ol>
<li>La funzione <strong>glColorTableEXT</strong> converte i valori a virgola mobile direttamente in un formato interno con precisione non specificata. Per i valori integer con segno viene eseguito il mapping lineare al formato interno, in modo che il valore integer rappresentabile più positivo sia mappato a 1,0 e che il valore integer rappresentabile più negativo sia mappato a-1,0. Viene eseguito il mapping dei dati integer senza segno in modo analogo: il valore integer più grande viene mappato a 1,0 e zero viene mappato a 0,0.</li>
<li>La funzione <strong>glColorTableEXT</strong> moltiplica i valori di colore risultanti per GL_c_SCALE e li aggiunge a GL_c_BIAS, dove <em>c</em> è rosso, verde, blu e alfa per i rispettivi componenti di colore. I risultati vengono fissati nell'intervallo [0, 1].</li>
<li>Se GL_MAP_COLOR è <strong>true</strong>, <strong>glColorTableEXT</strong> ridimensiona ogni componente del colore in base alla dimensione della tabella di ricerca GL_PIXEL_MAP_c_TO_c, quindi sostituisce il componente in base al valore a cui fa riferimento nella tabella. <em>c</em> è rispettivamente R, G, B o A.</li>
<li>La funzione <strong>glColorTableEXT</strong> converte i colori RGBA risultanti in frammenti associando <em>la posizione raster</em>corrente e le coordinate della trama a ogni pixel, quindi assegnando le coordinate della finestra <em>x</em> e <em>y</em> al frammento <em>n</em>, ad esempio<em>x</em>? = <em>larghezza</em> <em>x</em><sub>r</sub> + <em>n</em> mod<br/> <em></em>y? = <em>y</em><sub>r</sub> +<em>n/Larghezza</em><br/> dove (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) è la posizione raster corrente.<br/></li>
<li>Questi frammenti di pixel vengono quindi trattati come i frammenti generati dalla rasterizzazione di punti, linee o poligoni. La funzione <strong>glColorTableEXT</strong> applica il mapping di trama, la nebbia e tutte le operazioni di frammento prima di scrivere i frammenti sul framebuffer.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <dt><strong>GL_RED</strong></dt> </dl></td>
<td>Ogni pixel è un singolo componente rosso.<br/> La funzione <strong>glColorTableEXT</strong> converte il componente nel formato interno nello stesso modo in cui il componente rosso di un pixel RGBA è, quindi lo converte in un pixel RGBA con il verde e il blu impostati su 0,0 e Alpha impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt><strong>GL_GREEN</strong></dt> </dl></td>
<td>Ogni pixel è un singolo componente verde.<br/> La funzione <strong>glColorTableEXT</strong> converte il componente nel formato interno nello stesso modo in cui il componente verde di un pixel RGBA è e quindi lo converte in un pixel RGBA con il rosso e il blu impostati su 0,0 e Alpha impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt><strong>GL_BLUE</strong></dt> </dl></td>
<td>Ogni pixel è un singolo componente blu.<br/> La funzione <strong>glColorTableEXT</strong> converte il componente nel formato interno nello stesso modo in cui il componente blu di un pixel RGBA è e quindi lo converte in un pixel RGBA con rosso e verde impostato su 0,0 e Alpha impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt><strong>GL_ALPHA</strong></dt> </dl></td>
<td>Ogni pixel è un singolo componente alfa.<br/> La funzione <strong>glColorTableEXT</strong> converte il componente nel formato interno nello stesso modo in cui il componente alfa di un pixel RGBA è e quindi lo converte in un pixel RGBA con rosso, verde e blu impostato su 0,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt><strong>GL_RGB</strong></dt> </dl></td>
<td>Ogni pixel è un gruppo di tre componenti in questo ordine: rosso, verde, blu.<br/> La funzione <strong>glColorTableEXT</strong> converte ogni componente nel formato interno nello stesso modo in cui i componenti rosso, verde e blu di un pixel RGBA sono. Il colore triple viene convertito in un pixel RGBA con Alpha impostato su 1,0. Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt><strong>GL_BGR_EXT</strong></dt> </dl></td>
<td>Ogni pixel è un gruppo di tre componenti in questo ordine: blu, verde, rosso.<br/> GL_BGR_EXT fornisce un formato corrispondente al layout di memoria delle bitmap indipendenti dal dispositivo (DIB) Windows. In questo modo, le applicazioni possono usare gli stessi dati con le chiamate di funzione di Windows e le chiamate di funzione pixel OpenGL.<br/></td>
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

Tipo di dati per i *dati*. Sono accettate le costanti simboliche seguenti: GL \_ UNsigned \_ byte, GL \_ byte, GL \_ unsigned \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int e GL \_ float.

Nella tabella seguente viene riepilogato il significato delle costanti valide per il parametro di *tipo* .



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

Puntatore ai dati della trama con tavolozza. I dati vengono considerati come singoli pixel di una voce della tavolozza della trama da 1 a D per una voce della tavolozza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | *Width* non è un numero intero valido.<br/>                                                                                            |
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *target*, *internalFormat*, *Format* o *Type* non è un valore accettato.<br/>                                                 |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Le trame con tavolozza sono definite con una tavolozza di colori e un set di dati immagine costituito da indici per le voci di colori di una tavolozza (tabella dei colori).

La funzione **glColorTableEXT** specifica la tavolozza di trama di una trama di destinazione. Preleva i *dati* dalla memoria e li converte come se ogni voce della tavolozza è un singolo pixel di una trama da 1 a D. La funzione **glColorTableEXT** decomprime e converte i dati e li converte in un formato interno che corrisponde al *formato* specificato il più vicino possibile.

Se la *larghezza* della tavolozza è maggiore dell'intervallo degli indici di colore nei dati della trama, alcune voci della tavolozza sono inutilizzate. Se la *larghezza* della tavolozza è inferiore all'intervallo degli indici dei colori nei dati della trama, i bit più significativi dei dati della trama vengono ignorati e viene usato solo il numero appropriato di bit nell'indice quando si accede alla tavolozza. Quando si specifica una *destinazione* proxy usando \_ la trama \_ del proxy 1D \_ o \_ la trama del proxy 2D, la tavolozza della trama del proxy viene ridimensionata e i parametri vengono impostati, ma non viene eseguito il trasferimento o l'accesso ai dati.

Quando il parametro di *destinazione* è GL \_ proxy \_ texture \_ 1D o \_ GL proxy \_ texture \_ 2D e l'implementazione non supporta i valori specificati per il *formato* o la *larghezza*, **glColorTableEXT** può non essere in grado di creare la tabella dei colori richiesta. In questo caso, la tabella dei colori è vuota e tutti i parametri recuperati saranno pari a zero. È possibile determinare se OpenGL supporta un formato e una dimensione della tabella dei colori specifici chiamando **glColorTableEXT** con una destinazione proxy e quindi chiamando [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) o [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) per determinare se il parametro width corrisponde a quello impostato da **glColorTableEXT**. Se la larghezza recuperata è zero, la richiesta della tabella dei colori di **glColorTable** non è riuscita. Se la larghezza recuperata è diversa da zero, è possibile chiamare **glColorTable** con la destinazione reale con trama \_ 1D o trama \_ 2D per impostare la tabella dei colori.

> [!Note]  
> La funzione **glColorTableEXT** è una funzione di estensione che non fa parte della libreria OpenGL standard, ma fa parte dell'estensione di trama di GL \_ ext con \_ tavolozza \_ . Per verificare se l'implementazione di OpenGL supporta **glColorTableEXT**, chiamare [**glGetString**](glgetstring.md)(GL \_ Extensions). Se restituisce \_ \_ la trama della tavolozza GL ext \_ , **glColorTableEXT** è supportato. Per ottenere l'indirizzo della funzione di una funzione di estensione, chiamare [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).

 

Per recuperare i dati effettivi della tabella dei colori specificati dalla funzione **glColorTableEXT** , chiamare [**glGetColorTableEXT**](glgetcolortableext.md). Per recuperare i parametri, ad esempio *Width* e *Format*, della tabella dei colori specificata dalla funzione **GlColorTableEXT** , chiamare la funzione **glGetColorTableParameterivEXT** o **glGetColorTableParameterfvEXT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                      |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>GL. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorSubTableEXT**](glcolorsubtableext.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGetColorTableEXT**](glgetcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





