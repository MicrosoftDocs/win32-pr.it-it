---
title: Funzione glCopyTexImage1D (Gl.h)
description: La funzione glCopyTexImage1D copia i pixel dal framebuffer in un'immagine di trama unidimensionale.
ms.assetid: 3b4d12d5-5efe-40d2-ac5f-95ea5ef243dd
keywords:
- Funzione openGL glCopyTexImage1D
topic_type:
- apiref
api_name:
- glCopyTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e3dd966aa08eb5c74fa15235ed51f07a671c4e6f1378a990c6686fdc801e1d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118617349"
---
# <a name="glcopyteximage1d-function"></a>Funzione glCopyTexImage1D

La **funzione glCopyTexImage1D** copia i pixel dal framebuffer in un'immagine di trama unidimensionale.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glCopyTexImage1D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLint   border
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Destinazione per cui verranno modificati i dati dell'immagine. Deve avere il valore GL \_ TEXTURE \_ 1D.

</dd> <dt>

*level* 
</dt> <dd>

Numero di livello di dettaglio. Il livello 0 è l'immagine di base. Il *livello n* è *l'esima* immagine di riduzione mipmap.

</dd> <dt>

*internalFormat* 
</dt> <dd>

Formato interno e risoluzione dei dati di trama. Questo parametro deve essere uno dei valori simbolici seguenti.



| Costante                 | Bit R | Bit G | Bit B | Bit A | Bit L | Bit I |
|--------------------------|--------|--------|--------|--------|--------|--------|
| GL \_ ALPHA                |        |        |        |        |        |        |
| GL \_ ALPHA4               |        |        |        | 4      |        |        |
| GL \_ ALPHA8               |        |        |        | 8      |        |        |
| GL \_ ALPHA12              |        |        |        | 12     |        |        |
| GL \_ ALPHA16              |        |        |        | 16     |        |        |
| GL \_ LUMINANCE            |        |        |        |        |        |        |
| GL \_ LUMINANCE4           |        |        |        |        | 4      |        |
| GL \_ LUMINANCE8           |        |        |        |        | 8      |        |
| GL \_ LUMINANCE12          |        |        |        |        | 12     |        |
| GL \_ LUMINANCE16          |        |        |        |        | 16     |        |
| GL \_ LUMINANCE \_ ALPHA     |        |        |        |        |        |        |
| GL \_ LUMINANCE4 \_ ALPHA4   |        |        |        | 4      | 4      |        |
| GL \_ LUMINANCE6 \_ ALPHA2   |        |        |        | 2      | 6      |        |
| GL \_ LUMINANCE8 \_ ALPHA8   |        |        |        | 8      | 8      |        |
| GL \_ LUMINANCE12 \_ ALPHA4  |        |        |        | 4      | 12     |        |
| GL \_ LUMINANCE12 \_ ALPHA12 |        |        |        | 12     | 12     |        |
| GL \_ LUMINANCE16 \_ ALPHA16 |        |        |        | 16     | 16     |        |
| INTENSITÀ \_ GL            |        |        |        |        |        |        |
| INTENSITÀ \_ GL4           |        |        |        |        |        | 4      |
| INTENSITÀ \_ GL8           |        |        |        |        |        | 8      |
| INTENSITÀ \_ GL12          |        |        |        |        |        | 12     |
| INTENSITÀ \_ GL16          |        |        |        |        |        | 16     |
| GL \_ RGB                  |        |        |        |        |        |        |
| GL \_ R3 \_ G3 \_ B2           | 3      | 3      | 2      |        |        |        |
| GL \_ RGB4                 | 4      | 4      | 4      |        |        |        |
| GL \_ RGB5                 | 5      | 5      | 5      |        |        |        |
| GL \_ RGB8                 | 8      | 8      | 8      |        |        |        |
| GL \_ RGB10                | 10     | 10     | 10     |        |        |        |
| GL \_ RGB12                | 12     | 12     | 12     |        |        |        |
| GL \_ RGB16                | 16     | 16     | 16     |        |        |        |
| GL \_ RGBA                 |        |        |        |        |        |        |
| GL \_ RGBA2                | 2      | 2      | 2      | 2      |        |        |
| GL \_ RGBA4                | 4      | 4      | 4      | 4      |        |        |
| GL \_ RGB5 \_ A1             | 5      | 5      | 5      | 1      |        |        |
| GL \_ RGBA8                | 8      | 8      | 8      | 8      |        |        |
| GL \_ RGB10 \_ A2            | 10     | 10     | 10     | 2      |        |        |
| GL \_ RGBA12               | 12     | 12     | 12     | 12     |        |        |
| GL \_ RGBA16               | 16     | 16     | 16     | 16     |        |        |



 

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

Larghezza dell'immagine della trama. Deve essere zero o 2n + 2(*border*) per un numero intero *n*. L'altezza dell'immagine della trama è 1.

</dd> <dt>

*confine* 
</dt> <dd>

Larghezza del bordo. Deve essere zero o 1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *target* non è un valore accettato.<br/>                                                                                                           |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *level* è minore di zero o maggiore di log2 *max*, dove *max* è il valore restituito di GL \_ MAX TEXTURE \_ \_ SIZE.<br/>                           |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *border* non è zero o 1.<br/>                                                                                                                   |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *width* è minore di zero, maggiore di 2 + GL MAX TEXTURE SIZE o width non può essere rappresentato come \_ \_ \_ 2n +(*border*) per un numero *intero n*. <br/> |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>                    |



## <a name="remarks"></a>Commenti

La **funzione glCopyTexImage1D** definisce un'immagine di trama unidimensionale usando i pixel del framebuffer corrente, anziché dalla memoria principale, come nel caso di [**glTexImage1D.**](glteximage1d.md)

Usando il livello mipmap specificato con *level*, le matrici di trame vengono definite come una riga in pixel allineata con l'angolo inferiore sinistro della finestra alle coordinate specificate da *x* e *y*, con una lunghezza uguale a *width* + 2 \* *border*. Il formato interno della matrice di trame viene specificato con il *parametro internalFormat.*

La funzione **glCopyTexImage1D** elabora i pixel di una riga nello stesso modo di [**glCopyPixels**](glcopypixels.md), ad eccezione del fatto che prima della conversione finale dei pixel tutti i valori dei componenti pixel vengono bloccati \[ nell'intervallo 0,1 e convertiti nel formato interno della trama per \] l'archiviazione nella matrice di trame. L'ordinamento dei pixel viene determinato con *le coordinate x* inferiori corrispondenti alle coordinate della trama inferiori. Se uno dei pixel all'interno di una riga specificata del framebuffer corrente si trova all'esterno della finestra associata al contesto di rendering corrente, i relativi valori non sono definiti.

Non è possibile includere chiamate a **glCopyTexImage1D** negli elenchi di visualizzazione.

> [!Note]  
> La **funzione glCopyTexImage1D** è disponibile solo in OpenGL versione 1.1 o successiva.

 

La colorazione non ha alcun effetto in modalità color-index. Le [**funzioni glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) influiscono sulle immagini di trama esattamente nel modo in cui influiscono [**su glDrawPixels.**](gldrawpixels.md)

La funzione seguente recupera le informazioni correlate a **glCopyTexImage1D**:

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
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

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





