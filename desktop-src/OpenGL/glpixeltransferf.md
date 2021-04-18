---
title: funzione glPixelTransferf (GL. h)
description: Le funzioni glPixelTransferf e glPixelTransferi impostano le modalità di trasferimento pixel. | funzione glPixelTransferf (GL. h)
ms.assetid: c18ecbb9-af2a-4662-8e3f-0ac850b04fc1
keywords:
- funzione glPixelTransferf OpenGL
topic_type:
- apiref
api_name:
- glPixelTransferf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d6404c9b219b8a27dd3d422bfb85cd45ac8cac
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321406"
---
# <a name="glpixeltransferf-function"></a>glPixelTransferf (funzione)

Le funzioni **glPixelTransferf** e [**glPixelTransferi**](glpixeltransferi.md) impostano le modalità di trasferimento pixel.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPixelTransferf(
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pname* 
</dt> <dd>

Nome simbolico del parametro di trasferimento pixel da impostare. La tabella seguente fornisce il tipo, il valore iniziale e l'intervallo di valori validi per ognuno dei parametri di trasferimento pixel impostati con **glPixelTransfer**.



| Pname             | Tipo    | Valore iniziale  | Intervallo valido  |
|-------------------|---------|----------------|--------------|
| \_colore della mappa GL \_    | Boolean | false          | true/false   |
| \_stencil mappa \_ GL  | Boolean | false          | true/false   |
| \_spostamento indice \_ GL  | integer | 0              | (8, 8)        |
| \_offset indice \_ GL | integer | 0              | (8, 8)        |
| \_scala rossa \_ GL    | numero intero | 1.0            | (8, 8)        |
| \_scala verde \_ GL  | float   | 1.0            | (8, 8)        |
| \_scala GL blu \_   | float   | 1.0            | (8, 8)        |
| \_scala GL Alpha \_  | float   | 1.0            | (8, 8)        |
| \_scala di profondità GL \_  | float   | 1.0            | (8, 8)        |
| \_Bias rosso \_ GL     | float   | 0,0            | (8, 8)        |
| \_bias verde \_ GL   | float   | 0,0            | (8, 8)        |
| \_Bias blu \_ GL    | float   | 0,0            | (8, 8)        |
| \_ \_ distorsione GL Alpha   | float   | 0,0            | (8, 8)        |
| \_Bias profondità \_ GL   | float   | 0,0            | (8, 8)        |



 

</dd> <dt>

*param* 
</dt> <dd>

Valore su cui è impostato *pname* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione glPixelTransfer** imposta le modalità di trasferimento pixel che interessano il funzionamento dei comandi successivi [**glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md) [**, glCopyTexSubImage1D, glCopyTexSubImage2D**](glcopytexsubimage1d.md) [**, glDrawPixels**](glcopytexsubimage2d.md) [**, glReadPixels**](gldrawpixels.md) [**,**](glreadpixels.md) [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)e [**glTexSubImage2D**](gltexsubimage2d.md) . Gli algoritmi specificati dalle modalità di trasferimento dei pixel operano su pixel dopo essere stati letti dal framebuffer (**glReadPixels** e **glCopyPixels**) o decompressi dalla memoria client (**glDrawPixels**, **glTexImage1D** e **glTexImage2D**). Le operazioni di trasferimento pixel si verificano nello stesso ordine e nello stesso modo, indipendentemente dal comando che ha generato l'operazione pixel. Le modalità di archiviazione in pixel ([**glPixelStore**](glpixelstore-functions.md)) controllano la decompressione dei pixel letti dalla memoria del client e la compressione dei pixel riscritti nella memoria del client.

Le operazioni di trasferimento pixel gestiscono quattro tipi di pixel fondamentali: *colore*, *indice colore*, *profondità* e *stencil*. I pixel dei colori sono costituiti da quattro valori a virgola mobile con dimensioni mantissa e esponenti non specificate, ridimensionati in modo che 0,0 rappresenti l'intensità zero e 1,0 rappresenti l'intensità completa. Gli indici dei colori includono un singolo valore a virgola fissa, con una precisione non specificata a destra del punto binario. I pixel di profondità includono un singolo valore a virgola mobile, con dimensioni mantissa e esponenti non specificate, ridimensionato in modo che 0,0 rappresenti il valore del buffer di profondità minimo e 1,0 rappresenta il valore massimo del buffer di profondità. Infine, i pixel dello stencil includono un singolo valore a virgola fissa, con una precisione non specificata a destra del punto binario.

Le operazioni di trasferimento dei pixel eseguite sui quattro tipi di pixel di base sono le seguenti:



| Tipo di pixel  | Operazione di trasferimento pixel                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Colore       | Ognuno dei quattro componenti di colore viene moltiplicato per un fattore di scala e quindi aggiunto a un fattore di distorsione. Ovvero il componente rosso viene moltiplicato per la scala di contabilità di GL \_ \_ , quindi viene aggiunto alla \_ \_ polarizzazione rossa GL; il componente verde viene moltiplicato per la \_ \_ scalabilità verde GL, quindi viene aggiunto alla polarizzazione verde GL, \_ \_ il componente blu viene moltiplicato per la \_ scala GL blu \_ , quindi viene aggiunto alla \_ polarizzazione blu GL e \_ il componente alfa viene moltiplicato per la \_ scala GL Alpha \_ \_ \_ . Quando tutti e quattro i componenti di colore vengono ridimensionati e distorti, ognuno viene bloccato nell'intervallo compreso tra \[ 0 e 1 \] . Tutti i valori della scala dei colori e della distorsione sono specificati con **glPixelTransfer**. <br/> Se il \_ \_ colore della mappa GL è true, ogni componente colore viene ridimensionato in base alla dimensione della mappa da colore a colore corrispondente e quindi sostituito dal contenuto della mappa indicizzata dal componente ridimensionato. Ovvero il componente rosso viene ridimensionato in base alla \_ dimensione del mapping GL pixel \_ \_ r \_ a \_ r \_ e quindi sostituito dal contenuto di GL \_ pixel \_ Map \_ r \_ a \_ r indicizzato da solo. Il componente verde viene ridimensionato in base alle \_ \_ dimensioni della mappa da \_ g a g \_ \_ \_ , quindi sostituito dal contenuto della \_ mappa del pixel GL \_ \_ \_ a \_ g indicizzato da solo. Il componente blu viene ridimensionato in base alle dimensioni del pixel GL da \_ \_ \_ b \_ a \_ b \_ , quindi viene sostituito dal contenuto di GL \_ pixel \_ Map \_ b \_ a \_ b indicizzato da solo. Il componente alfa viene ridimensionato da GL \_ pixel \_ Map a \_ \_ su \_ una \_ dimensione e quindi sostituito dal contenuto di GL \_ pixel map a \_ \_ \_ \_ un oggetto indicizzato da solo. Tutti i componenti presi dalle mappe vengono quindi bloccati nell'intervallo compreso tra \[ 0 e 1 \] . Il \_ colore della mappa GL \_ è specificato con **glPixelTransfer**. Il contenuto delle diverse mappe viene specificato con **glPixelMap**.<br/>                                                                                                                        |
| Indice colori | Ogni indice dei colori viene spostato a sinistra dei \_ bit di spostamento degli indici GL \_ , riempiendo gli zeri di tutti i bit oltre il numero di bit della frazione trasportati dall'indice a virgola fissa. Se \_ \_ il cambio di indice GL è negativo, lo spostamento è a destra, di nuovo riempito con zero. \_ \_ L'offset dell'indice GL viene quindi aggiunto all'indice. GL \_ index \_ Shift e GL \_ \_ offset sono specificati con **glPixelTransfer**.<br/> Da questo punto, l'operazione varia a seconda del formato richiesto dei pixel risultanti. Se i pixel risultanti devono essere scritti in un buffer di indice dei colori o se vengono letti nuovamente nella memoria del client nel formato di \_ \_ Indice dei colori GL, i pixel continuano a essere considerati come indici. Se il \_ \_ colore della mappa GL è true, ogni indice è mascherato da 2 ^ *n* 1, dove *n* è \_ la \_ dimensione della mappa di i pixel GL \_ \_ \_ \_ , quindi sostituito dal contenuto della \_ mappa GL pixel \_ \_ i \_ a \_ indicizzati in base al valore mascherato. Il \_ colore della mappa GL \_ è specificato con **glPixelTransfer**. Il contenuto della mappa dell'indice viene specificato con **glPixelMap**.<br/> Se i pixel risultanti devono essere scritti in un buffer dei colori RGBA o se vengono letti nuovamente nella memoria del client in un formato diverso dall'indice dei \_ colori GL \_ , i pixel vengono convertiti da indici a colori facendo riferimento alle quattro mappe GL \_ pixel \_ mappa \_ i \_ a \_ R, GL \_ pixel \_ mappa \_ i \_ a \_ G, GL \_ pixel \_ Map \_ i \_ a \_ B e GL \_ pixel \_ mappa \_ i \_ a \_ un. Prima di essere dereferenziato, l'indice viene mascherato da 2 n 1, dove n è \_ la \_ mappa GL pixel i a \_ \_ \_ \_ dimensione R per la mappa rossa, GL \_ pixel \_ mappa \_ i \_ a \_ G \_ size per la mappa verde, GL pixel mappa i a B dimensioni per la mappa \_ \_ \_ \_ \_ \_ blu e GL pixel mappa i a \_ \_ \_ \_ \_ una dimensione per la mappa \_ alfa. Tutti i componenti presi dalle mappe vengono quindi bloccati nell'intervallo compreso tra \[ 0 e 1 \] . Il contenuto delle quattro mappe viene specificato con **glPixelMap**.<br/> |
| Profondità       | Ogni valore di profondità viene moltiplicato per la \_ scala di profondità GL \_ , aggiunto alla \_ \_ distorsione della profondità GL e quindi viene premuto per l'intervallo compreso tra \[ 0 e 1 \] .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Stencil     | Ogni indice viene spostato \_ in bit di spostamento dell'indice GL \_ come un indice di colore e quindi aggiunto all' \_ offset dell'indice GL \_ . Se lo \_ stencil della mappa GL \_ è true, ogni indice è mascherato da 2n 1, dove *n* è la \_ mappa dei pixel GL \_ \_ \_ alla dimensione s \_ \_ , quindi sostituito dal contenuto di GL \_ pixel \_ Map \_ s \_ a \_ s indicizzato dal valore mascherato.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

La funzione [**glPixelTransferf**](glpixeltransfer.md) può essere utilizzata per impostare qualsiasi parametro di trasferimento pixel. Se il tipo di parametro è booleano, 0,0 implica false e qualsiasi altro valore implica true. Se *pname* è un parametro Integer, *param* viene arrotondato all'intero più vicino.

Analogamente, è possibile usare **glPixelTransferi** anche per impostare i parametri di trasferimento dei pixel. I parametri booleani sono impostati su false se *param* è 0 e true in caso contrario. Il parametro *param* viene convertito in virgola mobile prima di essere assegnato a parametri con valori reali.

Se un comando [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glCopyPixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md)o [**glTexImage2D**](glteximage2d.md) viene inserito in un elenco di visualizzazione (vedere [**glNewList**](glnewlist.md) e [**glCallList**](glcalllist.md)), le impostazioni della modalità di trasferimento dei pixel attive quando viene *eseguito* l'elenco di visualizzazione sono quelle utilizzate. Potrebbero essere diverse dalle impostazioni durante la compilazione del comando nell'elenco di visualizzazione.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glPixelTransfer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con \_ colore mappa GL \_ argomento

**glGet** con \_ stencil Mappa GL \_ argomento

**glGet** con argomento \_ MAIUSC di indice GL \_

**glGet** con \_ offset indice GL \_ argomento

**glGet** con la \_ scala rossa argomento GL \_

**glGet** con \_ Bias rosso argomento \_ GL

**glGet** con argomento di \_ scala verde GL \_

**glGet** con argomento \_ bias verde \_

**glGet** con argomento con \_ scala GL blu \_

**glGet** con argomento \_ Bias Blue \_ Bias

**glGet** con argomento con \_ scala GL alfa \_

**glGet** con argomento GL \_ Alpha \_ Bias

**glGet** con livello di \_ profondità GL argomento \_

**glGet** con argomento \_ Bias Depth Depth \_

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelZoom**](glpixelzoom.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





