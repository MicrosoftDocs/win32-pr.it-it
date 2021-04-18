---
title: funzione glPixelStorei (GL. h)
description: Imposta le modalità di archiviazione pixel. | funzione glPixelStorei (GL. h)
ms.assetid: 1e1e94e9-aabe-4923-a0a9-f1c041a925ba
keywords:
- funzione glPixelStorei OpenGL
topic_type:
- apiref
api_name:
- glPixelStorei
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00c938d099665daf0578139d28c7497fc4f7debd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104558667"
---
# <a name="glpixelstorei-function"></a>glPixelStorei (funzione)

Imposta le modalità di archiviazione pixel.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPixelStorei(
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pname* 
</dt> <dd>

Nome simbolico del parametro da impostare. Sei parametri di archiviazione influiscono sul modo in cui i dati dei pixel vengono restituiti alla memoria del client e sono pertanto significativi solo per i comandi [**glReadPixels**](glreadpixels.md) . Sono i seguenti.



| Parametro di archiviazione                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_byte di \_ scambio GL Pack \_                                       | Se true, l'ordine dei byte per i componenti di colore multibyte, i componenti di profondità, gli indici dei colori o gli indici degli stencil è invertito Ovvero, se un componente a quattro byte è costituito da byte *b* 0, *b* 1, *b* 2, *b* 3, viene archiviato in memoria come *b* 3, *b* 2, *b* 1, *b* 0 se GL \_ pack \_ swap \_ byte è true. GL \_ pack \_ swap \_ byte non influisce sull'ordine di memoria dei componenti all'interno di un pixel, solo sull'ordine dei byte all'interno di componenti o indici. I tre componenti di un pixel di formato RGB GL, ad esempio, \_ vengono sempre archiviati con il primo rosso, il secondo verde e il terzo blu, indipendentemente dal valore dei \_ byte di scambio GL Pack \_ \_ .                                                                                                                                                                                                                                                                                                                                                                                               |
| \_primo pacchetto per GL Pack \_ LSB \_                                        | Se true, i bit vengono ordinati all'interno di un byte, dal meno significativo al più significativo; in caso contrario, il primo bit in ogni byte è quello più significativo. Questo parametro è significativo solo per i dati bitmap.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| \_ \_ lunghezza riga Pack \_ GL                                       | Se è maggiore di zero, \_ \_ la lunghezza della riga del pacchetto GL \_ definisce il numero di pixel in una riga. Se il primo pixel di una riga viene inserito nella posizione p in memoria, la posizione del primo pixel della riga successiva viene ottenuta ignorando ![ l'equazione che mostra la posizione del primo pixel della riga successiva in GL_PACK_ROW_LENGTH. ](images/pix01.png) \[ \]componenti di nuova riga o indici, dove *n* è il numero di componenti o indici in un pixel, *l* è il numero di pixel in una riga ( \- \- la lunghezza della riga GL Pack \- se è maggiore di zero, l'argomento Width alla routine pixel in caso contrario), *a* è il valore dell'allineamento di GL \- pack \- e *s* è la dimensione, in byte, di un singolo componente (se *a*  <  , è come se fosse  =  ). nel caso di valori a 1 bit, il percorso della riga successiva viene ottenuto ignorando ![ l'equazione che mostra la posizione della riga successiva in GL_PACK_ROW_LENGTH.](images/pix02.png)<br/> componenti o indici. Il *componente* di Word in questa descrizione fa riferimento ai valori di non indice rosso, verde, blu, alfa e profondità. Il formato di archiviazione GL \_ RGB, ad esempio, ha tre componenti per pixel: primo rosso, verde e infine blu.<br/> |
| GL \_ pack- \_ Ignora \_ pixel e <br/> \_ \_ Ignora righe del pacchetto GL \_ | Questi valori vengono forniti per praticità al programmatore; non forniscono funzionalità che non possono essere duplicate semplicemente incrementando il puntatore passato a [**glReadPixels**](glreadpixels.md). \_Se si imposta GL Pack \_ , i pixel vengono ignorati in \_ *i* equivalenti all'incremento del puntatore per *i n* componenti o indici, dove *n* è il numero di componenti o indici in ogni pixel. Impostando GL \_ pack \_ ignorare le \_ righe su *j* è equivalente all'incremento del puntatore per i componenti o gli indici *j k* , dove *k* è il numero di componenti o indici per riga, come calcolato sopra nella \_ \_ sezione relativa alla lunghezza delle righe del pacchetto GL \_ .                                                                                                                                                                                                                                                                                                                                                                                                   |
| \_allineamento GL Pack \_                                         | Specifica i requisiti di allineamento per l'inizio di ogni riga di pixel in memoria. I valori consentiti sono 1 (allineamento dei byte), 2 (righe allineate a byte pari), 4 (allineamento delle parole) e 8 (le righe iniziano con i limiti di doppia parola).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Gli altri sei parametri di archiviazione influiscono sulla modalità di lettura dei dati pixel dalla memoria del client. Questi valori sono significativi per [**glDrawPixels**](gldrawpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glBitmap**](glbitmap.md)e [**glPolygonStipple**](glpolygonstipple.md). Ecco quali sono:



| Parametro di archiviazione                                               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_byte di scambio di DEcomprimere GL \_ \_                                         | Se true, l'ordine dei byte per i componenti di colore multibyte, i componenti di profondità, gli indici dei colori o gli indici degli stencil è invertito Ovvero, se un componente a quattro byte è costituito da byte *b* 0, *b* 1, *b* 2, *b* 3, viene archiviato in memoria come *b* 3, *b* 2, *b* 1, *b* 0 se GL \_ unpack \_ swap \_ bytes è true. GL \_ unpack \_ swap \_ byte non influisce sull'ordine di memoria dei componenti all'interno di un pixel, solo sull'ordine dei byte all'interno di componenti o indici. I tre componenti di un pixel di formato RGB GL, ad esempio, \_ vengono sempre archiviati con il primo rosso, il secondo verde e il terzo blu, indipendentemente dal valore di GL \_ unpack \_ swap \_ bytes.                                                                                                                                                                                                                                                                                                                                                                                           |
| GL \_ decomprime prima il pacchetto \_ LSB \_                                          | Se true, i bit vengono ordinati all'interno di un byte, dal meno significativo al più significativo; in caso contrario, il primo bit in ogni byte è quello più significativo. Questa operazione è significativa solo per i dati bitmap.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_lunghezza di riga DEcomprimere GL \_ \_                                         | Se è maggiore di zero, GL \_ DEcomprimere \_ \_ la lunghezza della riga definisce il numero di pixel in una riga. Se il primo pixel di una riga viene inserito nella posizione p in memoria, la posizione del primo pixel della riga successiva viene ottenuta ignorando ![ l'equazione che mostra la posizione del primo pixel della riga successiva in GL_UNPACK_ROW_LENGTH. ](images/pix01.png) \[ \]componenti di nuova riga o indici, dove *n* è il numero di componenti o indici in un pixel, *l* è il numero di pixel in una riga ( \- \- la lunghezza della riga GL Pack \- se è maggiore di zero, l'argomento Width alla routine pixel in caso contrario), *a* è il valore dell'allineamento di GL \- pack \- e *s* è la dimensione, in byte, di un singolo componente (se *a*  <  , è come se fosse  =  ). nel caso di valori a 1 bit, il percorso della riga successiva viene ottenuto ignorando ![ l'equazione che mostra la posizione della riga successiva in GL_UNPACK_ROW_LENGTH.](images/pix02.png)<br/> componenti o indici. Il *componente* di Word in questa descrizione fa riferimento ai valori di non indice rosso, verde, blu, alfa e profondità. Il formato di archiviazione GL \_ RGB, ad esempio, ha tre componenti per pixel: primo rosso, verde e infine blu.<br/> |
| GL \_ DEcomprimere i \_ \_ pixel Skip e <br/> GL \_ DEcomprimere le \_ righe ignorate \_ | Questi valori vengono forniti per praticità al programmatore; non forniscono funzionalità che non possono essere duplicate semplicemente incrementando il puntatore passato a [**glDrawPixels**](gldrawpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glBitmap**](glbitmap.md)o [**glPolygonStipple**](glpolygonstipple.md). \_Se si imposta GL depack \_ Skip \_ pixel su *i* , equivale a incrementare il puntatore da *i n* componenti o indici, dove *n* è il numero di componenti o indici in ogni pixel. Impostando GL \_ depack \_ ignorare le \_ righe su *j* equivale a incrementare il puntatore per i componenti o gli indici *j k* , dove *k* è il numero di componenti o indici per riga, come calcolato sopra nella \_ sezione GL decomprimere la \_ lunghezza della riga \_ .                                                                                                                                                                                                                                    |
| \_allineamento GL DEcomprimere \_                                           | Specifica i requisiti di allineamento per l'inizio di ogni riga di pixel in memoria. I valori consentiti sono 1 (allineamento dei byte), 2 (righe allineate a byte pari), 4 (allineamento delle parole) e 8 (le righe iniziano con i limiti di doppia parola).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*param* 
</dt> <dd>

Valore su cui è impostato *pname* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **glPixelStore** imposta le modalità di archiviazione dei pixel che influiscono sul funzionamento di [**glDrawPixels**](gldrawpixels.md) e [**glReadPixels**](glreadpixels.md) successivi, nonché sulla decompressione dei modelli poligonali stipple (vedere [**glPolygonStipple**](glpolygonstipple.md)), bitmap (vedere [**glBitmap**](glbitmap.md)) e modelli di trama (vedere [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)e [**glTexSubImage2D**](gltexsubimage2d.md)).

La tabella seguente fornisce il tipo, il valore iniziale e l'intervallo di valori validi per ogni parametro di archiviazione che può essere impostato con **glPixelStore**.



| Pname                    | Tipo    | Valore iniziale | Intervallo valido   |
|--------------------------|---------|---------------|---------------|
| \_byte di \_ scambio GL Pack \_    | Boolean | false         | true o false |
| \_byte di \_ scambio GL Pack \_    | Boolean | false         | true o false |
| \_ \_ lunghezza riga Pack \_ GL    | integer | 0             | \[0,?)        |
| \_ \_ Ignora righe del pacchetto GL \_     | integer | 0             | \[0,?)        |
| GL \_ pack- \_ Ignora \_ pixel   | integer | 0             | \[0,?)        |
| \_allineamento GL Pack \_      | numero intero | 4             | 1, 2, 4 o 8 |
| \_byte di scambio di DEcomprimere GL \_ \_  | Boolean | false         | true o false |
| GL \_ decomprime prima il pacchetto \_ LSB \_   | Boolean | false         | true o false |
| \_lunghezza di riga DEcomprimere GL \_ \_  | integer | 0             | \[0,?)        |
| GL \_ DEcomprimere le \_ righe ignorate \_   | integer | 0             | \[0,?)        |
| \_DEcomprimere GL DEcomprimere i \_ \_ pixel | integer | 0             | \[0,?)        |
| \_allineamento GL DEcomprimere \_    | numero intero | 4             | 1, 2, 4 o 8 |



 

La funzione [**glPixelStoref**](glpixelstoref.md) può essere usata per impostare qualsiasi parametro di archivio pixel. Se il tipo di parametro è booleano e se *param* è 0,0, il parametro è false; in caso contrario, è impostato su true. Se *pname* è un parametro di tipo Integer, *param* viene arrotondato all'intero più vicino.

Analogamente, la funzione **glPixelStorei** può essere usata anche per impostare uno dei parametri dell'archivio pixel. I parametri booleani sono impostati su false se *param* è 0 e true in caso contrario. Il parametro *param* viene convertito in virgola mobile prima di essere assegnato a parametri con valori reali.

Le modalità di archiviazione pixel attive quando [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glBitmap**](glbitmap.md)o [**glPolygonStipple**](glpolygonstipple.md) vengono inserite in un elenco di visualizzazione, controllano l'interpretazione dei dati di memoria. Le modalità di archiviazione pixel attive quando viene eseguito un elenco di visualizzazione non sono significative.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glPixelStore**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Pack di \_ scambio \_ byte

**glGet** con argomento GL \_ pack \_ LSB \_ First

**glGet** con \_ \_ lunghezza riga argomento GL \_ Pack

**glGet** con argomento GL \_ pack \_ ignorare le \_ righe

**glGet** con argomento GL \_ pack \_ Skip \_ pixel

**glGet** con argomento \_ allineamento GL Pack \_

**glGet** con argomento GL \_ decomprimere \_ byte di swap \_

**glGet** con argomento GL \_ decomprimere \_ \_ prima lsb

**glGet** con argomento GL \_ decomprimere la \_ lunghezza delle righe \_

**glGet** con l'argomento GL \_ decomprimere le \_ righe ignorate \_

**glGet** con argomento GL \_ unpack \_ Skip \_ pixel

**glGet** con argomento GL \_ decomprimere l' \_ allineamento

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

[**glBitmap**](glbitmap.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**Remo**](glend.md)
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

 

 





