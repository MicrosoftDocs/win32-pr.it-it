---
title: Funzione glReadPixels (Gl.h)
description: La funzione glReadPixels legge un blocco di pixel dal framebuffer.
ms.assetid: 41fbad5c-b8ca-456d-bbfc-b48c176e15b0
keywords:
- Funzione glReadPixels OpenGL
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
ms.openlocfilehash: b03a90fcd6ee5179a900739c40e78f796c6340d9609f4cfbeb21e6a70156afe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937941"
---
# <a name="glreadpixels-function"></a>Funzione glReadPixels

La **funzione glReadPixels** legge un blocco di pixel dal framebuffer.

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

Coordinata *x* della finestra del primo pixel letto dal framebuffer. Insieme alla *coordinata y,* specifica la posizione dell'angolo inferiore sinistro di un blocco rettangolare di pixel.

</dd> <dt>

*y* 
</dt> <dd>

Coordinate *y della* finestra del primo pixel letto dal framebuffer. Insieme alla *coordinata x,* specifica la posizione dell'angolo inferiore sinistro di un blocco rettangolare di pixel.

</dd> <dt>

*width* 
</dt> <dd>

Larghezza del rettangolo in pixel.

</dd> <dt>

*height* 
</dt> <dd>

Altezza del rettangolo in pixel. *I* parametri *di larghezza e* altezza del valore "1" corrispondono a un singolo pixel.

</dd> <dt>

*format* 
</dt> <dd>

Formato dei dati pixel. Vengono accettati i valori simbolici seguenti:



