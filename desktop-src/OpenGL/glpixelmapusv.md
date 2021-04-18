---
title: funzione glPixelMapusv (GL. h)
description: La funzione glPixelMapusv imposta le mappe di trasferimento dei pixel.
ms.assetid: c542a1be-8fb0-4269-afc0-459182c89534
keywords:
- funzione glPixelMapusv OpenGL
topic_type:
- apiref
api_name:
- glPixelMapusv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dd4adc50af4a4168d14ac2e39d465ace360ccbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301461"
---
# <a name="glpixelmapusv-function"></a>glPixelMapusv (funzione)

La funzione **glPixelMapusv** imposta le mappe di trasferimento dei pixel.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPixelMapusv(
         GLenum   map,
         GLsizei  mapsize,
   const GLushort *values
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*map* 
</dt> <dd>

Nome di mappa simbolico. Le dieci mappe sono le seguenti.



| Valore                                                                                                                                                                               | Significato                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="GL_PIXEL_MAP_I_TO_I"></span><span id="gl_pixel_map_i_to_i"></span><dl> <dt>**\_mappa GL \_ pixel \_ i \_ \_**</dt> </dl> | Esegue il mapping degli indici colore agli indici colori.<br/>       |
| <span id="GL_PIXEL_MAP_S_TO_S"></span><span id="gl_pixel_map_s_to_s"></span><dl> <dt>**\_mapping GL \_ pixel \_ \_ a \_ s**</dt> </dl> | Esegue il mapping degli indici stencil agli indici stencil.<br/>   |
| <span id="GL_PIXEL_MAP_I_TO_R"></span><span id="gl_pixel_map_i_to_r"></span><dl> <dt>**\_mapping GL \_ pixel \_ I \_ a \_ R**</dt> </dl> | Esegue il mapping degli indici dei colori ai componenti rossi.<br/>      |
| <span id="GL_PIXEL_MAP_I_TO_G"></span><span id="gl_pixel_map_i_to_g"></span><dl> <dt>**\_mappa GL \_ pixel \_ I \_ a \_ G**</dt> </dl> | Esegue il mapping degli indici dei colori ai componenti verdi.<br/>    |
| <span id="GL_PIXEL_MAP_I_TO_B"></span><span id="gl_pixel_map_i_to_b"></span><dl> <dt>**\_mappa GL \_ pixel \_ I \_ a \_ B**</dt> </dl> | Esegue il mapping degli indici dei colori ai componenti blu.<br/>     |
| <span id="GL_PIXEL_MAP_I_TO_A"></span><span id="gl_pixel_map_i_to_a"></span><dl> <dt>**\_mappa GL \_ pixel \_ I \_ a \_**</dt> </dl> | Esegue il mapping degli indici dei colori ai componenti alfa.<br/>    |
| <span id="GL_PIXEL_MAP_R_TO_R"></span><span id="gl_pixel_map_r_to_r"></span><dl> <dt>**\_mapping GL \_ pixel \_ r \_ a \_ r**</dt> </dl> | Esegue il mapping dei componenti rossi ai componenti rossi.<br/>     |
| <span id="GL_PIXEL_MAP_G_TO_G"></span><span id="gl_pixel_map_g_to_g"></span><dl> <dt>**\_mappa GL \_ pixel \_ \_ da g a \_ g**</dt> </dl> | Esegue il mapping dei componenti verdi ai componenti verdi.<br/> |
| <span id="GL_PIXEL_MAP_B_TO_B"></span><span id="gl_pixel_map_b_to_b"></span><dl> <dt>**\_mappa GL \_ pixel \_ b \_ a \_ b**</dt> </dl> | Esegue il mapping dei componenti blu ai componenti blu.<br/>   |
| <span id="GL_PIXEL_MAP_A_TO_A"></span><span id="gl_pixel_map_a_to_a"></span><dl> <dt>**\_pixel GL \_ mappato \_ \_ a a \_**</dt> </dl> | Esegue il mapping dei componenti alfa ai componenti alfa.<br/> |



 

</dd> <dt>

*MapSize* 
</dt> <dd>

Dimensione della mappa da definire.

</dd> <dt>

*valori* 
</dt> <dd>

Matrice di valori *MapSize* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | il *mapping* non è un valore accettato.<br/>                                                                                                                                                                                |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | *MapSize* è un valore negativo o maggiore della tabella di mapping di GL \_ pixel \_ \_ . <br/>                                                                                                                                                   |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | *Map* is GL \_ pixel \_ Map \_ i \_ to \_ i, GL \_ pixel \_ Map \_ S \_ to \_ s, GL \_ pixel \_ Map \_ i \_ to \_ R, GL \_ pixel \_ Map \_ i \_ to \_ G, GL \_ pixel \_ Map \_ i \_ a \_ B o GL \_ pixel \_ Map \_ i \_ to \_ a e *MapSize* non era una potenza di due. <br/> |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). <br/>                                                                                     |



## <a name="remarks"></a>Commenti

