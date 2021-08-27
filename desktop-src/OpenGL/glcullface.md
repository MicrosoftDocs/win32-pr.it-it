---
title: Funzione glCullFace (Gl.h)
description: La funzione glCullFace specifica se è possibile eseguire il culled dei facet front-facing o back-facing.
ms.assetid: 53bf05b5-a68b-4d96-b4e7-2878a0a86a13
keywords:
- Funzione glCullFace OpenGL
topic_type:
- apiref
api_name:
- glCullFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70fd983e9a5921d96ba487f7eb8d6f631b000019e8ff566eb1ecc79e05ce4fb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081671"
---
# <a name="glcullface-function"></a>Funzione glCullFace

La **funzione glCullFace** specifica se è possibile eseguire il culled dei facet front-facing o back-facing.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glCullFace(
   GLenum mode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mode* 
</dt> <dd>

Specifica se i facet front-facing o back-facing sono candidati per il culling. Le costanti simboliche GL \_ FRONT, GL \_ BACK e GL FRONT AND BACK sono \_ \_ \_ accettate. Il valore predefinito è GL \_ BACK.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *mode* non è un valore accettato.<br/>                                                                                          |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glCullFace** specifica se i facet front-facing o back-facing vengono culled (come specificato dalla modalità *)* quando è abilitato il culling dei facet. È possibile abilitare e disabilitare il culling di facet [**usando glEnable**](glenable.md) [**e glDisable**](gldisable.md) con l'argomento GL \_ CULL \_ FACE. I facet includono triangoli, quadrilateri, poligoni e rettangoli.

La [**funzione glFrontFace**](glfrontface.md) specifica quali facet in senso orario e in senso antiorario sono rivolti all'inizio e all'indietro.

Se *mode* è GL FRONT E BACK, non viene disegnato alcun facet, ma vengono disegnate altre \_ primitive, ad esempio punti \_ \_ e linee.

Le funzioni seguenti recuperano informazioni correlate **a glCullFace:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ CULL \_ FACE \_ MODE

[**glIsEnabled con**](glisenabled.md) argomento GL \_ CULL \_ FACE

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFrontFace**](glfrontface.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





