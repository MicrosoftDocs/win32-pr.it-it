---
title: Funzione gluErrorString (Glu.h)
description: La funzione gluErrorString genera una stringa di errore da un codice di errore OpenGL o GLU. La stringa di errore è solo ANSI.
ms.assetid: 6d71a6d5-ac00-49f9-a56c-cfeeb88963eb
keywords:
- Funzione gluErrorString OpenGL
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
ms.openlocfilehash: beef90cfced2b33b612e15c1ef6918de81997520483acfb141f3a307ad64096d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777651"
---
# <a name="gluerrorstring-function"></a>Funzione gluErrorString

La **funzione gluErrorString** genera una stringa di errore da un codice di errore OpenGL o GLU. La stringa di errore è solo ANSI.

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

La **funzione gluErrorString** genera una stringa di errore da un codice di errore OpenGL o GLU. La stringa è in formato ISO Latin 1. Ad esempio, **gluErrorString**(GL \_ OUT OF \_ \_ MEMORY) restituisce la stringa "memoria insufficiente".

I codici di errore GLU standard sono GLU \_ INVALID \_ ENUM, GLU \_ INVALID VALUE e GLU OUT OF \_ \_ \_ \_ MEMORY. Alcune altre funzioni GLU possono restituire codici di errore specializzati tramite callback. Per l'elenco dei codici di errore OpenGL, vedere [**glGetError.**](glgeterror.md)

La **funzione gluErrorString** produce stringhe di errore solo in ANSI. Quando possibile, usare **gluErrorStringWIN,** che consente stringhe di errore ANSI o Unicode. In questo modo è più semplice localizzare il programma per l'uso con un altro linguaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
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

 

 





