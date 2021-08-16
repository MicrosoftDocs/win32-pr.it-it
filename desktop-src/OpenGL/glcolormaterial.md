---
title: Funzione glColorMaterial (Gl.h)
description: La funzione glColorMaterial fa in modo che un colore materiale rileva il colore corrente.
ms.assetid: 6dbef2c2-f902-4f25-8a87-9e3d710dd807
keywords:
- Funzione glColorMaterial OpenGL
topic_type:
- apiref
api_name:
- glColorMaterial
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55cc846cfbc400d2372186f9af4a09db08e5ad769d1e8fec5f5f6f757e1ff447
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360472"
---
# <a name="glcolormaterial-function"></a>Funzione glColorMaterial

La **funzione glColorMaterial** fa in modo che un colore materiale rileva il colore corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glColorMaterial(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Faccia* 
</dt> <dd>

Specifica se i parametri dei materiali anteriore, posteriore o anteriore e posteriore devono tenere traccia del colore corrente. I valori accettati sono GL \_ FRONT, GL \_ BACK e GL FRONT AND \_ \_ \_ BACK. Il valore predefinito è GL \_ FRONT \_ E \_ BACK.

</dd> <dt>

*mode* 
</dt> <dd>

Specifica quale dei diversi parametri di materiale tiene traccia del colore corrente. I valori accettati sono GL \_ EMISSION, GL \_ AMBIENT, GL \_ DIFFUSE, GL \_ SPECULAR e GL \_ AMBIENT \_ AND \_ DIFFUSE. Il valore predefinito è GL \_ AMBIENT \_ AND \_ DIFFUSE.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *face* o *mode* non è un valore accettato.<br/>                                                                                |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glColorMaterial** specifica i parametri del materiale che tiene traccia del colore corrente. Quando si abilita GL COLOR MATERIAL, per ogni materiale o materiale specificato da face , il parametro o i parametri del materiale specificati dalla modalità tiene traccia del colore \_ \_ corrente in qualsiasi momento.   Abilitare e disabilitare GL COLOR MATERIAL con le funzioni \_ \_ [**glEnable**](glenable.md) [**e glDisable,**](gldisable.md)chiamate con GL \_ COLOR MATERIAL come \_ argomento. Per impostazione predefinita, GL \_ COLOR \_ MATERIAL è disabilitato.

Con **glColorMaterial** è possibile modificare un subset di parametri di materiale per ogni vertice usando solo la funzione [**glColor,**](glcolor-functions.md) senza [**chiamare glMaterial.**](glmaterial-functions.md) Se si specifica solo un subset di parametri di questo tipo per ogni vertice, è meglio farlo con **glColorMaterial** che con **glMaterial**.

Le funzioni seguenti recuperano informazioni correlate **a glColorMaterial:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ COLOR \_ MATERIAL \_ PARAMETER

**glGet con** argomento GL \_ COLOR MATERIAL \_ \_ FACE

[**glIsEnabled con**](glisenabled.md) argomento GL \_ COLOR \_ MATERIAL

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





