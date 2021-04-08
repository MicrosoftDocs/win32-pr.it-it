---
title: funzione gluErrorString (Glu. h)
description: La funzione gluErrorString genera una stringa di errore da un codice di errore OpenGL o GLU. La stringa di errore è solo ANSI.
ms.assetid: 6d71a6d5-ac00-49f9-a56c-cfeeb88963eb
keywords:
- funzione gluErrorString OpenGL
topic_type:
- apiref
api_name:
- gluErrorString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cdcfad0e2a943bf3a475317f32d37921878a8f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741119"
---
# <a name="gluerrorstring-function"></a>gluErrorString (funzione)

La funzione **gluErrorString** genera una stringa di errore da un codice di errore OpenGL o Glu. La stringa di errore è solo ANSI.

## <a name="syntax"></a>Sintassi


```C++
const GLubyte* WINAPI gluErrorString(
   GLenum errCode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*errCode* 
</dt> <dd>

Codice di errore OpenGL o GLU.

</dd> </dl>

## <a name="remarks"></a>Commenti

La funzione **gluErrorString** genera una stringa di errore da un codice di errore OpenGL o Glu. La stringa è in un formato ISO Latin 1. Ad esempio, **gluErrorString**(GL \_ \_ \_ insufficiente) restituisce la stringa "memoria insufficiente".

I codici di errore standard GLU sono di tipo GLU \_ non valido \_ , il \_ valore non è valido \_ e il valore di Glu non è \_ \_ \_ sufficiente. Determinate altre funzioni GLU possono restituire codici di errore specializzati tramite callback. Per l'elenco dei codici di errore OpenGL, vedere [**glGetError**](glgeterror.md).

La funzione **gluErrorString** produce stringhe di errore solo in ANSI. Quando possibile, usare **gluErrorStringWIN**, che consente stringhe di errore ANSI o Unicode. Questo consente di localizzare più facilmente il programma per l'uso con un altro linguaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[*gluNurbsCallback*](glunurbs.md)
</dt> <dt>

[*gluQuadricCallback*](gluquadric.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> </dl>

 

 





