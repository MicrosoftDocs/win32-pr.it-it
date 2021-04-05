---
title: funzione glColorMask (GL. h)
description: La funzione glColorMask Abilita e Disabilita la scrittura di componenti colore del buffer dei frame.
ms.assetid: 23d7f94e-f290-423c-a841-f86caf94009d
keywords:
- funzione glColorMask OpenGL
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
ms.openlocfilehash: 3a9aa36eeceeae4aaa9373d73b50fda09663edb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873505"
---
# <a name="glcolormask-function"></a>glColorMask (funzione)

La funzione **glColorMask** Abilita e Disabilita la scrittura di componenti colore del buffer dei frame.

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

*Red* 
</dt> <dd>

Consente di specificare se è possibile o meno scrivere il colore rosso nel framebuffer. I valori predefiniti sono GL \_ true, a indicare che è possibile scrivere il componente color.

</dd> <dt>

*verde* 
</dt> <dd>

Specificare se è possibile o meno scrivere il colore verde nel framebuffer. Il valore predefinito è GL \_ true, a indicare che è possibile scrivere il componente color.

</dd> <dt>

*blu* 
</dt> <dd>

Consente di specificare se è possibile o meno scrivere il blu nel framebuffer. Il valore predefinito è GL \_ true, a indicare che è possibile scrivere il componente color.

</dd> <dt>

*Alfa* 
</dt> <dd>

Consente di specificare se è possibile o meno scrivere Alpha nel framebuffer. Il valore predefinito è GL \_ true, a indicare che è possibile scrivere il componente color.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glColorMask** specifica se i singoli componenti colore nel framebuffer possono o non possono essere scritti. Se il *colore rosso* è GL \_ false, ad esempio, non viene apportata alcuna modifica al componente rosso di qualsiasi pixel in uno dei buffer dei colori, indipendentemente dall'operazione di disegno tentata.

Non è possibile controllare le modifiche apportate a singoli bit di componenti. Le modifiche sono invece abilitate o disabilitate per interi componenti colore.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glColorMask**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Color \_ WRITEMASK

**glGet** con argomento GL \_ RGBA \_ mode

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glDepthMask**](gldepthmask.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glStencilMask**](glstencilmask.md)
</dt> </dl>

 

 





