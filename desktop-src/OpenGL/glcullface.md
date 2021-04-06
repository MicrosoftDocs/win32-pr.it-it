---
title: funzione glCullFace (GL. h)
description: La funzione glCullFace specifica se i facet front-end o back-facet possono essere rivolti.
ms.assetid: 53bf05b5-a68b-4d96-b4e7-2878a0a86a13
keywords:
- funzione glCullFace OpenGL
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
ms.openlocfilehash: 1c20370e0fa8bcf746d1b835ee45725f76158fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963871"
---
# <a name="glcullface-function"></a>glCullFace (funzione)

La funzione **glCullFace** specifica se i facet front-end o back-facet possono essere rivolti.

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

Specifica se i facet front-end o back-facing sono candidati per l'eliminazione. Vengono accettate le costanti simboliche GL \_ Front, GL \_ back e GL \_ front \_ e \_ back. Il valore predefinito è GL \_ back.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | la *modalità* non è un valore accettato.<br/>                                                                                          |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glCullFace** specifica se i facet front-end o back-facet vengono abbattuti (come specificato dalla *modalità*) quando è abilitata l'eliminazione dei facet. È possibile abilitare e disabilitare l'abbattimento dei facet usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) con la \_ faccia di abbattimento GL dell'argomento \_ . I facet includono triangoli, quadrilateri, poligoni e rettangoli.

La funzione [**glFrontFace**](glfrontface.md) specifica quale dei facet in senso orario e in senso antiorario sono rivolti verso il lato anteriore e posteriore.

Se la *modalità* è GL \_ front \_ e \_ back, non viene disegnato alcun facet, ma vengono disegnate altre primitive, ad esempio punti e linee.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glCullFace**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con la \_ modalità della \_ faccia abbattimento GL argomento \_

[**glIsEnabled**](glisenabled.md) con l'argomento relativo alla selezione degli \_ argomenti GL \_

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glFrontFace**](glfrontface.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





