---
title: Funzione glCallList (Gl.h)
description: La funzione glCallList esegue un elenco di visualizzazione.
ms.assetid: 9373d32e-b11e-4a80-8713-da2c1d8d9368
keywords:
- Funzione glCallList OpenGL
topic_type:
- apiref
api_name:
- glCallList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67805ff50eb4566e8a2a186c10229f944f4003baaef1274e9d4f52dd3b9c2a02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082121"
---
# <a name="glcalllist-function"></a>Funzione glCallList

La **funzione glCallList** esegue un elenco di visualizzazione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glCallList(
   GLuint list
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*list* 
</dt> <dd>

Nome intero dell'elenco di visualizzazione da eseguire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La chiamata della **funzione glCallList** avvia l'esecuzione dell'elenco di visualizzazione denominato. Le funzioni salvate nell'elenco di visualizzazione vengono eseguite in ordine, proprio come se le si chiamava senza usare un elenco di visualizzazione. Se *list* non è stato definito come elenco di visualizzazione, **glCallList viene** ignorato.

La **funzione glCallList** può essere visualizzata all'interno di un elenco di visualizzazione. Per evitare la possibilità di ricorsione infinita risultante da elenchi di visualizzazione che si chiamano tra loro, viene inserito un limite al livello di annidamento degli elenchi di visualizzazione durante l'esecuzione dell'elenco di visualizzazione. Questo limite è almeno 64, ma dipende dall'implementazione.

Lo stato OpenGL non viene salvato e ripristinato in una chiamata a **glCallList**. Di conseguenza, le modifiche apportate allo stato OpenGL durante l'esecuzione di un elenco di visualizzazione rimangono dopo il completamento dell'esecuzione dell'elenco di visualizzazione. Per mantenere lo stato OpenGL tra **le chiamate glCallList,** usare [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md)e [**glPopMatrix**](glpopmatrix.md).

È possibile eseguire elenchi di visualizzazione tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md), purché l'elenco di visualizzazione includa solo le funzioni consentite in questo intervallo.

Le funzioni seguenti recuperano informazioni correlate a **glCallList**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) l'argomento GL \_ MAX LIST \_ \_ NESTING

[**glIsList**](glislist.md)

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

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> <dt>

[**glPopAttrib**](glpopattrib.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





