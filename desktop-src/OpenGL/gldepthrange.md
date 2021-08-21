---
title: Funzione glDepthRange (Gl.h)
description: La funzione glDepthRange specifica il mapping dei valori z dalle coordinate del dispositivo normalizzate alle coordinate della finestra.
ms.assetid: 44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5
keywords:
- Funzione glDepthRange OpenGL
topic_type:
- apiref
api_name:
- glDepthRange
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ac72155449e70a59265e4ffd2576245059a547906092df2a932e84f221e48fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081651"
---
# <a name="gldepthrange-function"></a>Funzione glDepthRange

La **funzione glDepthRange** specifica il mapping dei valori *z* dalle coordinate del dispositivo normalizzate alle coordinate della finestra.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glDepthRange(
   GLclampd zNear,
   GLclampd zFar
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*zNear* 
</dt> <dd>

Mapping del piano di ritaglio vicino alle coordinate della finestra. Il valore predefinito è zero.

</dd> <dt>

*zFar* 
</dt> <dd>

Mapping del piano di ritaglio lontano alle coordinate della finestra. Il valore predefinito è 1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Dopo il ritaglio e la divisione per *w*, le coordinate *z* sono da 0,0 a 1,0, corrispondenti ai piani di ritaglio vicino e lontano. La **funzione glDepthRange** specifica un mapping lineare delle coordinate *z* normalizzate in questo intervallo alle coordinate *z* della finestra. Indipendentemente dall'implementazione effettiva del buffer di profondità, i valori di profondità delle coordinate della finestra vengono considerati come se fossero da 0,0 a 1,0 (ad esempio componenti di colore). Di conseguenza, i valori accettati **da glDepthRange** vengono entrambi a questo intervallo prima che siano accettati.

Il mapping predefinito di (0,1) esegue il mapping del piano vicino a 0 e del piano lontano a 1. Con questo mapping, l'intervallo di buffer di profondità viene completamente utilizzato.

Non è necessario che *zNear* sia minore di *zFar*. I mapping inversa, ad esempio (1,0), sono accettabili.

La funzione seguente recupera le informazioni correlate a **glDepthRange**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ DEPTH \_ RANGE

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

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





