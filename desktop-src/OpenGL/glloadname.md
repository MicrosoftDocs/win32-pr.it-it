---
title: funzione glLoadName (GL. h)
description: La funzione glLoadName carica un nome nello stack dei nomi.
ms.assetid: 8d7d582b-3743-401e-af71-28034e49f3c2
keywords:
- funzione glLoadName OpenGL
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
ms.openlocfilehash: bb47a0389cda13523104ee429bca46838970e15a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121591"
---
# <a name="glloadname-function"></a>glLoadName (funzione)

La funzione **glLoadName** carica un nome nello stack dei nomi.

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

Nome che sostituisce il valore superiore nello stack dei nomi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata mentre lo stack dei nomi era vuoto.<br/>                                                                    |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glLoadName** fa sì che il *nome* sostituisca il valore all'inizio dello stack dei nomi, che inizialmente è vuoto. Lo stack dei nomi viene usato durante la modalità di selezione per consentire l'identificazione univoca di set di comandi di rendering. È costituito da un set ordinato di interi senza segno.

Lo stack dei nomi è sempre vuoto mentre la modalità di rendering non è GL \_ Select. Le chiamate a **glLoadName** mentre la modalità di rendering non è GL \_ SELECT vengono ignorate.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glLoadName**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ \_ profondità dello stack nome GL \_

**glGet** con argomento- \_ \_ \_ profondità dello stack nome Max \_

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

[**glPushName**](glpushname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