| Valore                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**INDICE COLORI \_ GL \_**</dt> </dl>                                                                                                                                                                                                                                                                                                               | Gli indici dei colori vengono letti dal buffer dei colori selezionato da [**glReadBuffer**](glreadbuffer.md). Ogni indice viene convertito in virgola fissa, spostato a sinistra o a destra, a seconda del valore e del segno di GL INDEX SHIFT e aggiunto \_ \_ a GL INDEX \_ \_ OFFSET. Se GL MAP COLOR è GL TRUE, gli indici vengono sostituiti dai relativi mapping nella tabella \_ GL PIXEL MAP I TO \_ \_ \_ \_ \_ \_ \_ I.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_STENCIL_INDEX"></span><span id="gl_stencil_index"></span><dl> <dt>**INDICE \_ DEGLI STENCIL \_ GL**</dt> </dl>                                                                                                                                                                                                                                                                                                         | I valori degli stencil vengono letti dal buffer degli stencil. Ogni indice viene convertito in virgola fissa, spostato a sinistra o a destra, a seconda del valore e del segno di GL INDEX SHIFT e aggiunto \_ \_ a GL INDEX \_ \_ OFFSET. Se GL MAP STENCIL è GL TRUE, gli indici vengono sostituiti dai relativi mapping nella tabella \_ GL PIXEL MAP S TO \_ \_ \_ \_ \_ \_ \_ S.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_DEPTH_COMPONENT"></span><span id="gl_depth_component"></span><dl> <dt>**COMPONENTE DI \_ PROFONDITÀ GL \_**</dt> </dl>                                                                                                                                                                                                                                                                                                   | I valori di profondità vengono letti dal buffer di profondità. Ogni componente viene convertito in virgola mobile in modo che il valore minimo della profondità sia mappato a 0,0 e il valore massimo sia mappato a 1,0. Ogni componente viene quindi moltiplicato per GL DEPTH SCALE, aggiunto a GL DEPTH BIAS e infine aggiunto \_ \_ \_ all'intervallo \_ \[ 0,1. \]<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="GL_RED__GL_GREEN__GL_BLUE__GL_ALPHA__GL_RGB__GL_RGBA__GL_BGR_EXT__GL_BGRA_EXT__GL_LUMINANCE__GL_LUMINANCE_ALPHA"></span><span id="gl_red__gl_green__gl_blue__gl_alpha__gl_rgb__gl_rgba__gl_bgr_ext__gl_bgra_ext__gl_luminance__gl_luminance_alpha"></span><dl> <dt>**GL \_ RED, GL \_ GREEN, GL \_ BLUE, GL \_ ALPHA, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ EXT, GL \_ BGRA \_ EXT, GL \_ LUMINANCE, GL \_ LUMINANCE \_ ALPHA**</dt> </dl> | L'elaborazione varia a seconda che i buffer dei colori archivino gli indici dei colori o i componenti di colore RGBA. Se gli indici dei colori vengono archiviati, vengono letti dal buffer dei colori selezionato [**da glReadBuffer**](glreadbuffer.md). Ogni indice viene convertito in virgola fissa, spostato a sinistra o a destra, a seconda del valore e del segno di GL INDEX SHIFT e aggiunto \_ \_ a GL INDEX \_ \_ OFFSET. Gli indici vengono quindi sostituiti dai valori rosso, verde, blu e alfa ottenuti indicizzando le tabelle GL \_ PIXEL MAP I TO \_ \_ \_ \_ R, GL PIXEL MAP \_ I TO G, GL PIXEL MAP I TO B e \_ GL PIXEL MAP I \_ \_ \_ TO \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ A. Se i componenti di colore RGBA vengono archiviati nei buffer dei colori, vengono letti dal buffer dei colori selezionato da **glReadBuffer**. Ogni componente di colore viene convertito in virgola mobile in modo che l'intensità zero sia mappata a 0,0 e l'intensità completa sia mappata a 1,0. Ogni componente viene quindi moltiplicato per GL c SCALE e aggiunto a GL c BIAS, dove c è \_ \_ GL \_ \_ \_ RED, GL \_ GREEN, GL BLUE e GL \_ \_ ALPHA. Ogni componente è ancorato all'intervallo \[ 0,1. \] Infine, se GL MAP COLOR è GL TRUE, ogni componente di colore c viene sostituito dal relativo mapping nella tabella GL PIXEL MAP c TO c, dove c è ancora \_ \_ GL \_ \_ \_ \_ \_ \_ \_ RED, GL GREEN, GL \_ BLUE \_ \_ e GL ALPHA. Ogni componente viene ridimensionato in base alle dimensioni della tabella corrispondente prima che venga eseguita la ricerca. Infine, i dati non necessario vengono eliminati. Ad esempio, GL RED rimuove i componenti verde, blu e alfa, mentre GL RGB rimuove \_ solo il componente \_ alfa. GL LUMINANCE calcola un singolo valore di componente come somma dei componenti rosso, verde e \_ blu e GL LUMINANCE ALPHA esegue la stessa funzione, mantenendo alfa come \_ \_ secondo valore.<br/> |



 

</dd> <dt>

*type* 
</dt> <dd>

Tipo di dati dei dati pixel. Deve essere uno dei valori seguenti.



| Tipo                | Maschera indice | Conversione dei componenti |
|---------------------|------------|----------------------|
| GL \_ UNSIGNED \_ BYTE  | 281        | (281) *c*             |
| GL \_ BYTE            | 271        | \[(271) *c*-1 \] /2     |
| GL \_ BITMAP          | 1          | 1                    |
| GL \_ UNSIGNED \_ SHORT | 2 61       | (2 61) *c*            |
| GL \_ SHORT           | 2 51       | \[(2 51) *c* 1 \] /2     |
| GL \_ UNSIGNED \_ INT\_ | 2 1       | (2 1) *c*            |
| GL \_ INT             | 2 1      | \[(2 1) *c* 1 \] /2     |
| GL \_ FLOAT           | Nessuno       | *c*                  |



 

</dd> <dt>

*Pixel* 
</dt> <dd>

Restituisce i dati pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *format* o *type* non è un valore accettato.<br/>                                                                              |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | La *larghezza o* *l'altezza* erano negative.<br/>                                                                                   |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | *format* era GL \_ COLOR INDEX e i buffer dei colori \_ archiviati nei componenti a colori RGBA o BGRA.<br/>                                 |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | *il formato* era GL \_ STENCIL INDEX e non \_ esisteva alcun buffer di stencil.<br/>                                                          |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | *il formato* era GL \_ DEPTH COMPONENT e non era presente alcun buffer di \_ profondità.<br/>                                                          |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |

