---
title: Funzione glCopyTexSubImage2D (Gl.h)
description: La funzione glCopyTexSubImage2D copia un'immagine secondaria di un'immagine di trama bidimensionale dal framebuffer.
ms.assetid: cbb644d4-6a23-4d66-8599-5f8b48e9b91f
keywords:
- Funzione openGL glCopyTexSubImage2D
topic_type:
- apiref
api_name:
- glCopyTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2a6a5dbf175408ba8421a28e9ee7b7b80876849701b849935a3a4aba9b13e8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118617057"
---
# <a name="glcopytexsubimage2d-function"></a>Funzione glCopyTexSubImage2D

La **funzione glCopyTexSubImage2D** copia un'immagine secondaria di un'immagine di trama bidimensionale dal framebuffer.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glCopyTexSubImage2D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   yoffset,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Destinazione in cui verranno modificati i dati dell'immagine. Deve avere il valore GL \_ TEXTURE \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

Numero di livello di dettaglio. Il livello 0 è l'immagine di base. Il *livello n* è *l'esima* immagine di riduzione mipmap.

</dd> <dt>

*xoffset* 
</dt> <dd>

Offset del texel nella *direzione x* all'interno della matrice di trame.

</dd> <dt>

*yoffset* 
</dt> <dd>

Offset del texel nella *direzione y* all'interno della matrice di trame.

</dd> <dt>

*x* 
</dt> <dd>

Coordinate del piano x della finestra dell'angolo inferiore sinistro della riga di pixel da copiare.

</dd> <dt>

*y* 
</dt> <dd>

Coordinate del piano y della finestra dell'angolo inferiore sinistro della riga di pixel da copiare.

</dd> <dt>

*width* 
</dt> <dd>

Larghezza dell'immagine secondaria dell'immagine della trama. La specifica di un'immagine secondaria di trama con larghezza zero non ha alcun effetto.

</dd> <dt>

*height* 
</dt> <dd>

Altezza dell'immagine secondaria dell'immagine della trama. La specifica di un'immagine secondaria di trama con larghezza zero non ha alcun effetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *target* non è un valore accettato.<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *level* è minore di zero o maggiore del *log* 2 (*max*), dove *max* è il valore restituito di GL MAX \_ TEXTURE \_ \_ SIZE.<br/>                                                                                                                                                                                          |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *xoffset* è minore di *border* o (*xoffset* width ) è maggiore di (  +  *w*  +  *border*), *yoffset*   +    +    \_ \_  è \_ \_ minore di border oppure ( yoffset height ) è maggiore di ( h border ), dove w è GL TEXTURE WIDTH e border è GL TEXTURE BORDER. Si noti *che w* include il doppio dello *spessore del* bordo.<br/> |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *width* è minore di *border o* *y* è minore di *border*, dove *border* è la larghezza del bordo della matrice di trame.<br/>                                                                                                                                                                                           |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La matrice di trame non è stata definita da [**un'operazione glTexImage1D**](glteximage1d.md) precedente.<br/>                                                                                                                                                                                                                  |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>                                                                                                                                                                                       |



## <a name="remarks"></a>Commenti

La **funzione glCopyTexSubImage2D** sostituisce una parte rettangolare di un'immagine di trama bidimensionale con pixel del framebuffer corrente, anziché dalla memoria principale, come nel caso di [**glTexSubImage2D.**](gltexsubimage2d.md)

Un rettangolo di pixel che inizia con le  coordinate  della finestra *x* e *y* e con le dimensioni larghezza e altezza sostituisce la parte della matrice di trame con gli indici xoffset attraverso *xoffset* + (*width* - 1), con gli indici *yoffset* attraverso *yoffset* + (*width* - 1) al livello mipmap specificato da *level*.  Il rettangolo di destinazione nella matrice di trame non può includere texel esterni alla matrice di trame specificata in origine.

La funzione **glCopyTexSubImage2D** elabora i pixel di una riga nello stesso modo di [**glCopyPixels**](glcopypixels.md), ad eccezione del fatto che prima della conversione finale dei pixel, tutti i valori dei componenti pixel vengono bloccati \[ nell'intervallo 0,1 e convertiti nel formato interno della trama per \] l'archiviazione nella matrice di trame. L'ordinamento dei pixel viene determinato con *le coordinate x* inferiori corrispondenti alle coordinate della trama inferiori. Se uno dei pixel all'interno di una riga specificata del framebuffer corrente si trova all'esterno della finestra associata al contesto di rendering corrente, i relativi valori non sono definiti.

Se uno dei pixel all'interno del rettangolo specificato del framebuffer corrente si trova all'esterno della finestra di lettura associata al contesto di rendering corrente, i valori ottenuti per tali pixel non sono definiti. Non viene apportata alcuna modifica al parametro *internalFormat,* *width,* *height* o *border* della matrice di trame specificata o ai valori texel all'esterno dell'immagine secondaria di trama specificata.

Non è possibile includere chiamate a **glCopyTexSubImage2D** negli elenchi di visualizzazione.

> [!Note]  
> La **funzione glCopyTexSubImage2D** è disponibile solo in OpenGL versione 1.1 o successiva.

 

La colorazione non ha alcun effetto in modalità color-index. Le [**funzioni glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) influiscono sulle immagini di trama esattamente nel modo in cui influiscono sul modo in cui i pixel vengono disegnati usando [**glDrawPixels**](gldrawpixels.md).

Le funzioni seguenti recuperano informazioni correlate a **glCopyTexSubImage2D**:

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled con**](glisenabled.md) argomento GL \_ TEXTURE \_ 2D

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

[**glCopyTexSubImage1D**](glcopytexsubimage1d.md)
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

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





