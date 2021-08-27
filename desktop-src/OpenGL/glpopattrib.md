---
title: Funzione glPopAttrib (Gl.h)
description: Popola lo stack di attributi.
ms.assetid: 6a11392c-d5af-47bb-a66a-691730a58260
keywords:
- Funzione glPopAttrib OpenGL
topic_type:
- apiref
api_name:
- glPopAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92034154138ab3747ce190c05716e2df0d82ed3f6b26aba38da780873ce03721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081451"
---
# <a name="glpopattrib-function"></a>Funzione glPopAttrib

Popola lo stack di attributi.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPopAttrib(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ STACK \_ UNDERFLOW**</dt> </dl>   | La funzione è stata chiamata mentre lo stack di attributi era vuoto.<br/>                                                               |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La [**funzione glPushAttrib**](glpushattrib.md) accetta un argomento, una maschera che indica quali gruppi di variabili di stato salvare nello stack di attributi. Le costanti simboliche vengono usate per impostare i bit nella maschera. Il parametro mask viene in genere costruito **con OR** unendo diverse di queste costanti. La maschera speciale GL \_ ALL \_ ATTRIB BITS può essere usata per salvare tutti gli \_ stati impilabili.

La **funzione glPopAttrib** ripristina i valori delle variabili di stato salvate con l'ultimo [**comando glPushAttrib.**](glpushattrib.md) Quelli non salvati rimangono invariati.

È un errore eseguire il push degli attributi in uno stack completo o rimuovere gli attributi da uno stack vuoto. In entrambi i casi, il flag di errore viene impostato e non vengono apportate altre modifiche allo stato OpenGL.

Inizialmente, lo stack di attributi è vuoto.

Non tutti i valori per lo stato OpenGL possono essere salvati nello stack di attributi. Ad esempio, lo stato pack e unpack pixel, lo stato della modalità di rendering e lo stato di selezione e feedback non possono essere salvati.

La profondità dello stack di attributi dipende dall'implementazione, ma deve essere almeno 16.

Le funzioni seguenti recuperano informazioni correlate [**a glPushAttrib**](glpushattrib.md) e **glPopAttrib:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ ATTRIB \_ STACK \_ DEPTH

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ MAX \_ ATTRIB \_ STACK \_ DEPTH

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

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetClipPlane**](glgetclipplane.md)
</dt> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[**glGetLight**](glgetlight.md)
</dt> <dt>

[**glGetMap**](glgetmap.md)
</dt> <dt>

[**glGetMaterial**](glgetmaterial.md)
</dt> <dt>

[**glGetPixelMap**](glgetpixelmap.md)
</dt> <dt>

[**glGetPolygonStipple**](glgetpolygonstipple.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glGetTexEnv**](glgettexenv.md)
</dt> <dt>

[**glGetTexGen**](glgettexgen.md)
</dt> <dt>

[**glGetTexImage**](glgetteximage.md)
</dt> <dt>

[**glGetTexLevelParameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





