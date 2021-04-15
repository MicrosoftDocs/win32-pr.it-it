---
title: funzione glScissor (GL. h)
description: La funzione glScissor definisce la casella a forbice.
ms.assetid: c06a1d20-bf7b-4283-b0fe-8bd80bece4ce
keywords:
- funzione glScissor OpenGL
topic_type:
- apiref
api_name:
- glScissor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e18559bb30260dcb4285980d8dc75642a7c9ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479132"
---
# <a name="glscissor-function"></a>glScissor (funzione)

La funzione **glScissor** definisce la casella a forbice.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glScissor(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*x* 
</dt> <dd>

Coordinata x (asse verticale) dell'angolo inferiore sinistro della casella a forbice.

</dd> <dt>

*y* 
</dt> <dd>

Coordinata y (asse orizzontale) per l'angolo inferiore sinistro della casella a forbice. Insieme, x e y specificano l'angolo inferiore sinistro della casella a forbice. Inizialmente (0,0).

</dd> <dt>

*width* 
</dt> <dd>

Larghezza della casella a forbice.

</dd> <dt>

*height* 
</dt> <dd>

Altezza della casella a forbice. Quando un contesto OpenGL viene collegato per la *prima volta* a una finestra, la *larghezza* e l' *altezza* vengono impostate sulle dimensioni della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | La *larghezza* o l' *altezza* è negativa.<br/>                                                                                   |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glScissor** definisce un rettangolo, denominato casella Scissor, nelle coordinate della finestra. I primi due parametri, *x* e *y*, specificano l'angolo inferiore sinistro della casella. I parametri *Width* e *Height* specificano la larghezza e l'altezza della casella.

Il test a forbice viene abilitato e disabilitato usando [**glEnable**](glenable.md) e **glDisable** con l'argomento \_ test a forbice GL \_ . Mentre il test di scissor è abilitato, è possibile modificare solo i pixel che si trovano all'interno della casella di forbice disegnando comandi. Le coordinate della finestra hanno valori integer negli angoli condivisi dei pixel del framebuffer, quindi **glScissor**(0, 0, 1, 1) consente di modificare solo il pixel inferiore sinistro della finestra e **glScissor**(0, 0, 0, 0) non consente la modifica a tutti i pixel nella finestra.

Quando il test di scissor è disabilitato, è come se la casella Scissor includa l'intera finestra.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glScissor**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Scissor \_ Box

[**glIsEnabled**](glisenabled.md) con test della \_ forbice GL argomento \_

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

[**glEnable**](glenable.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





