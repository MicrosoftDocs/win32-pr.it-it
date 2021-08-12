---
title: Funzione glTexCoord1f (Gl.h)
description: Imposta le coordinate della trama corrente. | Funzione glTexCoord1f (Gl.h)
ms.assetid: 9b7e361a-ce3f-4014-af33-490b1edf2c68
keywords:
- Funzione glTexCoord1f OpenGL
topic_type:
- apiref
api_name:
- glTexCoord1f
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0090551f7faa3ba67edd0fea27065d92e95546a8439735fc89fd9524db0b4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118614062"
---
# <a name="gltexcoord1f-function"></a>Funzione glTexCoord1f

Imposta le coordinate della trama corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glTexCoord1f(
   GLfloat s
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*s* 
</dt> <dd>

Coordinata della trama s.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La [**funzione glTexCoord**](gltexcoord-functions.md) imposta le coordinate di trama correnti che fanno parte dei dati associati ai vertici del poligono. La **funzione glTexCoord** specifica le coordinate della trama in una, due, tre o quattro dimensioni. La funzione glTexCoord1 imposta le coordinate di trama correnti su (s, 0, 0, 1); una chiamata a glTexCoord2 li imposta su (s, t, 0, 1). Analogamente, glTexCoord3 specifica le coordinate della trama come (s, t, r, 1) e glTexCoord4 definisce tutti e quattro i componenti in modo esplicito come (s, t, r, q). È possibile aggiornare le coordinate di trama correnti in qualsiasi momento. In particolare, è possibile chiamare glTexCoord tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). La funzione seguente recupera le informazioni correlate a **glTexCoord:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ CURRENT TEXTURE \_ \_ COORDS

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

[glVertex](glvertex-functions.md)
</dt> </dl>

 

 





