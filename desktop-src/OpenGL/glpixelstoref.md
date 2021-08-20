---
title: Funzione glPixelStoref (Gl.h)
description: Imposta le modalità di archiviazione pixel. | Funzione glPixelStoref (Gl.h)
ms.assetid: 8d5055d7-3ea4-40b7-9447-2a005129da58
keywords:
- Funzione glPixelStoref OpenGL
topic_type:
- apiref
api_name:
- glPixelStoref
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 928cf7ccc054a94840e146e0e2ce6a7afdb74f7cde5f59569ec1cf71acbb3dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128081"
---
# <a name="glpixelstoref-function"></a>Funzione glPixelStoref

Imposta le modalità di archiviazione pixel.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPixelStoref(
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Nome simbolico del parametro da impostare. Sei dei parametri di archiviazione influiscono sul modo in cui i dati pixel vengono restituiti alla memoria client e pertanto sono significativi solo per [**i comandi glReadPixels.**](glreadpixels.md) Ecco quali sono:



| Archiviazione Parametro                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GL \_ PACK \_ SWAP \_ BYTES                                       | Se true, l'ordinamento dei byte per i componenti a colori multibyte, i componenti di profondità, gli indici dei colori o gli indici degli stencil viene invertito. Ciò significa che se un componente a quattro byte è costituito da byte *b* 0 , *b* 1 , *b* 2 , *b* 3 , viene archiviato in memoria come *b* 3 , *b* 2 , *b* 1 , *b* 0 se GL PACK SWAP BYTES \_ è \_ \_ true. GL PACK SWAP BYTES non ha effetto sull'ordine di memoria dei componenti all'interno di un pixel, ma solo sull'ordine dei byte all'interno di \_ \_ componenti o \_ indici. Ad esempio, i tre componenti di un pixel in formato RGB GL vengono sempre archiviati con il primo rosso, il secondo verde e il terzo blu, indipendentemente dal valore di \_ GL \_ PACK SWAP \_ \_ BYTES.                                                                                                                                                                                                                                                                                                                                                                                               |
| GL \_ PACK \_ LSB \_ FIRST                                        | Se true, i bit vengono ordinati all'interno di un byte dal meno significativo al più significativo; In caso contrario, il primo bit in ogni byte è il più significativo. Questo parametro è significativo solo per i dati bitmap.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| GL \_ PACK \_ ROW \_ LENGTH                                       | Se maggiore di zero, GL \_ PACK ROW LENGTH definisce il numero di pixel in una \_ \_ riga. Se il primo pixel di una riga viene posizionato nella posizione p in memoria, la posizione del primo pixel della riga successiva viene ottenuta ignorando Equazione che mostra la posizione del primo pixel della riga successiva in ![ GL_PACK_ROW_LENGTH. ](images/pix01.png) \[ Componenti o indici di nuova riga, dove n è il numero di componenti o indici in un pixel, l è il numero di pixel in una riga (gl pack row length if it is greater than zero, the width argument to the pixel routine otherwise), a è il valore di gl pack alignment e s è la \]   \- \- \-  \- \- dimensione, in byte,    <     =  di un singolo componente (se è , è come se fosse un s ). Nel caso di valori a 1 bit, la posizione della riga successiva viene ottenuta ignorando Equazione che mostra la posizione della riga ![ successiva nel GL_PACK_ROW_LENGTH.](images/pix02.png)<br/> componenti o indici. Il componente *della* parola in questa descrizione fa riferimento ai valori non indicizzati rosso, verde, blu, alfa e profondità. Archiviazione formato GL RGB, ad esempio, ha tre componenti per pixel: primo rosso, verde \_ e infine blu.<br/> |
| GL \_ PACK SKIP PIXELS \_ \_ and <br/> GL \_ PACK \_ SKIP \_ ROWS | Questi valori vengono forniti per comodità al programmatore. Non forniscono alcuna funzionalità che non può essere duplicata semplicemente incrementando il puntatore passato [**a glReadPixels**](glreadpixels.md). L'impostazione di GL PACK SKIP PIXELS su i equivale a incrementare il puntatore di i n componenti o indici, dove n è il numero di componenti o indici \_ \_ in ogni \_ pixel.    L'impostazione di GL PACK SKIP ROWS su j equivale all'incremento del puntatore di j k componenti o indici, dove k è il numero di componenti o indici per riga, come calcolato in precedenza nella sezione \_ \_ GL PACK ROW \_    \_ \_ \_ LENGTH.                                                                                                                                                                                                                                                                                                                                                                                                   |
| ALLINEAMENTO DEI PACK GL \_ \_                                         | Specifica i requisiti di allineamento per l'inizio di ogni riga di pixel in memoria. I valori consentiti sono 1 (allineamento byte), 2 (righe allineate a byte pari), 4 (allineamento delle parole) e 8 (le righe iniziano in base ai limiti di due parole).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Gli altri sei parametri di archiviazione influiscono sulla modalità di lettura dei dati pixel dalla memoria client. Questi valori sono significativi per [**glDrawPixels**](gldrawpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glBitmap**](glbitmap.md)e [**glPolygonStipple**](glpolygonstipple.md). Ecco quali sono:



| Archiviazione Parametro                                               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GL \_ UNPACK \_ SWAP \_ BYTES                                         | Se true, l'ordinamento dei byte per i componenti a colori multibyte, i componenti di profondità, gli indici dei colori o gli indici degli stencil viene invertito. Ciò significa che se un componente a quattro byte è costituito da byte *b* 0 , *b* 1 , *b* 2 , *b* 3 , viene archiviato in memoria come *b* 3 , *b* 2 , *b* 1 , *b* 0 se GL \_ UNPACK \_ SWAP BYTES è \_ true. GL UNPACK SWAP BYTES non ha alcun effetto sull'ordine di memoria dei componenti all'interno di un pixel, ma solo sull'ordine dei byte all'interno di \_ \_ componenti o \_ indici. Ad esempio, i tre componenti di un pixel in formato RGB GL vengono sempre archiviati con il primo rosso, il secondo verde e il terzo blu, indipendentemente dal valore di \_ GL \_ UNPACK \_ SWAP \_ BYTES.                                                                                                                                                                                                                                                                                                                                                                                           |
| GL \_ UNPACK \_ LSB \_ FIRST                                          | Se true, i bit vengono ordinati all'interno di un byte dal meno significativo al più significativo; In caso contrario, il primo bit in ogni byte è il più significativo. Questo è significativo solo per i dati bitmap.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| GL \_ UNPACK \_ ROW \_ LENGTH                                         | Se maggiore di zero, GL \_ UNPACK \_ ROW LENGTH definisce il numero di pixel in una \_ riga. Se il primo pixel di una riga viene posizionato nella posizione p in memoria, la posizione del primo pixel della riga successiva viene ottenuta ignorando Equazione che mostra la posizione del primo pixel della riga successiva in ![ GL_UNPACK_ROW_LENGTH. ](images/pix01.png) \[ Componenti o indici di nuova riga, dove n è il numero di componenti o indici in un pixel, l è il numero di pixel in una riga (gl pack row length if it is greater than zero, the width argument to the pixel routine otherwise), a è il valore di gl pack alignment e s è la \]   \- \- \-  \- \- dimensione, in byte,    <     =  di un singolo componente (se è , è come se fosse un s ). Nel caso di valori a 1 bit, la posizione della riga successiva viene ottenuta ignorando Equazione che mostra la posizione della riga ![ successiva nel GL_UNPACK_ROW_LENGTH.](images/pix02.png)<br/> componenti o indici. Il componente *della* parola in questa descrizione fa riferimento ai valori non indicizzati rosso, verde, blu, alfa e profondità. Archiviazione formato GL RGB, ad esempio, ha tre componenti per pixel: primo rosso, verde \_ e infine blu.<br/> |
| GL \_ UNPACK \_ SKIP PIXELS \_ and <br/> GL \_ UNPACK \_ SKIP \_ ROWS | Questi valori vengono forniti per comodità al programmatore. Non forniscono funzionalità che non possono essere duplicate semplicemente incrementando il puntatore passato a [**glDrawPixels**](gldrawpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glBitmap**](glbitmap.md)o [**glPolygonStipple**](glpolygonstipple.md). L'impostazione di GL UNPACK SKIP PIXELS su i equivale a incrementare il puntatore di i n componenti o indici, dove n è il numero di componenti o indici \_ \_ in ogni \_ pixel.    L'impostazione di GL UNPACK SKIP ROWS su j equivale a incrementare il puntatore di j k componenti o indici, dove k è il numero di componenti o indici per riga, come calcolato in precedenza nella \_ \_ sezione GL \_ UNPACK ROW    \_ \_ \_ LENGTH.                                                                                                                                                                                                                                    |
| ALLINEAMENTO \_ DI DECOMPRESSIONE GL \_                                           | Specifica i requisiti di allineamento per l'inizio di ogni riga di pixel in memoria. I valori consentiti sono 1 (allineamento byte), 2 (righe allineate a byte pari), 4 (allineamento delle parole) e 8 (le righe iniziano in base ai limiti di due parole).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*param* 
</dt> <dd>

Valore su cui *è impostato pname.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **glPixelStore** imposta le modalità di archiviazione pixel che influiscono sul funzionamento di [**glDrawPixels**](gldrawpixels.md) e [**glReadPixels**](glreadpixels.md) successivi, nonché la decompressione di modelli di stipple poligoni (vedere [**glPolygonStipple),**](glpolygonstipple.md)bitmap (vedere [**glBitmap)**](glbitmap.md)e modelli di trama (vedere [**glTexImage1D,**](glteximage1d.md) [**glTexImage2D,**](glteximage2d.md) [**glTexSubImage1D**](gltexsubimage1d.md)e [**glTexSubImage2D).**](gltexsubimage2d.md)

La tabella seguente fornisce il tipo, il valore iniziale e l'intervallo di valori validi per ognuno dei parametri di archiviazione che possono essere impostati con **glPixelStore.**



| Pname                    | Tipo    | Valore iniziale | Intervallo valido   |
|--------------------------|---------|---------------|---------------|
| GL \_ PACK \_ SWAP \_ BYTES    | Boolean | false         | true o false |
| GL \_ PACK \_ SWAP \_ BYTES    | Boolean | false         | true o false |
| GL \_ PACK \_ ROW \_ LENGTH    | integer | 0             | \[0,?)        |
| GL \_ PACK \_ SKIP \_ ROWS     | integer | 0             | \[0,?)        |
| GL \_ PACK \_ SKIP \_ PIXELS   | integer | 0             | \[0,?)        |
| ALLINEAMENTO DEI PACK GL \_ \_      | numero intero | 4             | 1, 2, 4 o 8 |
| \_DECOMPRIMERE I \_ BYTE DI SCAMBIO GL \_  | Boolean | false         | true o false |
| GL \_ UNPACK \_ LSB \_ FIRST   | Boolean | false         | true o false |
| GL \_ DECOMPRIMERE \_ LA LUNGHEZZA DELLE \_ RIGHE  | integer | 0             | \[0,?)        |
| GL \_ DECOMPRIMERE \_ LE RIGHE \_ SKIP   | integer | 0             | \[0,?)        |
| GL \_ DECOMPRIMERE \_ I PIXEL \_ IGNORATI | integer | 0             | \[0,?)        |
| ALLINEAMENTO \_ DECOMPRESSIONE GL \_    | numero intero | 4             | 1, 2, 4 o 8 |



 

La **funzione glPixelStoref** può essere usata per impostare qualsiasi parametro dell'archivio pixel. Se il tipo di parametro è booleano e *se param* è 0,0, il parametro è false. in caso contrario, è impostato su true. Se *pname* è un parametro di tipo Integer, *il parametro* viene arrotondato all'intero più vicino.

Analogamente, la **funzione glPixelStorei** può essere usata anche per impostare i parametri dell'archivio pixel. I parametri booleani sono impostati su false se *param* è 0 e true in caso contrario. Il *parametro param* viene convertito in virgola mobile prima di essere assegnato a parametri con valori reali.

Le modalità di archiviazione pixel applicate quando [**glDrawPixels,**](gldrawpixels.md) [**glReadPixels,**](glreadpixels.md) [**glTexImage1D,**](glteximage1d.md) [**glTexImage2D,**](glteximage2d.md) [**glBitmap**](glbitmap.md)o [**glPolygonStipple**](glpolygonstipple.md) vengono inseriti in un elenco di visualizzazione controllano l'interpretazione dei dati di memoria. Le modalità di archiviazione pixel applicate quando viene eseguito un elenco di visualizzazione non sono significative.

Le funzioni seguenti recuperano informazioni correlate **a glPixelStore**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ PACK SWAP \_ \_ BYTES

**glGet con** argomento GL \_ PACK \_ LSB \_ FIRST

**glGet con** argomento GL \_ PACK ROW \_ \_ LENGTH

**glGet con** argomento GL \_ PACK SKIP \_ \_ ROWS

**glGet con** argomento GL \_ PACK SKIP \_ \_ PIXELS

**glGet con** argomento GL \_ PACK \_ ALIGNMENT

**glGet con** argomento GL \_ UNPACK \_ SWAP \_ BYTES

**glGet con** argomento GL \_ UNPACK \_ LSB \_ FIRST

**glGet con** argomento GL \_ UNPACK \_ ROW \_ LENGTH

**glGet con** argomento GL \_ UNPACK \_ SKIP \_ ROWS

**glGet con** argomento GL \_ UNPACK \_ SKIP \_ PIXELS

**glGet con** argomento GL \_ UNPACK \_ ALIGNMENT

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

[**glBitmap**](glbitmap.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPixelZoom**](glpixelzoom.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





