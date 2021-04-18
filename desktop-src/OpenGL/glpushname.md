---
title: funzione glPushName (GL. h)
description: Le funzioni glPushName e glPopName effettuano il push e il pop dello stack dei nomi. | funzione glPushName (GL. h)
ms.assetid: e4319018-42c0-4567-b67f-31dbdbee9b13
keywords:
- funzione glPushName OpenGL
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
ms.openlocfilehash: 1ff783a108f5cb1ac34141c6c57f47b16e23531a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321545"
---
# <a name="glpushname-function"></a>glPushName (funzione)

Le funzioni **glPushName** e [**glPopName**](glpopname.md) effettuano il push e il pop dello stack dei nomi.

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

Nome che verrà inserito nello stack dei nomi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_overflow dello stack GL \_**</dt> </dl>    | La funzione è stata chiamata mentre lo stack della matrice corrente era pieno.<br/>                                                           |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glPushName** fa sì che il nome venga inserito nello stack dei nomi, inizialmente vuoto. La funzione [**glPopName**](glpopname.md) estrae un nome all'inizio dello stack. Lo stack dei nomi viene usato durante la modalità di selezione per consentire l'identificazione univoca di set di comandi di rendering. È costituito da un set ordinato di interi senza segno.

Lo stack dei nomi è sempre vuoto mentre la modalità di rendering non è GL \_ Select. Le chiamate a **glPushName** o [**glPopName**](glpopname.md) mentre la modalità di rendering non è GL \_ SELECT vengono ignorate.

Le funzioni seguenti recuperano informazioni relative a **glPushName** e [**glPopName**](glpopname.md):

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ \_ profondità dello stack nome GL \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento- \_ \_ \_ profondità dello stack nome Max \_

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

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





