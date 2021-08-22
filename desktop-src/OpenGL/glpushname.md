---
title: Funzione glPushName (Gl.h)
description: Le funzioni glPushName e glPopName esegono il push e il pop dello stack di nomi. | Funzione glPushName (Gl.h)
ms.assetid: e4319018-42c0-4567-b67f-31dbdbee9b13
keywords:
- Funzione glPushName OpenGL
topic_type:
- apiref
api_name:
- glPushName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd447c4b36822e25d70f0aa387040a76738f280a2b22393b53732941a087ff45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358331"
---
# <a name="glpushname-function"></a>Funzione glPushName

Le **funzioni glPushName** e [**glPopName**](glpopname.md) esegono il push e il pop dello stack di nomi.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPushName(
   GLuint name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nome* 
</dt> <dd>

Nome che verrà inserito nello stack di nomi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ STACK \_ OVERFLOW**</dt> </dl>    | La funzione è stata chiamata mentre lo stack di matrici corrente era pieno.<br/>                                                           |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glPushName** fa sì che name sia inserito nello stack dei nomi, inizialmente vuoto. La [**funzione glPopName**](glpopname.md) prescindo un nome dall'inizio dello stack. Lo stack di nomi viene usato durante la modalità di selezione per consentire l'identificazione univoca di set di comandi di rendering. È costituito da un set ordinato di interi senza segno.

Lo stack di nomi è sempre vuoto, mentre la modalità di rendering non è GL \_ SELECT. Le chiamate **a glPushName** o [**glPopName**](glpopname.md) mentre la modalità di rendering non è GL \_ SELECT vengono ignorate.

Le funzioni seguenti recuperano informazioni correlate **a glPushName** e [**glPopName:**](glpopname.md)

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

 

 





