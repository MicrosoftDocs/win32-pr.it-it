---
title: Funzione glPixelMapfv (Gl.h)
description: La funzione glPixelMapfv configura le mappe di trasferimento pixel.
ms.assetid: 13403243-1ec4-4b1d-a9da-9a6693b6f9b8
keywords:
- Funzione glPixelMapfv OpenGL
topic_type:
- apiref
api_name:
- glPixelMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e447e471f1a37f4d0c8c6bd8fb3ce548bb5657e49afafa01e785b0870ebdd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938356"
---
# <a name="glpixelmapfv-function"></a>Funzione glPixelMapfv

La **funzione glPixelMapfv** configura le mappe di trasferimento pixel.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPixelMapfv(
         GLenum  map,
         GLsizei mapsize,
   const GLfloat *values
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*map* 
</dt> <dd>

Nome simbolico della mappa. Le dieci mappe sono le seguenti.



| Valore                                                                                                                                                                               | Significato                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="GL_PIXEL_MAP_I_TO_I"></span><span id="gl_pixel_map_i_to_i"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ I \_ TO \_ I**</dt> </dl> | Mappe indici dei colori in indici dei colori.<br/>       |
| <span id="GL_PIXEL_MAP_S_TO_S"></span><span id="gl_pixel_map_s_to_s"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ S \_ TO \_ S**</dt> </dl> | Mappe gli indici degli stencil agli indici degli stencil.<br/>   |
| <span id="GL_PIXEL_MAP_I_TO_R"></span><span id="gl_pixel_map_i_to_r"></span><dl> <dt>**MAPPA \_ PIXEL GL DA I A \_ \_ \_ \_ R**</dt> </dl> | Mappe indici dei colori ai componenti rossi.<br/>      |
| <span id="GL_PIXEL_MAP_I_TO_G"></span><span id="gl_pixel_map_i_to_g"></span><dl> <dt>**MAPPA \_ PIXEL GL DA I A \_ \_ \_ \_ G**</dt> </dl> | Mappe indici dei colori ai componenti verdi.<br/>    |
| <span id="GL_PIXEL_MAP_I_TO_B"></span><span id="gl_pixel_map_i_to_b"></span><dl> <dt>**MAPPA \_ PIXEL GL DA I A \_ \_ \_ \_ B**</dt> </dl> | Mappe indici dei colori ai componenti blu.<br/>     |
| <span id="GL_PIXEL_MAP_I_TO_A"></span><span id="gl_pixel_map_i_to_a"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ I \_ TO \_ A**</dt> </dl> | Mappe indici dei colori ai componenti alfa.<br/>    |
| <span id="GL_PIXEL_MAP_R_TO_R"></span><span id="gl_pixel_map_r_to_r"></span><dl> <dt>**MAPPA \_ DEI PIXEL GL DA R A \_ \_ \_ \_ R**</dt> </dl> | Mappe componenti in rosso.<br/>     |
| <span id="GL_PIXEL_MAP_G_TO_G"></span><span id="gl_pixel_map_g_to_g"></span><dl> <dt>**MAPPA \_ PIXEL GL DA G A \_ \_ \_ \_ G**</dt> </dl> | Mappe componenti verdi ai componenti verdi.<br/> |
| <span id="GL_PIXEL_MAP_B_TO_B"></span><span id="gl_pixel_map_b_to_b"></span><dl> <dt>**MAPPA \_ DEI PIXEL GL DA B A \_ \_ \_ \_ B**</dt> </dl> | Mappe componenti blu in componenti blu.<br/>   |
| <span id="GL_PIXEL_MAP_A_TO_A"></span><span id="gl_pixel_map_a_to_a"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ A \_ TO \_ A**</dt> </dl> | Mappe componenti alfa in componenti alfa.<br/> |



 

</dd> <dt>

*mapsize* 
</dt> <dd>

Dimensioni della mappa da definire.

</dd> <dt>

*Valori* 
</dt> <dd>

Matrice di *valori mapsize.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *map* non è un valore accettato.<br/>                                                                                                                                                                                |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *mapsize è* negativo o maggiore di GL \_ PIXEL MAP \_ \_ TABLE. <br/>                                                                                                                                                   |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *map* era GL \_ PIXEL MAP I TO \_ \_ \_ \_ I, GL PIXEL MAP \_ S TO \_ \_ \_ \_ S, GL PIXEL MAP \_ I TO \_ \_ \_ \_ R, GL PIXEL MAP I \_ \_ TO \_ \_ \_ G, GL PIXEL MAP I TO B o GL PIXEL MAP I TO \_ A \_ \_ \_ \_ \_ \_ \_ \_ \_  e mapsize non era una potenza di due. <br/> |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). <br/>                                                                                     |



## <a name="remarks"></a>Commenti

La funzione **glPixelMap** configura le tabelle di traduzione, o mappe *,* usate da [**glCopyPixels,**](glcopypixels.md) [**glCopyTexImage1D,**](glcopyteximage1d.md) [**glCopyTexImage2D,**](glcopyteximage2d.md) [**glCopyTexSubImage1D,**](glcopytexsubimage1d.md) [**glCopyTexSubImage2D,**](glcopytexsubimage2d.md) [**glDrawPixels,**](gldrawpixels.md) [**glReadPixels,**](glreadpixels.md) [**glTexImage1D,**](glteximage1d.md) [**glTexImage2D,**](glteximage2d.md) [**glTexSubImage1D**](gltexsubimage1d.md)e [**glTexSubImage2D.**](gltexsubimage2d.md) L'uso di queste mappe è descritto completamente nell'argomento [**glPixelTransfer**](glpixeltransfer.md) e in parte negli argomenti per i comandi pixel e immagine di trama. In questo argomento viene descritta solo la specifica delle mappe.

