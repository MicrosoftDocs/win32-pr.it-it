---
title: Funzione glScissor (Gl.h)
description: La funzione glScissor definisce la casella di forbice.
ms.assetid: c06a1d20-bf7b-4283-b0fe-8bd80bece4ce
keywords:
- Funzione glScissor OpenGL
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
ms.openlocfilehash: fafefaaaa3315679af2900808f581324040512816dd2211a0250375c36f824dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777821"
---
# <a name="glscissor-function"></a>Funzione glScissor

La **funzione glScissor** definisce la casella di forbice.

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

Coordinata x (asse verticale) per l'angolo inferiore sinistro della casella di forbice.

</dd> <dt>

*y* 
</dt> <dd>

Coordinata y (asse orizzontale) per l'angolo inferiore sinistro della casella della forbice. Insieme, x e y specificano l'angolo inferiore sinistro della casella della forbice. Inizialmente (0,0).

</dd> <dt>

*width* 
</dt> <dd>

Larghezza della casella di forbice.

</dd> <dt>

*height* 
</dt> <dd>

Altezza della casella di forbice. Quando un contesto OpenGL *viene* collegato per  la prima volta a una *finestra,* la larghezza e l'altezza vengono impostate alle dimensioni di tale finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | La *larghezza o* *l'altezza* erano negative.<br/>                                                                                   |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glScissor** definisce un rettangolo, denominato casella di forbice, nelle coordinate della finestra. I primi due parametri, *x* *e y*, specificano l'angolo inferiore sinistro della casella. I *parametri width* e *height* specificano la larghezza e l'altezza della casella.

Il test della forbice è abilitato e disabilitato usando [**glEnable**](glenable.md) **e glDisable con** l'argomento GL \_ SCISSOR \_ TEST. Mentre il test della forbice è abilitato, solo i pixel che si trovano all'interno della casella di forbice possono essere modificati dai comandi di disegno. Le coordinate della finestra hanno valori interi agli angoli condivisi dei pixel framebuffer, quindi **glScissor**(0,0,1,1) consente la modifica solo del pixel inferiore sinistro nella finestra e **glScissor**(0,0,0,0)non consente la modifica di tutti i pixel nella finestra.

Quando il test della forbice è disabilitato, è come se la casella di forbice include l'intera finestra.

Le funzioni seguenti recuperano informazioni correlate **a glScissor**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ SCISSOR \_ BOX

[**glIsEnabled con**](glisenabled.md) argomento GL \_ SCISSOR \_ TEST

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

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





