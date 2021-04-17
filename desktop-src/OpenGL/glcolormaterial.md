---
title: funzione glColorMaterial (GL. h)
description: La funzione glColorMaterial fa sì che un colore del materiale tenga traccia del colore corrente.
ms.assetid: 6dbef2c2-f902-4f25-8a87-9e3d710dd807
keywords:
- funzione glColorMaterial OpenGL
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
ms.openlocfilehash: d32823eaa82e6a260790dd6fa23747f2b4228649
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400706"
---
# <a name="glcolormaterial-function"></a>glColorMaterial (funzione)

La funzione **glColorMaterial** fa sì che un colore del materiale tenga traccia del colore corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glColorMaterial(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*faccia* 
</dt> <dd>

Specifica se i parametri del materiale anteriore, posteriore o anteriore e posteriore devono tenere traccia del colore corrente. I valori accettati sono GL \_ Front, GL \_ back e GL \_ front \_ e \_ back. Il valore predefinito è GL \_ front \_ e \_ back.

</dd> <dt>

*mode* 
</dt> <dd>

Specifica quali dei diversi parametri del materiale tengono traccia del colore corrente. I valori accettati sono GL \_ Emission, GL \_ ambient, GL Diffusion, GL \_ \_ Specular e GL \_ ambient \_ e \_ Diffusion. Il valore predefinito è GL \_ ambient \_ e \_ Diffusion.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | il tipo *o la* *modalità* non è un valore accettato.<br/>                                                                                |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glColorMaterial** specifica i parametri del materiale che tengono traccia del colore corrente. Quando si Abilita il \_ \_ materiale del colore GL, per ogni materiale o materiale specificato da *Face*, il parametro Material o i parametri specificati in *modalità* tengono sempre traccia del colore corrente. Abilitare e disabilitare \_ \_ il materiale di colore GL con le funzioni [**glEnable**](glenable.md) e [**glDisable**](gldisable.md), che è possibile chiamare con il \_ materiale di colore GL \_ come argomento. Per impostazione predefinita, \_ il \_ materiale colore GL è disabilitato.

Con **glColorMaterial** è possibile modificare un subset di parametri Material per ogni vertice usando solo la funzione [**glColor**](glcolor-functions.md) , senza chiamare [**glMaterial**](glmaterial-functions.md). Se si prevede di specificare solo un subset di parametri per ogni vertice, è preferibile farlo con **glColorMaterial** che con **glMaterial**.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glColorMaterial**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con parametro del \_ materiale colore GL argomento \_ \_

**glGet** con argomento del \_ colore del \_ materiale GL \_

[**glIsEnabled**](glisenabled.md) con argomento relativo al \_ colore del \_ materiale GL

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**Remo**](glend.md)
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

 

 





