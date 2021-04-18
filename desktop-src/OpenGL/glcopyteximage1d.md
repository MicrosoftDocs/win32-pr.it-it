---
title: funzione glCopyTexImage1D (GL. h)
description: La funzione glCopyTexImage1D copia i pixel dal framebuffer in un'immagine di trama unidimensionale.
ms.assetid: 3b4d12d5-5efe-40d2-ac5f-95ea5ef243dd
keywords:
- funzione glCopyTexImage1D OpenGL
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
ms.openlocfilehash: e63180386c094f0c4e4de0f1a361bc3bcb1c6e5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301926"
---
# <a name="glcopyteximage1d-function"></a>glCopyTexImage1D (funzione)

La funzione **glCopyTexImage1D** copia i pixel dal framebuffer in un'immagine di trama unidimensionale.

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

Destinazione per cui verranno modificati i dati dell'immagine. Deve avere il valore GL \_ texture \_ 1D.

</dd> <dt>

*level* 
</dt> <dd>

Numero del livello di dettaglio. Il livello 0 è l'immagine di base. Il livello *n* è l'immagine di riduzione del mipmap *n*.

</dd> <dt>

*internalFormat* 
</dt> <dd>

Il formato interno e la risoluzione dei dati della trama. Questo parametro deve essere uno dei seguenti valori simbolici.



| Costante                 | Bit R | Bit G | Bit B | Bit | Bit L | Bit I |
|--------------------------|--------|--------|--------|--------|--------|--------|
| \_alfa GL                |        |        |        |        |        |        |
| \_ALPHA4 GL               |        |        |        | 4      |        |        |
| \_ALPHA8 GL               |        |        |        | 8      |        |        |
| \_ALPHA12 GL              |        |        |        | 12     |        |        |
| \_ALPHA16 GL              |        |        |        | 16     |        |        |
| \_luminanza GL            |        |        |        |        |        |        |
| \_LUMINANCE4 GL           |        |        |        |        | 4      |        |
| \_LUMINANCE8 GL           |        |        |        |        | 8      |        |
| \_LUMINANCE12 GL          |        |        |        |        | 12     |        |
| \_LUMINANCE16 GL          |        |        |        |        | 16     |        |
| \_alfa luminanza GL \_     |        |        |        |        |        |        |
| GL \_ LUMINANCE4 \_ ALPHA4   |        |        |        | 4      | 4      |        |
| GL \_ LUMINANCE6 \_ alfa2   |        |        |        | 2      | 6      |        |
| GL \_ LUMINANCE8 \_ ALPHA8   |        |        |        | 8      | 8      |        |
| GL \_ LUMINANCE12 \_ ALPHA4  |        |        |        | 4      | 12     |        |
| GL \_ LUMINANCE12 \_ ALPHA12 |        |        |        | 12     | 12     |        |
| GL \_ LUMINANCE16 \_ ALPHA16 |        |        |        | 16     | 16     |        |
| \_intensità GL            |        |        |        |        |        |        |
| \_INTENSITY4 GL           |        |        |        |        |        | 4      |
| \_INTENSITY8 GL           |        |        |        |        |        | 8      |
| \_INTENSITY12 GL          |        |        |        |        |        | 12     |
| \_INTENSITY16 GL          |        |        |        |        |        | 16     |
| GL \_ RGB                  |        |        |        |        |        |        |
| GL \_ R3 \_ G3 \_ B2           | 3      | 3      | 2      |        |        |        |
| \_RGB4 GL                 | 4      | 4      | 4      |        |        |        |
| \_RGB5 GL                 | 5      | 5      | 5      |        |        |        |
| \_RGB8 GL                 | 8      | 8      | 8      |        |        |        |
| \_RGB10 GL                | 10     | 10     | 10     |        |        |        |
| \_RGB12 GL                | 12     | 12     | 12     |        |        |        |
| \_Rgb16 GL                | 16     | 16     | 16     |        |        |        |
| \_RGBA GL                 |        |        |        |        |        |        |
| \_RGBA2 GL                | 2      | 2      | 2      | 2      |        |        |
| \_RGBA4 GL                | 4      | 4      | 4      | 4      |        |        |
| GL \_ RGB5 \_ a1             | 5      | 5      | 5      | 1      |        |        |
| \_Rgba8 GL                | 8      | 8      | 8      | 8      |        |        |
| GL \_ RGB10 \_ a2            | 10     | 10     | 10     | 2      |        |        |
| \_RGBA12 GL               | 12     | 12     | 12     | 12     |        |        |
| \_RGBA16 GL               | 16     | 16     | 16     | 16     |        |        |



 

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

Larghezza dell'immagine della trama. Deve essere zero o 2n + 2 (*bordo*) per alcuni numeri interi *n*. L'altezza dell'immagine della trama è 1.

</dd> <dt>

*bordo* 
</dt> <dd>

Larghezza del bordo. Deve essere zero o 1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *target* non è un valore accettato.<br/>                                                                                                           |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | il *livello* è minore di zero o maggiore di log2 *Max*, dove *Max* è il valore restituito della \_ dimensione della trama GL Max \_ \_ .<br/>                           |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | il *bordo* non è zero o 1.<br/>                                                                                                                   |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | *Width* è minore di zero, maggiore di 2 + GL \_ \_ dimensione della trama max \_ oppure la *larghezza* non può essere rappresentata come 2n + (*bordo*) per alcuni numeri interi *n*.<br/> |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>                    |



## <a name="remarks"></a>Commenti

La funzione **glCopyTexImage1D** definisce un'immagine di trama unidimensionale usando i pixel del framebuffer corrente, anziché dalla memoria principale come nel caso di [**glTexImage1D**](glteximage1d.md).

Usando il livello mipmap specificato con *Level*, le matrici di trama sono definite come una riga in pixel allineata all'angolo inferiore sinistro della finestra in corrispondenza delle coordinate specificate da *x* e *y*, con una lunghezza uguale a *Width* + 2 \* *Border*. Il formato interno della matrice di trama viene specificato con il parametro *internalFormat* .

La funzione **glCopyTexImage1D** elabora i pixel in una riga nello stesso modo in cui si trova [**glCopyPixels**](glcopypixels.md), ad eccezione del fatto che prima della conversione finale dei pixel, tutti i valori dei componenti pixel vengono bloccati nell'intervallo \[ 0, 1 \] e vengono convertiti nel formato interno della trama per l'archiviazione nella matrice di trame. L'ordinamento dei pixel è determinato da coordinate *x* inferiori corrispondenti a coordinate di trama inferiori. Se uno dei pixel all'interno di una riga specificata del framebuffer corrente è esterno alla finestra associata al contesto di rendering corrente, i relativi valori non sono definiti.

Non è possibile includere chiamate a **glCopyTexImage1D** negli elenchi di visualizzazione.

> [!Note]  
> La funzione **glCopyTexImage1D** è disponibile solo in OpenGL versione 1,1 o successiva.

 

La texturing non ha alcun effetto sulla modalità di indicizzazione del colore. Le funzioni [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) influiscono sulle immagini della trama esattamente come influiscono su [**glDrawPixels**](gldrawpixels.md).

La funzione seguente recupera le informazioni correlate a **glCopyTexImage1D**:

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

 

 





