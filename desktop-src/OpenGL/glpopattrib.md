---
title: funzione glPopAttrib (GL. h)
description: Estrae lo stack dell'attributo.
ms.assetid: 6a11392c-d5af-47bb-a66a-691730a58260
keywords:
- funzione glPopAttrib OpenGL
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
ms.openlocfilehash: e2258b0f16e6f61e660384931abc394300a29516
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301794"
---
# <a name="glpopattrib-function"></a>glPopAttrib (funzione)

Estrae lo stack dell'attributo.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPopAttrib(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_underflow dello stack GL \_**</dt> </dl>   | La funzione è stata chiamata mentre lo stack dell'attributo è vuoto.<br/>                                                               |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione [**glPushAttrib**](glpushattrib.md) accetta un argomento, una maschera che indica i gruppi di variabili di stato da salvare nello stack di attributi. Le costanti simboliche vengono utilizzate per impostare i bit nella maschera. Il parametro mask viene in genere costruito da **o** con alcune di queste costanti insieme. La maschera speciale GL \_ tutti \_ i \_ bit attrib può essere usata per salvare tutti gli Stati impilabili.

La funzione **glPopAttrib** Ripristina i valori delle variabili di stato salvate con l'ultimo comando [**glPushAttrib**](glpushattrib.md) . Quelli non salvati vengono lasciati invariati.

Non è possibile eseguire il push degli attributi in uno stack completo oppure per estrarre gli attributi da uno stack vuoto. In entrambi i casi, viene impostato il flag di errore e non viene apportata alcuna modifica allo stato OpenGL.

Inizialmente, lo stack dell'attributo è vuoto.

Non tutti i valori per lo stato OpenGL possono essere salvati nello stack di attributi. Ad esempio, non è possibile salvare lo stato di pixel Pack e unpack, lo stato della modalità di rendering e lo stato di selezione e feedback.

La profondità dello stack di attributi dipende dall'implementazione, ma deve essere almeno 16.

Le funzioni seguenti recuperano informazioni relative a [**glPushAttrib**](glpushattrib.md) e **glPopAttrib**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ \_ profondità dello stack \_ attrib

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ profondità massima \_ \_ dello stack \_ attrib

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

[**Remo**](glend.md)
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

 

 





