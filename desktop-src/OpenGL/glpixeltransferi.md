---
title: Funzione glPixelTransferi (Gl.h)
description: Le funzioni glPixelTransferf e glPixelTransferi impostano le modalità di trasferimento pixel. | Funzione glPixelTransferi (Gl.h)
ms.assetid: 351a872d-2cce-4fb1-b736-72201baf4157
keywords:
- Funzione glPixelTransferi OpenGL
topic_type:
- apiref
api_name:
- glPixelTransferi
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a2aa93fdcf0fd86975c433fca88310171986aea9edb6a00d9db8f569db02e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132910"
---
# <a name="glpixeltransferi-function"></a>Funzione glPixelTransferi

Le [**funzioni glPixelTransferf**](glpixeltransferf.md) **e glPixelTransferi** impostano le modalità di trasferimento pixel.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPixelTransferi(
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Nome simbolico del parametro di trasferimento pixel da impostare. Nella tabella seguente vengono forniti il tipo, il valore iniziale e l'intervallo di valori validi per ognuno dei parametri di trasferimento pixel impostati con **glPixelTransfer**.



| Pname             | Tipo    | Valore iniziale  | Intervallo valido  |
|-------------------|---------|----------------|--------------|
| COLORE \_ MAPPA GL \_    | Boolean | false          | true/false   |
| STENCIL MAPPA GL \_ \_  | Boolean | false          | true/false   |
| SPOSTAMENTO \_ \_ DELL'INDICE GL  | integer | 0              | (8,8)        |
| OFFSET \_ \_ DELL'INDICE GL | integer | 0              | (8,8)        |
| GL \_ RED \_ SCALE    | numero intero | 1.0            | (8,8)        |
| GL \_ GREEN \_ SCALE  | float   | 1.0            | (8,8)        |
| GL \_ BLUE \_ SCALE   | float   | 1.0            | (8,8)        |
| GL \_ ALPHA \_ SCALE  | float   | 1.0            | (8,8)        |
| GL \_ DEPTH \_ SCALE  | float   | 1.0            | (8,8)        |
| DISTORSIONE ROSSO GL \_ \_     | float   | 0,0            | (8,8)        |
| DISTORSIONE VERDE GL \_ \_   | float   | 0,0            | (8,8)        |
| DISTORSIONE BLU GL \_ \_    | float   | 0,0            | (8,8)        |
| DISTORSIONE \_ ALFA GL \_   | float   | 0,0            | (8,8)        |
| DISTORSIONE \_ DELLA PROFONDITÀ GL \_   | float   | 0,0            | (8,8)        |



 

</dd> <dt>

*param* 
</dt> <dd>

Valore su cui *è impostato pname.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **glPixelTransfer** imposta le modalità di trasferimento pixel che influiscono sul funzionamento dei comandi [**glCopyPixels,**](glcopypixels.md) [**glCopyTexImage1D,**](glcopyteximage1d.md) [**glCopyTexImage2D,**](glcopyteximage2d.md) [**glCopyTexSubImage1D,**](glcopytexsubimage1d.md) [**glCopyTexSubImage2D,**](glcopytexsubimage2d.md) [**glDrawPixels,**](gldrawpixels.md) [**glReadPixels,**](glreadpixels.md) [**glTexImage1D,**](glteximage1d.md) [**glTexImage2D,**](glteximage2d.md) [**glTexSubImage1D**](gltexsubimage1d.md)e [**glTexSubImage2D.**](gltexsubimage2d.md) Gli algoritmi specificati dalle modalità di trasferimento pixel operano sui pixel dopo la lettura dal framebuffer (**glReadPixels** e **glCopyPixels**) o decompressi dalla memoria client (**glDrawPixels**, **glTexImage1D** e **glTexImage2D**). Le operazioni di trasferimento dei pixel vengono eseguite nello stesso ordine e nello stesso modo, indipendentemente dal comando che ha comportato l'operazione sui pixel. Le modalità di archiviazione pixel ([**glPixelStore**](glpixelstore-functions.md)) controllano la decompressione dei pixel letti dalla memoria client e la creazione di un pacchetto di pixel scritti nella memoria client.

Le operazioni di trasferimento dei pixel gestiscono quattro tipi di pixel fondamentali: *colore,* indice *colori,* *profondità* e *stencil.* I pixel di colore sono formati da quattro valori a virgola mobile con dimensioni mantissa ed esponenti non specificati, ridimensionati in modo che 0,0 rappresenti l'intensità zero e 1,0 rappresenta l'intensità completa. Gli indici dei colori comprendono un singolo valore a virgola fissa, con precisione non specificata a destra del punto binario. I pixel di profondità comprendono un singolo valore a virgola mobile, con dimensioni mantissa ed esponenti non specifiche, ridimensionati in modo che 0,0 rappresenti il valore minimo del buffer di profondità e 1,0 rappresenta il valore massimo del buffer di profondità. Infine, i pixel degli stencil comprendono un singolo valore a virgola fissa, con una precisione non specificata a destra del punto binario.

Le operazioni di trasferimento dei pixel eseguite sui quattro tipi di pixel di base sono le seguenti:



| Tipo di pixel  | Operazione di trasferimento dei pixel                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Color       | Ognuno dei quattro componenti di colore viene moltiplicato per un fattore di scala e quindi aggiunto a un fattore di distorsione. Ciò significa che il componente rosso viene moltiplicato per GL RED SCALE e quindi aggiunto a GL RED BIAS; il componente verde viene moltiplicato per GL GREEN SCALE e quindi aggiunto a GL GREEN BIAS; il componente blu viene moltiplicato per GL BLUE SCALE e quindi aggiunto a GL BLUE BIAS e il componente alfa viene moltiplicato per GL ALPHA SCALE e quindi aggiunto a \_ \_ GL \_ \_ \_ ALPHA \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ BIAS. Dopo che tutti e quattro i componenti di colore sono stati ridimensionati e distorti, ognuno di essi è ancorato all'intervallo \[ 0,1. \] Tutti i valori di scala dei colori e distorsione vengono specificati **con glPixelTransfer**. <br/> Se GL MAP COLOR è true, ogni componente di colore viene ridimensionato in base alle dimensioni della mappa \_ color-to-color corrispondente e quindi sostituito dal contenuto della mappa indicizzata dal componente \_ ridimensionato. Ciò significa che il componente rosso viene ridimensionato da GL PIXEL MAP R TO R SIZE e quindi sostituito dal contenuto di GL PIXEL MAP R TO R indicizzato \_ \_ \_ da \_ \_ \_ \_ \_ \_ \_ \_ solo. Il componente verde viene ridimensionato da GL PIXEL MAP G TO G SIZE e quindi sostituito dal contenuto di \_ GL PIXEL MAP G \_ TO G \_ \_ \_ \_ \_ \_ \_ \_ \_ indicizzato da solo. Il componente blu viene ridimensionato da GL PIXEL MAP B TO B SIZE e quindi sostituito dal contenuto di \_ GL PIXEL MAP B \_ TO B \_ \_ \_ \_ \_ \_ \_ \_ \_ indicizzato da solo. Il componente alfa viene ridimensionato da GL PIXEL MAP A TO A SIZE e quindi sostituito dal contenuto di \_ GL PIXEL MAP A \_ TO A \_ \_ \_ \_ \_ \_ \_ \_ \_ indicizzato da solo. Tutti i componenti presi dalle mappe vengono quindi ancorati all'intervallo \[ 0,1. \] GL \_ MAP COLOR viene specificato con \_ **glPixelTransfer**. Il contenuto delle varie mappe viene specificato con **glPixelMap**.<br/>                                                                                                                        |
| Indice colori | Ogni indice colori viene spostato a sinistra dei bit GL INDEX SHIFT, riempiendo con zeri qualsiasi bit oltre il numero di bit frazionari trasportati dall'indice \_ \_ a virgola fissa. Se GL \_ INDEX \_ SHIFT è negativo, lo spostamento si trova a destra, di nuovo con riempimento zero. GL \_ INDEX OFFSET viene quindi aggiunto \_ all'indice. GL \_ INDEX SHIFT e GL INDEX OFFSET vengono specificati con \_ \_ \_ **glPixelTransfer**.<br/> Da questo punto, l'operazione diverge a seconda del formato richiesto dei pixel risultanti. Se i pixel risultanti devono essere scritti in un index buffer di colori o se vengono letti nella memoria client nel formato GL COLOR INDEX, i pixel continuano a essere considerati come \_ \_ indici. Se GL MAP COLOR è true, ogni indice viene mascherato da \_ \_ 2 ^ *n* 1, dove *n* è GL PIXEL MAP I TO I SIZE e quindi sostituito dal contenuto di GL PIXEL MAP I TO I indicizzato dal valore \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ mascherato. GL \_ MAP COLOR viene specificato con \_ **glPixelTransfer.** Il contenuto della mappa dell'indice viene specificato **con glPixelMap.**<br/> Se i pixel risultanti devono essere scritti in un buffer dei colori RGBA o se vengono letti nella memoria client in un formato diverso da GL COLOR INDEX, i pixel vengono convertiti da indici in colori facendo riferimento alle quattro mappe \_ GL PIXEL MAP I TO \_ \_ \_ \_ \_ \_ R, GL PIXEL MAP I TO G, GL PIXEL MAP I TO B e \_ GL \_ PIXEL MAP I \_ \_ TO \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ A. Prima di essere dereferenziato, l'indice viene mascherato da 2 n 1, dove n è GL PIXEL MAP I TO R SIZE per la mappa rossa, GL PIXEL MAP I TO G SIZE per la mappa \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ verde, GL PIXEL MAP I TO B \_ \_ \_ \_ \_ \_ \_ SIZE \_ \_ \_ \_ \_ \_ per la mappa blu e GL PIXEL MAP I TO A SIZE per la mappa alfa. Tutti i componenti prelevati dalle mappe vengono quindi definiti nell'intervallo \[ 0,1. \] Il contenuto delle quattro mappe viene specificato con **glPixelMap.**<br/> |
| Profondità       | Ogni valore di profondità viene moltiplicato per GL DEPTH SCALE, aggiunto a GL DEPTH BIAS e quindi impostato \_ \_ \_ sull'intervallo \_ \[ 0,1. \]                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Stencil     | Ogni indice viene spostato in bit GL INDEX SHIFT esattamente come un indice di colore e quindi \_ aggiunto a GL INDEX \_ \_ \_ OFFSET. Se GL MAP STENCIL è true, ogni indice viene mascherato da \_ \_ 2n 1, dove *n* è GL PIXEL MAP S TO S SIZE, quindi sostituito dal contenuto di GL PIXEL MAP S TO S indicizzato dal valore \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ mascherato.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

La [**funzione glPixelTransferf**](glpixeltransfer.md) può essere usata per impostare qualsiasi parametro di trasferimento pixel. Se il tipo di parametro è booleano, 0,0 implica false e qualsiasi altro valore implica true. Se *pname* è un parametro integer, *il parametro* viene arrotondato all'intero più vicino.

Analogamente, **glPixelTransferi** può essere usato anche per impostare i parametri di trasferimento pixel. I parametri booleani sono impostati su false se *param* è 0 e true in caso contrario. Il *parametro param* viene convertito in virgola mobile prima di essere assegnato a parametri con valori reali.

Se un comando [**glDrawPixels,**](gldrawpixels.md) [**glReadPixels**](glreadpixels.md), [**glCopyPixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md)o [**glTexImage2D**](glteximage2d.md) viene inserito in un elenco di visualizzazione (vedere [**glNewList**](glnewlist.md) e [**glCallList**](glcalllist.md)), le impostazioni della modalità di trasferimento pixel applicate quando viene eseguito l'elenco di visualizzazione sono quelle usate.  Possono essere diverse dalle impostazioni quando il comando è stato compilato nell'elenco di visualizzazione.

Le funzioni seguenti recuperano informazioni correlate **a glPixelTransfer:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ MAP \_ COLOR

**glGet** con argomento GL \_ MAP \_ STENCIL

**glGet** con argomento GL \_ INDEX \_ SHIFT

**glGet** con argomento GL \_ INDEX \_ OFFSET

**glGet** con argomento GL \_ RED \_ SCALE

**glGet** con argomento GL \_ RED \_ BIAS

**glGet** con argomento GL \_ GREEN \_ SCALE

**glGet** con argomento GL \_ GREEN \_ BIAS

**glGet con** argomento GL \_ BLUE \_ SCALE

**glGet** con argomento GL \_ BLUE \_ BIAS

**glGet con** argomento GL \_ ALPHA \_ SCALE

**glGet con** argomento GL \_ ALPHA \_ BIAS

**glGet con** argomento GL \_ DEPTH \_ SCALE

**glGet** con argomento GL \_ DEPTH \_ BIAS

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
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

 

 