La funzione **glPixelMap** imposta le tabelle di conversione, *o Maps*, utilizzate [**da glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), GlCopyTexSubImage2D, glDrawPixels, [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)e [**glTexSubImage2D**](gltexsubimage2d.md). [](glcopytexsubimage2d.md) [](gldrawpixels.md) L'uso di queste mappe è descritto completamente nell'argomento [**glPixelTransfer**](glpixeltransfer.md) e in parte negli argomenti relativi ai comandi per immagini pixel e trama. In questo argomento viene descritta solo la specifica delle mappe.

Il parametro *Map* è un nome di mappa simbolico che indica una delle dieci mappe da impostare. Il parametro *MapSize* specifica il numero di voci nella mappa e *values* è un puntatore a una matrice di valori della mappa *MapSize* .

Le voci in una mappa possono essere specificate come numeri a virgola mobile e precisione singola, interi brevi senza segno o interi long senza segno. Mappe che archiviano i valori dei componenti colore (tutti tranne GL \_ pixel \_ Map \_ i \_ to \_ i e GL \_ pixel \_ Map \_ s \_ to \_ s) mantengono i valori in formato a virgola mobile, con dimensioni mantissa e esponenti non specificate. I valori a virgola mobile specificati da [**glPixelMapfv**](glpixelmap.md) vengono convertiti direttamente nel formato a virgola mobile interno di queste mappe, quindi vengono bloccati nell'intervallo compreso tra \[ 0 e 1 \] . I valori interi senza segno specificati da **glPixelMapusv** e **glPixelMapuiv** vengono convertiti linearmente in modo che il valore integer rappresentabile più grande sia mappato a 1,0 e zero sia mappato a 0,0.

Mappe che archiviano gli indici, GL \_ pixel \_ Map \_ i \_ to \_ i e GL \_ pixel \_ Map \_ s \_ to \_ s, mantengono i valori in formato a virgola fissa, con un numero di bit non specificato a destra del punto binario. I valori a virgola mobile specificati da [**glPixelMapfv**](glpixelmap.md) vengono convertiti direttamente nel formato a virgola fissa interno di queste mappe. I valori interi senza segno specificati da **glPixelMapusv** e **glPixelMapuiv** specificano i valori integer, con tutti gli zeri a destra del punto binario.

Nella tabella seguente vengono illustrate le dimensioni e i valori iniziali per ogni mappa. Le mappe indicizzate in base agli indici colore o stencil devono avere *MapSize* = 2 ^ *n* per alcuni *n* o i risultati non sono definiti. Le dimensioni massime consentite per ogni mapping dipendono dall'implementazione e possono essere determinate chiamando **glGet** con la \_ tabella di mappa dei pixel max dell'argomento \_ \_ \_ . Il valore massimo viene applicato a tutte le mappe ed è almeno pari a 32.



| Mappa                      | Indice di ricerca  | Valore di ricerca  | Dimensioni iniziali | Valore iniziale |
|--------------------------|---------------|---------------|--------------|---------------|
| \_mappa GL \_ pixel \_ i \_ \_ | indice colori   | indice colori   | 1            | 0,0           |
| \_mapping GL \_ pixel \_ \_ a \_ s | Indice stencil | Indice stencil | 1            | 0,0           |
| \_mapping GL \_ pixel \_ I \_ a \_ R | indice colori   | R             | 1            | 0,0           |
| \_mappa GL \_ pixel \_ I \_ a \_ G | indice colori   | G             | 1            | 0,0           |
| \_mappa GL \_ pixel \_ I \_ a \_ B | indice colori   | B             | 1            | 0,0           |
| \_mappa GL \_ pixel \_ I \_ a \_ | indice colori   | A             | 1            | 0,0           |
| \_mapping GL \_ pixel \_ r \_ a \_ r | R             | R             | 1            | 0,0           |
| \_mappa GL \_ pixel \_ \_ da g a \_ g | G             | G             | 1            | 0,0           |
| \_mappa GL \_ pixel \_ b \_ a \_ b | B             | B             | 1            | 0,0           |
| \_pixel GL \_ mappato \_ \_ a a \_ | A             | A             | 1            | 0,0           |



 

Le funzioni seguenti consentono di recuperare informazioni correlate a **glPixelMap**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ pixel \_ Map \_ i \_ to \_ i \_ size

**glGet** con argomento \_ \_ di mapping GL pixel per la \_ \_ \_ \_ dimensione s

**glGet** con argomento GL \_ pixel \_ Map \_ I \_ to \_ R \_ size

**glGet** con argomento GL \_ pixel \_ mapping \_ I \_ a \_ G \_ size

**glGet** con argomento GL \_ pixel \_ Map \_ I \_ a \_ B \_ size

**glGet** con argomento GL \_ pixel \_ mappa \_ I \_ a \_ una \_ dimensione

**glGet** con argomento GL \_ pixel \_ Map \_ r \_ to \_ r \_ size

**glGet** con argomento GL \_ pixel \_ mappa \_ g \_ a \_ g \_ size

**glGet** con argomento GL \_ pixel \_ mappa \_ b \_ a \_ b \_ dimensioni

**glGet** con argomento GL \_ pixel \_ mappa \_ a \_ \_ una \_ dimensione

**glGet** con argomento \_ tabella di \_ mappa pixel max \_ \_

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**Remo**](glend.md)
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

 

 





