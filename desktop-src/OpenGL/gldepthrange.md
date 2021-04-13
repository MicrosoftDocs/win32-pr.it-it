---
title: funzione glDepthRange (GL. h)
description: La funzione glDepthRange specifica il mapping dei valori z dalle coordinate del dispositivo normalizzate alle coordinate della finestra.
ms.assetid: 44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5
keywords:
- funzione glDepthRange OpenGL
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
ms.openlocfilehash: d0bd6a22ae91877c9b20fa5387edd9438942a07d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400422"
---
# <a name="gldepthrange-function"></a>glDepthRange (funzione)

La funzione **glDepthRange** specifica il mapping dei valori *z* dalle coordinate del dispositivo normalizzate alle coordinate della finestra.

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

Mapping del piano di ritaglio estremo alle coordinate della finestra. Il valore predefinito è 1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Dopo il ritaglio e la divisione per *w*, le coordinate *z* variano da 0,0 a 1,0, corrispondenti ai piani di ritaglio vicini e lontani. La funzione **glDepthRange** specifica un mapping lineare delle coordinate *z* normalizzate in questo intervallo alla finestra *z*-coordinates. Indipendentemente dall'implementazione effettiva del buffer di profondità, i valori di profondità delle coordinate della finestra vengono considerati come se fossero compresi tra 0,0 e 1,0 (ad esempio, i componenti dei colori). Pertanto, i valori accettati da **glDepthRange** vengono entrambi fissati a questo intervallo prima che vengano accettati.

Il mapping predefinito di (0, 1) esegue il mapping del piano vicino a 0 e del piano lontano a 1. Con questo mapping, l'intervallo di buffer di profondità viene utilizzato completamente.

Non è necessario che *zNear* sia minore di *zFar*. I mapping inversi, ad esempio (1, 0), sono accettabili.

La funzione seguente recupera le informazioni correlate a **glDepthRange**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con intervallo di \_ profondità GL argomento \_

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

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