Il *parametro map* è un nome di mappa simbolico, che indica una delle dieci mappe da impostare. Il *parametro mapsize* specifica il numero di voci nella mappa e *i* valori sono un puntatore a una matrice di valori *mappa mapsize.*

Le voci in una mappa possono essere specificate come numeri a virgola mobile e precisione singola, interi brevi senza segno o interi lunghi senza segno. Mappe che archiviano i valori dei componenti di colore (tutti, ad eccezioni di GL PIXEL MAP I TO I e GL PIXEL MAP S TO S), mantengono i valori in formato a virgola mobile, con \_ \_ \_ dimensioni \_ \_ \_ \_ \_ \_ \_ mantissa ed esponenti non specifiche. I valori a virgola mobile specificati da [**glPixelMapfv**](glpixelmap.md) vengono convertiti direttamente nel formato a virgola mobile interno di queste mappe e quindi sono ancorati all'intervallo \[ 0,1. \] I valori interi senza segno specificati da **glPixelMapusv** e **glPixelMapuiv** vengono convertiti in modo lineare in modo che il numero intero rappresentabile più grande sia mappato a 1,0 e zero sia mappato a 0,0.

Mappe che archiviano gli indici, GL PIXEL MAP I TO I e GL PIXEL MAP S TO S, mantengono i valori in formato a virgola fissa, con un numero non specificato di bit a destra del punto \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ binario. I valori a virgola mobile specificati da [**glPixelMapfv**](glpixelmap.md) vengono convertiti direttamente nel formato a virgola fissa interno di queste mappe. I valori integer senza segno specificati da **glPixelMapusv** e **glPixelMapuiv** specificano valori interi, con tutti gli zeri a destra del punto binario.

La tabella seguente illustra le dimensioni iniziali e i valori per ognuna delle mappe. Mappe indicizzati da indici di colori o di stencil devono avere *mapsize* = 2 ^ *n* per alcuni *n* o i risultati non sono definiti. La dimensione massima consentita per ogni mappa dipende dall'implementazione e può essere determinata chiamando **glGet** con l'argomento GL \_ MAX PIXEL MAP \_ \_ \_ TABLE. Il singolo massimo si applica a tutte le mappe ed è almeno 32.



| Mappa                      | Indice di ricerca  | Valore di ricerca  | Dimensioni iniziali | Valore iniziale |
|--------------------------|---------------|---------------|--------------|---------------|
| GL \_ PIXEL \_ MAP \_ I \_ TO \_ I | indice dei colori   | indice dei colori   | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ S \_ TO \_ S | indice degli stencil | indice degli stencil | 1            | 0,0           |
| MAPPA \_ PIXEL GL DA I A \_ \_ \_ \_ R | indice dei colori   | R             | 1            | 0,0           |
| MAPPA \_ PIXEL GL DA I A \_ \_ \_ \_ G | indice dei colori   | G             | 1            | 0,0           |
| MAPPA \_ PIXEL GL DA I A \_ \_ \_ \_ B | indice dei colori   | B             | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ I \_ TO \_ A | indice dei colori   | A             | 1            | 0,0           |
| MAPPA \_ DEI PIXEL GL DA R A \_ \_ \_ \_ R | R             | R             | 1            | 0,0           |
| GL \_ PIXEL MAP DA G A \_ \_ \_ \_ G | G             | G             | 1            | 0,0           |
| MAPPA \_ DEI PIXEL GL DA B A \_ \_ \_ \_ B | B             | B             | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ A \_ TO \_ A | A             | A             | 1            | 0,0           |



 

Le funzioni seguenti recuperano informazioni correlate **a glPixelMap**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ PIXEL MAP I TO I \_ \_ \_ \_ \_ SIZE

**glGet con** argomento GL \_ PIXEL MAP S TO S \_ \_ \_ \_ \_ SIZE

**glGet con** argomento GL \_ PIXEL MAP I TO R \_ \_ \_ \_ \_ SIZE

**glGet con** argomento GL \_ PIXEL MAP I TO G \_ \_ \_ \_ \_ SIZE

**glGet con** argomento GL \_ PIXEL MAP I TO B \_ \_ \_ \_ \_ SIZE

**glGet con** argomento GL \_ PIXEL MAP I TO A \_ \_ \_ \_ \_ SIZE

**glGet con** argomento GL \_ PIXEL MAP R TO R \_ \_ \_ \_ \_ SIZE

**glGet con** argomento GL \_ PIXEL MAP G TO G \_ \_ \_ \_ \_ SIZE

**glGet con** argomento GL \_ PIXEL MAP B TO B \_ \_ \_ \_ \_ SIZE

**glGet con** argomento GL \_ PIXEL MAP A TO A \_ \_ \_ \_ \_ SIZE

**glGet con** argomento GL \_ MAX PIXEL MAP \_ \_ \_ TABLE

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

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





