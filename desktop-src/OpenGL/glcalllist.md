---
title: funzione glCallList (GL. h)
description: La funzione glCallList esegue un elenco di visualizzazione.
ms.assetid: 9373d32e-b11e-4a80-8713-da2c1d8d9368
keywords:
- funzione glCallList OpenGL
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
ms.openlocfilehash: f0d356adc5d16ceb0ea10e3834d8dbb98abed2b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120071"
---
# <a name="glcalllist-function"></a>glCallList (funzione)

La funzione **glCallList** esegue un elenco di visualizzazione.

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

Quando si richiama la funzione **glCallList** , viene avviata l'esecuzione dell'elenco di visualizzazione denominato. Le funzioni salvate nell'elenco di visualizzazione vengono eseguite in ordine, come se fossero state chiamate senza usare un elenco di visualizzazione. Se l' *elenco* non è stato definito come elenco di visualizzazione, **glCallList** viene ignorato.

La funzione **glCallList** può essere visualizzata all'interno di un elenco di visualizzazione. Per evitare la possibilità di una ricorsione infinita risultante da elenchi di visualizzazione che si richiamano, viene applicato un limite al livello di annidamento degli elenchi di visualizzazione durante l'esecuzione dell'elenco di visualizzazione. Questo limite è almeno 64, ma dipende dall'implementazione di.

Lo stato OpenGL non viene salvato e ripristinato tramite una chiamata a **glCallList**. Pertanto, le modifiche apportate allo stato OpenGL durante l'esecuzione di un elenco di visualizzazione rimangono al termine dell'esecuzione dell'elenco di visualizzazione. Per mantenere lo stato OpenGL tra le chiamate a **glCallList** , usare [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md)e [**glPopMatrix**](glpopmatrix.md).

È possibile eseguire gli elenchi di visualizzazione tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md), purché nell'elenco di visualizzazione siano incluse solo le funzioni consentite in questo intervallo.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glCallList**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con elenco di \_ \_ \_ nidificazione elenco massimo argomenti

[**Pagina di**](glislist.md)

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

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**Pagina di**](glislist.md)
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

 

 





