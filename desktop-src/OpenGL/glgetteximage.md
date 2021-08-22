---
title: Funzione glGetTexImage (Gl.h)
description: La funzione glGetTexImage restituisce un'immagine di trama.
ms.assetid: d7235df4-2dd8-4537-aadd-284c130a3f99
keywords:
- Funzione glGetTexImage OpenGL
topic_type:
- apiref
api_name:
- glGetTexImage
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b116bc4ae517d0767d794767ad5232d8537033d62a099a3906f9f2ca96a7166c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493751"
---
# <a name="glgetteximage-function"></a>Funzione glGetTexImage

La **funzione glGetTexImage** restituisce un'immagine di trama.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGetTexImage(
   GLenum target,
   GLint  level,
   GLenum format,
   GLenum type,
   GLvoid *pixels
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Specifica la trama da ottenere. Sono \_ accettati GL TEXTURE \_ 1D e GL \_ TEXTURE \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

Numero di livello di dettaglio dell'immagine desiderata. Il livello 0 è il livello dell'immagine di base. Il *livello n* è *l'esima* immagine di riduzione mipmap.

</dd> <dt>

*format* 
</dt> <dd>

Formato pixel per i dati restituiti. I formati supportati sono GL \_ RED, GL \_ GREEN, GL \_ BLUE, GL \_ ALPHA, GL \_ RGB, GL \_ RGBA, GL \_ LUMINANCE, GL \_ BGR \_ EXT, GL \_ BGRA EXT e GL \_ \_ LUMINANCE \_ ALPHA.

</dd> <dt>

*type* 
</dt> <dd>

Tipo di pixel per i dati restituiti. I tipi supportati sono GL \_ UNSIGNED \_ BYTE, GL \_ BYTE, GL \_ UNSIGNED \_ SHORT, GL \_ SHORT, GL \_ UNSIGNED \_ INT, GL \_ INT e GL \_ FLOAT.

</dd> <dt>

*Pixel* 
</dt> <dd>

Restituisce l'immagine della trama. Deve essere un puntatore a una matrice del tipo specificato dal *tipo*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *target*, *format* o *type* non è un valore accettato.<br/>                                                                    |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *level* è minore di zero o maggiore del *log* 2 (*max*), dove *max* è il valore restituito di GL MAX \_ TEXTURE \_ \_ SIZE.<br/>      |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md) .<br/> |



## <a name="remarks"></a>Commenti

La **funzione glGetTexImage** restituisce un'immagine di trama in *pixel.* Il *parametro di* destinazione specifica se l'immagine della trama desiderata è specificata da [**glTexImage1D**](glteximage1d.md)**(** GL TEXTURE 1D ) o \_ da \_ [**glTexImage2D**](glteximage2d.md)**(** GL TEXTURE \_ \_ 2D **)**. Il *parametro level* specifica il numero di livello di dettaglio dell'immagine desiderata. I *parametri di* formato *e* tipo specificano il formato e il tipo della matrice di immagini desiderata. Per una descrizione dei valori  accettabili rispettivamente per i parametri *di* formato e tipo, vedere **glTexImage1D** e [**glDrawPixels.**](gldrawpixels.md)

Il funzionamento **di glGetTexImage** è più comprensibile considerando l'immagine di trama interna a quattro componenti selezionata come buffer di colore RGBA delle dimensioni dell'immagine.  La semantica di **glGetTexImage** è identica a quella dei [**glReadPixel chiamati**](glreadpixels.md) con lo stesso formato e lo stesso tipo , con *x* e  *y* impostati su *zero,* la larghezza impostata sulla larghezza dell'immagine della trama (incluso il bordo se ne è stato specificato uno) e l'altezza impostata su uno per le immagini 1D o sull'altezza dell'immagine della trama (incluso il bordo, se specificato) per le immagini 2D. 

Poiché l'immagine della trama interna è un'immagine RGBA, i formati di pixel GL COLOR INDEX, GL STENCIL INDEX e GL DEPTH COMPONENT non sono accettati e il tipo di pixel GL BITMAP non \_ \_ è \_ \_ \_ \_ \_ accettato.

Se l'immagine di trama selezionata non contiene quattro componenti, vengono applicati i mapping seguenti. Le trame a componente singolo vengono considerate come buffer RGBA con rosso impostato sul valore a componente singolo e verde, blu e alfa impostati su zero.

Le trame a due componenti vengono considerate come buffer RGBA, con il rosso impostato sul valore del componente zero, il valore alfa impostato sul valore del componente uno e il verde e il blu impostati su zero. Infine, le trame a tre componenti vengono considerate come buffer RGBA con rosso impostato sul componente zero, verde impostato sul componente uno, blu impostato sul componente due e alfa impostato su zero.

Per determinare le dimensioni necessarie per i *pixel,* usare [**glGetTexLevelParameter**](glgettexlevelparameter.md) per verificare le dimensioni dell'immagine di trama interna  e quindi ridimensionare il numero di pixel richiesto dallo spazio di archiviazione necessario per ogni pixel, in base al formato e al *tipo*. Assicurarsi di prendere in considerazione i parametri di archiviazione pixel, in particolare GL \_ PACK \_ ALIGNMENT.

Se viene generato un errore, non viene apportata alcuna modifica al contenuto dei *pixel*.

Le funzioni seguenti recuperano informazioni correlate **a glGetTexImage:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ PACK ALIGNMENT e \_ altri

[**glGetTexLevelParameter con**](glgettexlevelparameter.md) argomento GL \_ TEXTURE \_ WIDTH

**glGetTexLevelParameter con** argomento GL \_ TEXTURE \_ HEIGHT

**glGetTexLevelParameter con** argomento GL \_ TEXTURE \_ BORDER

**glGetTexLevelParameter con** argomento GL \_ TEXTURE \_ COMPONENTS

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

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetTexLevelParameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





