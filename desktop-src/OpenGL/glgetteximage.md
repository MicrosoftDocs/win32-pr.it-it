---
title: funzione glGetTexImage (GL. h)
description: La funzione glGetTexImage restituisce un'immagine di trama.
ms.assetid: d7235df4-2dd8-4537-aadd-284c130a3f99
keywords:
- funzione glGetTexImage OpenGL
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
ms.openlocfilehash: da38ca1d6605fdc3cd6cf73cdd017404b71961e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302500"
---
# <a name="glgetteximage-function"></a>glGetTexImage (funzione)

La funzione **glGetTexImage** restituisce un'immagine di trama.

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

Specifica la trama da ottenere. \_ \_ Viene accettata la trama GL 1D e GL \_ texture \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

Il numero del livello di dettaglio dell'immagine desiderata. Il livello 0 è il livello dell'immagine di base. Il livello *n* è l'immagine di riduzione del mipmap *n*.

</dd> <dt>

*format* 
</dt> <dd>

Formato pixel per i dati restituiti. I formati supportati sono GL \_ Red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ Luminance, GL \_ BGR \_ ext, GL \_ BGRA \_ ext e GL \_ Luminance \_ alpha.

</dd> <dt>

*type* 
</dt> <dd>

Tipo di pixel per i dati restituiti. I tipi supportati sono GL \_ UNsigned \_ byte, GL \_ byte, GL unsigned \_ \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int e GL \_ float.

</dd> <dt>

*pixel* 
</dt> <dd>

Restituisce l'immagine della trama. Deve essere un puntatore a una matrice del tipo specificato dal *tipo*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | la *destinazione*, il *formato* o il *tipo* non è un valore accettato.<br/>                                                                    |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | il *livello* è minore di zero o maggiore di *log* 2 (*Max*), dove *Max* è il valore restituito della \_ dimensione della trama GL Max \_ \_ .<br/>      |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md) .<br/> |



## <a name="remarks"></a>Commenti

La funzione **glGetTexImage** restituisce un'immagine di trama in *pixel*. Il parametro di *destinazione* specifica se l'immagine di trama desiderata è una specificata da [**glTexImage1D**](glteximage1d.md)**(** GL \_ texture \_ 1D **)** o da [**glTexImage2D**](glteximage2d.md)**(** GL \_ trama \_ 2D **)**. Il parametro *Level* specifica il numero del livello di dettaglio dell'immagine desiderata. Il *formato* e i parametri di *tipo* specificano il formato e il tipo della matrice di immagini desiderata. Per una descrizione dei valori accettabili per i parametri *Format* e *Type* , vedere rispettivamente **glTexImage1D** e [**glDrawPixels**](gldrawpixels.md).

Il funzionamento di **glGetTexImage** è ottimale, considerando che l'immagine della trama a quattro componenti interna selezionata è un buffer di colore RGBA dimensioni dell'immagine. La semantica di **glGetTexImage** è quindi identica a quella di [**glReadPixels**](glreadpixels.md) chiamata con lo stesso *formato* e *tipo*, con *x* e *y* impostati su zero, *Width* impostato sulla larghezza dell'immagine della trama (incluso il bordo se ne è stato specificato uno) e *Height* impostato su uno per le immagini 1-d o sull'altezza dell'immagine della trama (incluso il bordo, se ne è stato specificato uno) per le immagini 2D.

Poiché l'immagine di trama interna è un'immagine RGBA, i formati di pixel GL \_ \_ index, GL \_ stencil \_ index e GL \_ Depth \_ Component non vengono accettati e il tipo di pixel \_ bitmap GL non viene accettato.

Se l'immagine di trama selezionata non contiene quattro componenti, vengono applicati i mapping seguenti. Le trame a singolo componente vengono considerate come buffer RGBA con il rosso impostato sul valore del singolo componente, verde, blu e alfa impostati su zero.

Le trame a due componenti vengono considerate come buffer RGBA, con rosso impostato sul valore di Component zero, Alpha impostato sul valore di Component One e verde e blu impostati su zero. Infine, le trame a tre componenti vengono considerate come buffer RGBA con il rosso impostato sul componente zero, il verde impostato sul componente uno, il blu impostato sul componente due e l'alfa impostati su zero.

Per determinare le dimensioni richieste dei *pixel*, usare [**glGetTexLevelParameter**](glgettexlevelparameter.md) per verificare le dimensioni dell'immagine di trama interna, quindi ridimensionare il numero necessario di pixel in base allo spazio di archiviazione necessario per ogni pixel, in base al *formato* e al *tipo*. Assicurarsi di prendere in considerazione i parametri di archiviazione in pixel, in particolare l'allineamento di GL \_ pack \_ .

Se viene generato un errore, non viene apportata alcuna modifica al contenuto dei *pixel*.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glGetTexImage**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ allineamento GL Pack \_ e altri

[**glGetTexLevelParameter**](glgettexlevelparameter.md) con argomento \_ spessore trama \_ GL

**glGetTexLevelParameter** con \_ altezza trama GL \_ argomento

**glGetTexLevelParameter** con \_ bordo trama GL \_ argomento

**glGetTexLevelParameter** con l'argomento \_ componenti di trama GL \_

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

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGetTexLevelParameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





