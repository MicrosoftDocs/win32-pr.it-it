---
title: funzione glRasterPos2sv (GL. h)
description: Specifica la posizione raster per le operazioni sui pixel. | funzione glRasterPos2sv (GL. h)
ms.assetid: 7a217946-affa-442f-85d8-e21a0e458b5f
keywords:
- funzione glRasterPos2sv OpenGL
topic_type:
- apiref
api_name:
- glRasterPos2sv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6a2c813932d4ebe1aeb1486f683423ae80b92c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321960"
---
# <a name="glrasterpos2sv-function"></a>glRasterPos2sv (funzione)

Specifica la posizione raster per le operazioni sui pixel.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glRasterPos2sv(
   const GLshort *v
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*v* 
</dt> <dd>

Puntatore a una matrice di due elementi, che specifica le coordinate x e y per la posizione raster corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

OpenGL mantiene una posizione 3D nelle coordinate della finestra. Questa posizione, denominata posizione raster, viene mantenuta con l'accuratezza dei subpixel. Viene usato per posizionare le operazioni di scrittura di pixel e bitmap. Vedere [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md)e [**glCopyPixels**](glcopypixels.md).

La posizione raster corrente è costituita da tre coordinate della finestra (*x, y, z*), un valore di coordinata di ritaglio *w* , una distanza delle coordinate oculari, un bit valido e coordinate di trama e dati di colore associati. La coordinata *w* è una coordinata di ritaglio, perché *w* non è proiettata sulle coordinate della finestra. La funzione [glRasterPos4](glrasterpos-functions.md) specifica in modo esplicito le coordinate dell'oggetto *x, y, z* e *w* . La funzione glRasterPos3 specifica in modo esplicito le coordinate dell'oggetto *x, y* e *z* , mentre *w* viene impostato in modo implicito su uno. La funzione glRasterPos2 usa i valori degli argomenti per *x* e *y* , impostando in modo implicito *z* e *w* su zero e uno.

Le coordinate degli oggetti presentate da [glRasterPos](glrasterpos-functions.md) vengono gestite esattamente come quelle di un comando [glVertex](glvertex-functions.md) . Vengono trasformati dalle matrici Modelview e Projection correnti e passate alla fase di ritaglio. Se il vertice non viene raccolto, viene proiettato e ridimensionato in base alle coordinate della finestra, che diventano la nuova posizione raster corrente e \_ \_ \_ viene impostato il flag valido della posizione raster corrente \_ . Se il vertice viene eliminato, viene cancellato il bit valido e la posizione raster corrente e le coordinate del colore e della trama associate non sono definite.

La posizione raster corrente include anche alcuni dati di colore e coordinate di trama associati. Se l'illuminazione è abilitata, il \_ colore raster corrente di GL, \_ \_ in modalità RGBA o \_ l' \_ Indice raster corrente GL \_ , in modalità di indice dei colori, viene impostato sul colore prodotto dal calcolo dell'illuminazione (vedere [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md)e [**glShadeModel**](glshademodel.md)). Se l'illuminazione è disabilitata, per aggiornare il colore raster corrente viene usato il colore corrente (in modalità RGBA, la variabile di stato GL \_ Current \_ Color) o l'indice dei colori (in modalità di indice colore, variabile di stato GL \_ Current \_ index).

Analogamente, \_ le \_ \_ coordinate di trama raster correnti GL \_ vengono aggiornate come funzione di \_ coordinate di trama correnti GL \_ \_ , in base alla matrice di trama e alle funzioni di generazione della trama (vedere [glTexGen](gltexgen-functions.md)). Infine, la distanza dall'origine del sistema di coordinate oculari al vertice, come trasformato solo dalla matrice Modelview, sostituisce la \_ distanza raster corrente di GL \_ \_ .

Inizialmente, la posizione raster corrente è (0, 0, 0, 1), la distanza raster corrente è 0, è impostato il bit valido, il colore RGBA associato è (1, 1, 1, 1), l'indice colori associato è 1 e le coordinate di trama associate sono (0, 0, 0, 1). In modalità RGBA, GL \_ Current \_ raster \_ index è sempre 1; in modalità di indice dei colori, il colore RGBA raster corrente mantiene sempre il proprio valore iniziale.

> [!Note]  
> La posizione raster viene modificata da [glRasterPos](glrasterpos-functions.md) e da [**glBitmap**](glbitmap.md).

 

> [!Note]  
> Quando le coordinate della posizione raster non sono valide, i comandi di disegno basati sulla posizione raster vengono ignorati, ovvero non comportano modifiche allo stato di OpenGL.

 

Le funzioni seguenti consentono di recuperare informazioni correlate a [glRasterPos](glrasterpos-functions.md):

<dl>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ raster \_ position  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ raster \_ position \_ valido  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ raster \_ distance  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ \_ color raster  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ \_ index raster  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento con \_ \_ coordinate di \_ trama \_ raster correnti  
</dl>

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

[**glBitmap**](glbitmap.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[glLight](gllight-functions.md)
</dt> <dt>

[glLightModel](gllightmodel-functions.md)
</dt> <dt>

[**glShadeModel**](glshademodel.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[glTexGen](gltexgen-functions.md)
</dt> <dt>

[glVertex](glvertex-functions.md)
</dt> </dl>

 

 





