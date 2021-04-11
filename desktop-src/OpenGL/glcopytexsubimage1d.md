---
title: funzione glCopyTexSubImage1D (GL. h)
description: La funzione glCopyTexSubImage1D copia un'immagine secondaria di un'immagine di trama unidimensionale dal framebuffer.
ms.assetid: 718aee8a-6dce-49e1-a441-19beccd89f8d
keywords:
- funzione glCopyTexSubImage1D OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64006f9cec7e5fd2f3ca6f860249e579b16dbf10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964452"
---
# <a name="glcopytexsubimage1d-function"></a>glCopyTexSubImage1D (funzione)

La funzione **glCopyTexSubImage1D** copia un'immagine secondaria di un'immagine di trama unidimensionale dal framebuffer.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glCopyTexSubImage1D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   x,
   GLint   y,
   GLsizei width
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Destinazione in cui verranno modificati i dati dell'immagine. Deve avere il valore GL \_ texture \_ 1D.

</dd> <dt>

*level* 
</dt> <dd>

Numero del livello di dettaglio. Il livello 0 è l'immagine di base. Il livello *n* è l'immagine di riduzione del mipmap *n*.

</dd> <dt>

*xoffset* 
</dt> <dd>

Offset Texel all'interno della matrice di trame.

</dd> <dt>

*x* 
</dt> <dd>

Coordinata del piano x della finestra dell'angolo inferiore sinistro della riga di pixel da copiare.

</dd> <dt>

*y* 
</dt> <dd>

Coordinata del piano y della finestra dell'angolo inferiore sinistro della riga di pixel da copiare.

</dd> <dt>

*width* 
</dt> <dd>

Larghezza dell'immagine secondaria dell'immagine della trama. La specifica di un'immagine secondaria della trama con larghezza zero non ha alcun effetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *target* non è un valore accettato.<br/>                                                                                                                                                                               |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | il *livello* è minore di zero o il *livello* è maggiore di *log* 2 (*Max*), dove *Max* è il valore restituito della dimensione della \_ trama GL Max \_ \_ .<br/>                                                                                 |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | *xoffset* è minore del *bordo* o (  +  *larghezza* xoffset) è maggiore di (  +  *bordo* w), dove *w* è la \_ larghezza della trama GL \_ e il *bordo* è il \_ bordo della trama GL \_ . Si noti che *w* include il doppio della larghezza del *bordo* .<br/> |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | la *larghezza* era minore *del bordo* o *y* era minore del *bordo*, dove *Border* è lo spessore del bordo della matrice di trame.<br/>                                                                                            |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La matrice di trama non è stata definita da un'operazione [**glTexImage1D**](glteximage1d.md) precedente.<br/>                                                                                                                   |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>                                                                                        |



## <a name="remarks"></a>Commenti

La funzione **glCopyTexSubImage1D** sostituisce una parte di un'immagine di trama unidimensionale usando i pixel del framebuffer corrente, anziché dalla memoria principale come nel caso di [**glTexSubImage1D**](gltexsubimage1d.md).

Una riga di pixel che inizia con le coordinate della finestra specificate da *x* e *y* e con la *larghezza* della lunghezza sostituisce la parte della matrice di trama con gli indici *xoffset* tramite *xoffset* + (*Width* -1). La destinazione nella matrice di trame non può includere Texel all'esterno della matrice di trama specificata in origine.

La funzione **glCopyTexSubImage1D** elabora i pixel in una riga allo stesso modo di [**glCopyPixels**](glcopypixels.md) , ad eccezione del fatto che prima della conversione finale dei pixel, tutti i valori dei componenti pixel vengono fissati all'intervallo \[ 0, 1 \] e vengono convertiti nel formato interno della trama per l'archiviazione nella matrice di trame. L'ordinamento dei pixel è determinato da coordinate *x* inferiori corrispondenti a coordinate di trama inferiori. Se uno dei pixel all'interno di una riga specificata del framebuffer corrente è esterno alla finestra associata al contesto di rendering corrente, i relativi valori non sono definiti.

Non viene apportata alcuna modifica al parametro *internalFormat*, *Width* o *Border* della matrice di trama specificata o ai valori Texel al di fuori dell'immagine secondaria della trama specificata.

Non è possibile includere chiamate a **glCopyTexSubImage1D** negli elenchi di visualizzazione.

> [!Note]  
> La funzione **glCopyTexSubImage1D** è disponibile solo in OpenGL versione 1,1 o successiva.

 

La texturing non ha alcun effetto sulla modalità di indicizzazione del colore. Le funzioni [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) influiscono sulle immagini della trama esattamente come influiscono sul modo in cui i pixel vengono disegnati usando [**glDrawPixels**](gldrawpixels.md).

Le funzioni seguenti consentono di recuperare informazioni correlate a **glCopyTexSubImage1D**:

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled**](glisenabled.md) con argomento GL \_ texture \_ 1D

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

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glFog**](glfog.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





