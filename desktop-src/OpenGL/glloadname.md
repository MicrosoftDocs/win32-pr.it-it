---
title: Funzione glLoadName (Gl.h)
description: La funzione glLoadName carica un nome nello stack dei nomi.
ms.assetid: 8d7d582b-3743-401e-af71-28034e49f3c2
keywords:
- Funzione glLoadName OpenGL
topic_type:
- apiref
api_name:
- glLoadName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f362862d2d4b57c43e12e522e2dac1767bbd36d88bda4ce3fb27f3c525fb3ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520391"
---
# <a name="glloadname-function"></a>Funzione glLoadName

La **funzione glLoadName** carica un nome nello stack dei nomi.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glLoadName(
   GLuint name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nome* 
</dt> <dd>

Nome che sostituirà il primo valore nello stack dei nomi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata mentre lo stack dei nomi era vuoto.<br/>                                                                    |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glLoadName** fa *in modo* che name sostituisca il valore all'inizio dello stack dei nomi, che è inizialmente vuoto. Lo stack di nomi viene usato durante la modalità di selezione per consentire l'identificazione univoca di set di comandi di rendering. È costituito da un set ordinato di interi senza segno.

Lo stack dei nomi è sempre vuoto mentre la modalità di rendering non è GL \_ SELECT. Le chiamate a **glLoadName** mentre la modalità di rendering non è GL \_ SELECT vengono ignorate.

Le funzioni seguenti recuperano informazioni correlate a **glLoadName**:

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

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glPushName**](glpushname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





