---
title: Funzione glCopyTexSubImage1D (Gl.h)
description: La funzione glCopyTexSubImage1D copia un'immagine secondaria di un'immagine di trama unidimensionale dal framebuffer.
ms.assetid: 718aee8a-6dce-49e1-a441-19beccd89f8d
keywords:
- Funzione openGL glCopyTexSubImage1D
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
ms.openlocfilehash: 38c35e28a37608ebbbdbaf331e2837f83022768cf4eb4033cad2a482d477b37f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118617136"
---
# <a name="glcopytexsubimage1d-function"></a>Funzione glCopyTexSubImage1D

La **funzione glCopyTexSubImage1D** copia un'immagine secondaria di un'immagine di trama unidimensionale dal framebuffer.

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

Destinazione in cui verranno modificati i dati dell'immagine. Deve avere il valore GL \_ TEXTURE \_ 1D.

</dd> <dt>

*level* 
</dt> <dd>

Numero di livello di dettaglio. Il livello 0 è l'immagine di base. Il *livello n* è *l'esima* immagine di riduzione mipmap.

</dd> <dt>

*xoffset* 
</dt> <dd>

Offset texel all'interno della matrice di trame.

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

Larghezza dell'immagine secondaria dell'immagine della trama. La specifica di un'immagine secondaria di trama con larghezza zero non ha alcun effetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *target* non è un valore accettato.<br/>                                                                                                                                                                               |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *level* è minore di zero o *level* è maggiore del *log* 2(*max*), dove *max* è il valore restituito di GL MAX \_ TEXTURE \_ \_ SIZE.<br/>                                                                                 |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *xoffset è* minore di *border* o (*xoffset* width ) è maggiore di ( w border ), dove w è GL TEXTURE WIDTH e  +    +  border è  GL TEXTURE \_ \_  \_ \_ BORDER. Si noti *che w* include il doppio dello *spessore del* bordo.<br/> |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *width* è minore di *border o* *y* è minore di *border*, dove *border* è la larghezza del bordo della matrice di trame.<br/>                                                                                            |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La matrice di trame non è stata definita da [**un'operazione glTexImage1D**](glteximage1d.md) precedente.<br/>                                                                                                                   |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>                                                                                        |



## <a name="remarks"></a>Commenti

La **funzione glCopyTexSubImage1D** sostituisce una parte di un'immagine di trama unidimensionale usando i pixel del framebuffer corrente, anziché dalla memoria principale, come nel caso di [**glTexSubImage1D.**](gltexsubimage1d.md)

Una riga di pixel che inizia con le coordinate  della finestra specificate da *x* e *y* e con la larghezza della lunghezza sostituisce la parte della matrice di trame con gli indici *da xoffset* a *xoffset* + (*width* - 1). La destinazione nella matrice di trame non può includere texel esterni alla matrice di trame specificata in origine.

La funzione **glCopyTexSubImage1D** elabora i pixel di una riga nello stesso modo di [**glCopyPixels,**](glcopypixels.md) ad eccezione del fatto che prima della conversione finale dei pixel tutti i valori dei componenti pixel vengono bloccati \[ nell'intervallo 0,1 e convertiti nel formato interno della trama per \] l'archiviazione nella matrice di trame. L'ordinamento dei pixel viene determinato con *le coordinate x* inferiori corrispondenti alle coordinate della trama inferiori. Se uno dei pixel all'interno di una riga specificata del framebuffer corrente si trova all'esterno della finestra associata al contesto di rendering corrente, i relativi valori non sono definiti.

Non viene apportata alcuna modifica al parametro *internalFormat,* *width* o *border* della matrice di trama specificata o ai valori texel all'esterno della sotto-immagine di trama specificata.

Non è possibile includere chiamate a **glCopyTexSubImage1D** negli elenchi di visualizzazione.

> [!Note]  
> La **funzione glCopyTexSubImage1D** è disponibile solo in OpenGL versione 1.1 o successiva.

 

La colorazione non ha alcun effetto in modalità color-index. Le [**funzioni glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) influiscono sulle immagini di trama esattamente nel modo in cui influiscono sul modo in cui i pixel vengono disegnati usando [**glDrawPixels**](gldrawpixels.md).

Le funzioni seguenti recuperano informazioni correlate a **glCopyTexSubImage1D:**

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled con**](glisenabled.md) argomento GL \_ TEXTURE \_ 1D

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

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
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

 

 