## <a name="remarks"></a>Commenti

La **funzione glReadPixels** restituisce i dati in pixel dal framebuffer, a partire dal pixel il cui angolo inferiore sinistro si trova nella posizione (*x*, *y*), nella memoria client a partire dai pixel *della posizione*. Diversi parametri controllano l'elaborazione dei dati pixel prima di essere inseriti nella memoria client. Questi parametri vengono impostati con tre comandi: [**glPixelStore**](glpixelstore-functions.md), [**glPixelTransfer**](glpixeltransfer.md)e [**glPixelMap**](glpixelmap.md). Questo argomento descrive gli effetti sulla maggior **parte dei glReadPixel,** ma non tutti i parametri specificati da questi tre comandi.

La **funzione glReadPixels** restituisce i valori di ogni pixel con l'angolo inferiore sinistro in corrispondenza di (*x* + i, *y* + j) per 0 = i < *width* e 0 = j < *height*. Si dice che questo pixel sia *l'eesimo* pixel nella *riga j.* I pixel vengono restituiti in ordine di riga dalla riga più bassa alla riga più alta, da sinistra a destra in ogni riga.

I fattori di spostamento, scala, distorsione e ricerca descritti in precedenza sono tutti specificati da [**glPixelTransfer**](glpixeltransfer.md). Il contenuto della tabella di ricerca viene specificato [**da glPixelMap**](glpixelmap.md).

Il passaggio finale prevede la conversione degli indici o dei componenti nel formato corretto, come specificato dal *tipo*. Se *format* è GL COLOR INDEX o GL STENCIL INDEX e type non è GL FLOAT, ogni indice viene mascherato con il valore \_ mask specificato nella tabella \_ \_ \_  \_ seguente. Se *type* è GL \_ FLOAT, ogni indice integer viene convertito in formato a virgola mobile e precisione singola.

Se *format* è GL \_ RED, GL \_ GREEN, GL \_ BLUE, GL \_ ALPHA, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ EXT, GL \_ BGRA \_ EXT, \_ GL LUMINANCE o GL \_ LUMINANCE \_ ALPHA  \_ e il tipo non è GL FLOAT, ogni componente viene moltiplicato per il moltiplicatore illustrato nella tabella precedente. Se type è GL FLOAT, ogni componente viene passato così com'è (o convertito nel formato a virgola mobile a precisione singola del client se è diverso da quello usato \_ da OpenGL).

I valori restituiti vengono inseriti in memoria come indicato di seguito. Se *format* è GL \_ COLOR \_ INDEX, GL STENCIL \_ \_ INDEX, GL DEPTH \_ \_ COMPONENT, GL \_ RED, GL \_ GREEN, GL BLUE, GL ALPHA o GL LUMINANCE, \_ \_ \_      +  viene restituito un singolo valore e i dati per l'eesimo pixel nella riga j th vengono posizionati nella posizione ( j ) width i . GL RGB e GL BGR EXT restituiscono tre \_ valori, GL RGBA e GL BGRA EXT restituiscono quattro valori e GL LUMINANCE ALPHA restituisce due valori per ogni pixel, con tutti i valori corrispondenti a un singolo pixel che occupa lo spazio \_ \_ \_ \_ \_ \_ \_ contiguo in *pixel.* Archiviazione parametri impostati da [**glPixelStore,**](glpixelstore-functions.md)ad esempio GL PACK SWAP BYTES e \_ GL PACK \_ \_ \_ \_ LSB \_ FIRST, influiscono sul modo in cui i dati vengono scritti in memoria. Per [**una descrizione, vedere glPixelStore.**](glpixelstore-functions.md)

I valori per i pixel che si trovano all'esterno della finestra connessa al contesto OpenGL corrente non sono definiti.

Se viene generato un errore, non viene apportata alcuna modifica al contenuto dei *pixel.*

La funzione seguente recupera informazioni correlate a **glReadPixels**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ INDEX \_ MODE

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> </dl>

 

 





