---
title: Funzione glColorMask (Gl.h)
description: La funzione glColorMask abilita e disabilita la scrittura di componenti di colore del buffer di frame.
ms.assetid: 23d7f94e-f290-423c-a841-f86caf94009d
keywords:
- Funzione glColorMask OpenGL
topic_type:
- apiref
api_name:
- glColorMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e8b3e9e00eaa294f77813f8e994358cbb473fc4e5c02fce8e5115dc517cae20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081721"
---
# <a name="glcolormask-function"></a>Funzione glColorMask

La **funzione glColorMask** abilita e disabilita la scrittura di componenti di colore del buffer di frame.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glColorMask(
   GLboolean red,
   GLboolean green,
   GLboolean blue,
   GLboolean alpha
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Rosso* 
</dt> <dd>

Specificare se il rosso può o non può essere scritto nel framebuffer. I valori predefiniti sono GL TRUE, a indicare che è possibile scrivere il \_ componente colore.

</dd> <dt>

*Verde* 
</dt> <dd>

Specificare se il verde può o non può essere scritto nel framebuffer. Il valore predefinito è GL TRUE, che indica che è possibile scrivere il \_ componente colore.

</dd> <dt>

*Blu* 
</dt> <dd>

Specificare se il blu può o non può essere scritto nel framebuffer. Il valore predefinito è GL TRUE, che indica che è possibile scrivere il \_ componente colore.

</dd> <dt>

*Alfa* 
</dt> <dd>

Specificare se alpha può o non può essere scritto nel framebuffer. Il valore predefinito è GL TRUE, che indica che è possibile scrivere il \_ componente colore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glColorMask** specifica se i singoli componenti di colore nel framebuffer possono o non possono essere scritti. Se *rosso* è GL FALSE, ad esempio, non viene apportata alcuna modifica al componente rosso di qualsiasi pixel in uno dei buffer di colore, indipendentemente dall'operazione \_ di disegno tentata.

Le modifiche ai singoli bit di componenti non possono essere controllate. Le modifiche vengono invece abilitate o disabilitate per interi componenti di colore.

Le funzioni seguenti recuperano informazioni correlate a **glColorMask**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ COLOR \_ WRITEMASK

**glGet con** argomento GL \_ RGBA \_ MODE

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glDepthMask**](gldepthmask.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glStencilMask**](glstencilmask.md)
</dt> </dl>

 

 





