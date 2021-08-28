---
title: Funzione glRasterPos2f (Gl.h)
description: Specifica la posizione raster per le operazioni in pixel. | Funzione glRasterPos2f (Gl.h)
ms.assetid: cf63d1a5-505b-466e-bc6e-4f05adf8cc46
keywords:
- Funzione glRasterPos2f OpenGL
topic_type:
- apiref
api_name:
- glRasterPos2f
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1c045238e9d21dbd4300a6d32c972b9706979ed2033d556cac13117446d83d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492501"
---
# <a name="glrasterpos2f-function"></a>Funzione glRasterPos2f

Specifica la posizione raster per le operazioni in pixel.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glRasterPos2f(
   GLfloat x,
   GLfloat y
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*x* 
</dt> <dd>

Specifica la coordinata x per la posizione raster corrente.

</dd> <dt>

*y* 
</dt> <dd>

Specifica la coordinata y per la posizione raster corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

OpenGL mantiene una posizione 3D nelle coordinate della finestra. Questa posizione, denominata posizione raster, viene mantenuta con l'accuratezza dei subpixel. Viene usato per posizionare le operazioni di scrittura di pixel e bitmap. Vedere [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md)e [**glCopyPixels**](glcopypixels.md).

La posizione raster corrente è costituita da tre coordinate della finestra *(x, y, z*), una coordinata di ritaglio con valore *w,* una distanza delle coordinate oculare, un bit valido e le coordinate di trama e i dati colore associati. La *coordinata w* è una coordinata di ritaglio, perché *w* non viene proiettata nelle coordinate della finestra. La [funzione glRasterPos4](glrasterpos-functions.md) specifica in modo esplicito le coordinate degli oggetti *x, y, z* e *w.* La funzione glRasterPos3 specifica le coordinate degli oggetti *x, y* e *z* in modo esplicito, mentre *w* è impostato in modo implicito su uno. La funzione glRasterPos2 usa i valori degli argomenti per *x* e *y* mentre imposta in modo implicito *z* e *w* su zero e uno.

Le coordinate dell'oggetto [presentate da glRasterPos](glrasterpos-functions.md) vengono considerate esattamente come quelle di un [comando glVertex.](glvertex-functions.md) Vengono trasformate dalle matrici correnti di visualizzazione del modello e proiezione e passate alla fase di ritaglio. Se il vertice non viene culled, viene proiettato e ridimensionato in base alle coordinate della finestra, che diventano la nuova posizione raster corrente, e viene impostato il flag GL \_ CURRENT \_ RASTER \_ POSITION \_ VALID. Se il vertice viene eliminato, il bit valido viene cancellato e la posizione raster corrente e le coordinate di colore e trama associate non sono definite.

La posizione raster corrente include anche alcuni dati di colore associati e le coordinate della trama. Se l'illuminazione è abilitata, GL CURRENT RASTER COLOR, in modalità RGBA, o GL CURRENT RASTER INDEX, in modalità color-index, viene impostato sul colore prodotto dal calcolo dell'illuminazione \_ \_ \_ \_ \_ \_ (vedere [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md)e [**glShadeModel).**](glshademodel.md) Se l'illuminazione è disabilitata, per aggiornare il colore raster corrente viene usato il colore corrente (in modalità RGBA, la variabile di stato GL CURRENT COLOR) o l'indice colori (in modalità \_ color-index, variabile di stato \_ GL \_ CURRENT \_ INDEX).

Analogamente, GL CURRENT RASTER TEXTURE COORDS viene aggiornato come funzione di GL CURRENT TEXTURE COORDS, in base alla matrice di trama e alle funzioni di generazione \_ \_ della trama \_ \_ \_ \_ \_ (vedere [glTexGen).](gltexgen-functions.md) Infine, la distanza dall'origine del sistema di coordinate oculare al vertice, trasformata solo dalla matrice della visualizzazione modello, sostituisce GL \_ CURRENT \_ RASTER \_ DISTANCE.

Inizialmente, la posizione raster corrente è (0,0,0,1), la distanza raster corrente è 0, il bit valido è impostato, il colore RGBA associato è (1,1,1,1), l'indice dei colori associato è 1 e le coordinate della trama associate sono (0, 0, 0, 1). In modalità RGBA, GL CURRENT RASTER INDEX è sempre 1. In modalità indice colore, il colore \_ \_ RGBA raster corrente mantiene sempre \_ il valore iniziale.

> [!Note]  
> La posizione raster viene modificata sia da [glRasterPos](glrasterpos-functions.md) che da [**glBitmap.**](glbitmap.md)

 

> [!Note]  
> Quando le coordinate di posizione raster non sono valide, i comandi di disegno basati sulla posizione raster vengono ignorati, ovvero non comportano modifiche allo stato OpenGL.

 

Le funzioni seguenti recuperano informazioni correlate [a glRasterPos:](glrasterpos-functions.md)

<dl>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ CURRENT \_ RASTER \_ POSITION  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ CURRENT \_ RASTER \_ POSITION \_ VALID  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ CURRENT \_ RASTER \_ DISTANCE  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ CURRENT \_ RASTER \_ COLOR  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ CURRENT \_ RASTER \_ INDEX  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ CURRENT \_ RASTER \_ TEXTURE \_ COORDS  
</dl>

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

[**glBitmap**](glbitmap.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
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

 

 





