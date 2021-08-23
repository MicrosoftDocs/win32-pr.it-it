---
title: Funzione glInitNames (Gl.h)
description: La funzione glInitNames inizializza lo stack di nomi.
ms.assetid: 26c134f5-c17c-4637-93b6-5293f316dd6c
keywords:
- Funzione glInitNames OpenGL
topic_type:
- apiref
api_name:
- glInitNames
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a567242431fc90be3b60d8ae08875b585ff6a81794899a6c9eb69e7a0a03daa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012119"
---
# <a name="glinitnames-function"></a>Funzione glInitNames

La **funzione glInitNames** inizializza lo stack di nomi.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glInitNames(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glInitNames** causa l'inizializzazione dello stack di nomi allo stato vuoto predefinito. Lo stack di nomi viene usato durante la modalità di selezione per consentire l'identificazione univoca di set di comandi di rendering. È costituito da un set ordinato di interi senza segno.

Lo stack di nomi è sempre vuoto, mentre la modalità di rendering non è GL \_ SELECT. Le chiamate **a glInitNames** mentre la modalità di rendering non è GL \_ SELECT vengono ignorate.

Le funzioni seguenti recuperano informazioni correlate **a glInitNames:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ NAME STACK \_ \_ DEPTH

**glGet con** argomento GL \_ MAX NAME STACK \_ \_ \_ DEPTH

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

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glPushName**](glpushname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





