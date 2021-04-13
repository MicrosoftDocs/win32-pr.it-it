---
title: funzione glReadPixels (GL. h)
description: La funzione glReadPixels legge un blocco di pixel dal framebuffer.
ms.assetid: 41fbad5c-b8ca-456d-bbfc-b48c176e15b0
keywords:
- funzione glReadPixels OpenGL
topic_type:
- apiref
api_name:
- glReadPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a853d67be282227168da4b90f4fdd47a49d2d212
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400251"
---
# <a name="glreadpixels-function"></a>glReadPixels (funzione)

La funzione **glReadPixels** legge un blocco di pixel dal framebuffer.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glReadPixels(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLenum  format,
   GLenum  type,
   GLvoid  *pixels
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*x* 
</dt> <dd>

Coordinata *x* della finestra del primo pixel letto dal framebuffer. Insieme alla coordinata *y* , specifica la posizione dell'angolo inferiore sinistro di un blocco rettangolare di pixel.

</dd> <dt>

*y* 
</dt> <dd>

Coordinate della finestra *y* del primo pixel letto dal framebuffer. Insieme alla coordinata *x* , specifica la posizione dell'angolo inferiore sinistro di un blocco rettangolare di pixel.

</dd> <dt>

*width* 
</dt> <dd>

Larghezza del rettangolo pixel.

</dd> <dt>

*height* 
</dt> <dd>

Altezza del rettangolo pixel. I parametri di *larghezza* e *altezza* del valore "1" corrispondono a un singolo pixel.

</dd> <dt>

*format* 
</dt> <dd>

Formato dei dati pixel. Sono accettati i valori simbolici seguenti:



| Valore                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**\_indice colori \_ GL**</dt> </dl>                                                                                                                                                                                                                                                                                                               | Gli indici di colore vengono letti dal buffer dei colori selezionato da [**glReadBuffer**](glreadbuffer.md). Ogni indice viene convertito in un punto fisso, spostato a sinistra o a destra, a seconda del valore e del segno dello \_ spostamento di indice GL \_ e aggiunto all' \_ offset dell'indice GL \_ . Se \_ \_ il colore della mappa GL è GL \_ true, gli indici vengono sostituiti dai relativi mapping nella tabella GL \_ pixel \_ Map \_ i \_ a \_ i.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_STENCIL_INDEX"></span><span id="gl_stencil_index"></span><dl> <dt>**\_indice dello stencil GL \_**</dt> </dl>                                                                                                                                                                                                                                                                                                         | I valori dello stencil vengono letti dal buffer dello stencil. Ogni indice viene convertito in un punto fisso, spostato a sinistra o a destra, a seconda del valore e del segno dello \_ spostamento di indice GL \_ e aggiunto all' \_ offset dell'indice GL \_ . Se \_ \_ lo stencil della mappa GL è GL \_ true, gli indici vengono sostituiti dai relativi mapping nella tabella GL \_ pixel \_ Map \_ s \_ a \_ s.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_DEPTH_COMPONENT"></span><span id="gl_depth_component"></span><dl> <dt>**\_componente profondità \_ GL**</dt> </dl>                                                                                                                                                                                                                                                                                                   | I valori di profondità vengono letti dal buffer di profondità. Ogni componente viene convertito in virgola mobile in modo che il valore di profondità minimo sia mappato a 0,0 e il valore massimo sia mappato a 1,0. Ogni componente viene quindi moltiplicato per la \_ scala di profondità GL \_ , aggiunto \_ alla \_ distorsione della profondità GL e infine fissato all'intervallo compreso tra \[ 0 e 1 \] .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="GL_RED__GL_GREEN__GL_BLUE__GL_ALPHA__GL_RGB__GL_RGBA__GL_BGR_EXT__GL_BGRA_EXT__GL_LUMINANCE__GL_LUMINANCE_ALPHA"></span><span id="gl_red__gl_green__gl_blue__gl_alpha__gl_rgb__gl_rgba__gl_bgr_ext__gl_bgra_ext__gl_luminance__gl_luminance_alpha"></span><dl> <dt>**GL \_ Red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ Luminance, GL \_ Luminance \_ Alpha**</dt> </dl> | L'elaborazione varia a seconda che i buffer dei colori memorizzino gli indici colori o i componenti di colore RGBA. Se gli indici dei colori vengono archiviati, vengono letti dal buffer dei colori selezionato da [**glReadBuffer**](glreadbuffer.md). Ogni indice viene convertito in un punto fisso, spostato a sinistra o a destra, a seconda del valore e del segno dello \_ spostamento di indice GL \_ e aggiunto all' \_ offset dell'indice GL \_ . Gli indici vengono quindi sostituiti dai valori rosso, verde, blu e alfa ottenuti indicizzando la \_ mappa GL pixel da i \_ \_ \_ a \_ R, GL \_ pixel \_ Map \_ i \_ a \_ G, GL \_ pixel \_ Map \_ i \_ a \_ B e GL \_ pixel \_ Map \_ i \_ a \_ una tabella. Se i componenti di colore RGBA vengono archiviati nei buffer dei colori, vengono letti dal buffer dei colori selezionato da **glReadBuffer**. Ogni componente colore viene convertito in virgola mobile in modo tale che l'intensità zero sia mappata a 0,0 e l'intensità completa sia mappata a 1,0. Ogni componente viene quindi moltiplicato per GL \_ c \_ scale e aggiunto alla \_ \_ distorsione GL c, dove c è GL \_ Red, GL \_ Green, GL \_ Blue e GL \_ alpha. Ogni componente viene bloccato nell'intervallo compreso tra \[ 0 e 1 \] . Infine, se \_ \_ il colore della mappa GL è GL \_ true, ogni componente di colore c viene sostituito dal mapping nella tabella GL \_ pixel \_ Map \_ c \_ in \_ c, dove c è di nuovo GL \_ Red, GL \_ Green, GL \_ Blue e GL \_ alpha. Ogni componente viene ridimensionato in base alle dimensioni della tabella corrispondente prima dell'esecuzione della ricerca. Infine, i dati non necessari vengono eliminati. Ad esempio, GL \_ Red ignora i componenti verde, blu e alfa, mentre GL \_ RGB rimuove solo il componente alfa. La \_ luminanza GL calcola un singolo valore di componente come la somma dei componenti rosso, verde e blu, mentre GL \_ Luminance \_ Alpha esegue la stessa operazione mantenendo alfa come secondo valore.<br/> |



 

</dd> <dt>

*type* 
</dt> <dd>

Tipo di dati dei dati pixel. Deve essere uno dei valori seguenti.



| Tipo                | Maschera di indice | Conversione componenti |
|---------------------|------------|----------------------|
| \_byte senza segno GL \_  | 281        | (281) *c*             |
| \_byte GL            | 271        | \[(271) *c*-1 \] /2     |
| \_bitmap GL          | 1          | 1                    |
| \_short senza segno GL \_ | 2 61       | (2 61) *c*            |
| \_short GL           | 2 51       | \[(2 51) *c* 1 \] /2     |
| GL \_ senza segno \_ int\_ | 2 1       | (2 1) *c*            |
| GL \_ int             | 2 1      | \[(2 1) *c* 1 \] /2     |
| GL \_ float           | Nessuno       | *c*                  |



 

</dd> <dt>

*pixel* 
</dt> <dd>

Restituisce i dati in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | il *formato* o il *tipo* non è un valore accettato.<br/>                                                                              |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | La *larghezza* o l' *altezza* è negativa.<br/>                                                                                   |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | *Format* è \_ \_ l'indice dei colori GL e i buffer dei colori archiviati RGBA o BGRA color Components.<br/>                                 |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | il *formato* è l' \_ indice dello stencil GL e non \_ è presente alcun buffer dello stencil.<br/>                                                          |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | il *formato* è \_ il \_ componente di profondità GL e non è presente alcun buffer di profondità.<br/>                                                          |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |

## <a name="remarks"></a>Commenti

La funzione **glReadPixels** restituisce i dati pixel dal framebuffer, a partire dal pixel il cui angolo inferiore sinistro si trova nella posizione (*x*, *y*) nella memoria del client a partire dalla posizione *pixel*. Diversi parametri controllano l'elaborazione dei dati pixel prima che vengano inseriti nella memoria del client. Questi parametri vengono impostati con tre comandi: [**glPixelStore**](glpixelstore-functions.md), [**glPixelTransfer**](glpixeltransfer.md)e [**glPixelMap**](glpixelmap.md). Questo argomento descrive gli effetti su **glReadPixels** della maggior parte, ma non tutti i parametri specificati da questi tre comandi.

La funzione **glReadPixels** restituisce valori da ogni pixel con angolo inferiore sinistro a (*x* + i, *y* + j) per 0 = i < *Width* e 0 = j < *Height*. Questo pixel viene definito il pixel i *th nella* riga *j* th. I pixel vengono restituiti nell'ordine delle righe dalla riga più bassa alla riga più alta, da sinistra a destra in ogni riga.

I fattori Shift, scale, bias e Lookup descritti in precedenza sono tutti specificati da [**glPixelTransfer**](glpixeltransfer.md). Il contenuto della tabella di ricerca viene specificato da [**glPixelMap**](glpixelmap.md).

Il passaggio finale prevede la conversione degli indici o dei componenti nel formato corretto, come specificato dal *tipo*. Se *Format* è GL \_ Color \_ index o GL \_ stencil \_ index e *Type* non è di tipo GL \_ float, ogni indice viene mascherato con il valore della maschera indicato nella tabella seguente. Se *Type* è di tipo GL \_ float, ogni indice Integer viene convertito nel formato a virgola mobile a precisione singola.

Se *Format* è GL \_ Red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ Luminance o GL \_ Luminance \_ Alpha e *Type* non sono GL \_ float, ogni componente viene moltiplicato per il moltiplicatore illustrato nella tabella precedente. Se Type è di tipo GL \_ float, ogni componente viene passato come è o convertito nel formato a virgola mobile a precisione singola del client se è diverso da quello usato da OpenGL.

I valori restituiti vengono inseriti in memoria come indicato di seguito. Se *Format* è \_ l'indice dei colori GL \_ , GL \_ stencil \_ index, GL \_ Depth \_ Component, GL \_ Red, GL \_ Green, GL \_ Blue, GL \_ Alpha o \_ GL Luminance, viene restituito un singolo valore e i dati per il i/o del pixel nella riga *j* si trovano in location (*j* )*Width*  +  *i*. GL \_ RGB e GL \_ BGR \_ ext restituiscono tre valori, GL \_ RGBA e GL \_ BGRA \_ ext restituiscono quattro valori, mentre GL \_ Luminance \_ Alpha restituisce due valori per ogni pixel, con tutti i valori corrispondenti a un singolo pixel che occupa lo spazio contiguo in *pixel*. I parametri di archiviazione impostati da [**glPixelStore**](glpixelstore-functions.md), ad esempio GL \_ pack \_ swap \_ bytes e GL \_ pack \_ LSB \_ , influiscono sulla modalità di scrittura dei dati in memoria. Per una descrizione, vedere [**glPixelStore**](glpixelstore-functions.md) .

I valori per i pixel che si trovano all'esterno della finestra connessa al contesto OpenGL corrente non sono definiti.

Se viene generato un errore, non viene apportata alcuna modifica al contenuto dei *pixel*.

La funzione seguente recupera le informazioni correlate a **glReadPixels**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con \_ modalità Indice GL \_ argomento

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> </dl>

 

 





