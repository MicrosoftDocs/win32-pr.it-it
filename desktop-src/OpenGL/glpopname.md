---
title: Funzione glPopName (Gl.h)
description: Le funzioni glPushName e glPopName esegono il push e il pop dello stack di nomi. | Funzione glPopName (Gl.h)
ms.assetid: ee741188-b275-4839-a89d-4d988c547d07
keywords:
- Funzione glPopName OpenGL
topic_type:
- apiref
api_name:
- glPopName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe30aa09d401fc8ef35a3671e02a898776af26111ae0f8e31cd1f6ad3bff70b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290171"
---
# <a name="glpopname-function"></a>Funzione glPopName

Le [**funzioni glPushName**](glpushname.md) e **glPopName** esegono il push e il pop dello stack di nomi.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPopName(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ STACK \_ UNDERFLOW**</dt> </dl>   | La funzione è stata chiamata mentre lo stack di matrici corrente conteneva una sola matrice.<br/>                                     |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La [**funzione glPushName**](glpushname.md) fa sì che name sia inserito nello stack dei nomi, inizialmente vuoto. La **funzione glPopName** prescindo un nome dall'inizio dello stack. Lo stack di nomi viene usato durante la modalità di selezione per consentire l'identificazione univoca di set di comandi di rendering. È costituito da un set ordinato di interi senza segno.

Lo stack di nomi è sempre vuoto, mentre la modalità di rendering non è GL \_ SELECT. Le chiamate [**a glPushName**](glpushname.md) o **glPopName** mentre la modalità di rendering non è GL \_ SELECT vengono ignorate.

Le funzioni seguenti recuperano informazioni correlate [**a glPushName**](glpushname.md) e **glPopName:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ NAME STACK \_ \_ DEPTH

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ MAX NAME STACK \_ \_ \_ DEPTH

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

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





