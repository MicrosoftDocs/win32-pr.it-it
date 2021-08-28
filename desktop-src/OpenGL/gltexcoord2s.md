---
title: Funzione glTexCoord2s (Gl.h)
description: Imposta le coordinate della trama corrente. | Funzione glTexCoord2s (Gl.h)
ms.assetid: d1bd7286-e32e-43ef-919a-4debf62a50ef
keywords:
- Funzione glTexCoord2s OpenGL
topic_type:
- apiref
api_name:
- glTexCoord2s
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f53c1900727044fc1499ad6de3557f30270e7136a30e493fa3b522b7d7effb0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491171"
---
# <a name="gltexcoord2s-function"></a>Funzione glTexCoord2s

Imposta le coordinate della trama corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glTexCoord2s(
   GLshort s,
   GLshort t
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*s* 
</dt> <dd>

Coordinata della trama.

</dd> <dt>

*t* 
</dt> <dd>

Coordinata della trama t.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La [**funzione glTexCoord**](gltexcoord-functions.md) imposta le coordinate di trama correnti che fanno parte dei dati associati ai vertici poligoni. La **funzione glTexCoord** specifica le coordinate di trama in una, due, tre o quattro dimensioni. La funzione glTexCoord1 imposta le coordinate di trama correnti su (s, 0, 0, 1); una chiamata a glTexCoord2 li imposta su (s, t, 0, 1). Analogamente, glTexCoord3 specifica le coordinate della trama come (s, t, r, 1) e glTexCoord4 definisce tutti e quattro i componenti in modo esplicito come (s, t, r, q). È possibile aggiornare le coordinate di trama correnti in qualsiasi momento. In particolare, è possibile chiamare glTexCoord tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). La funzione seguente recupera le informazioni correlate **a glTexCoord:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ CURRENT \_ TEXTURE \_ COORDS

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

 

 





