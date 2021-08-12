---
title: Funzione glTexCoord4s (Gl.h)
description: Imposta le coordinate della trama corrente. | Funzione glTexCoord4s (Gl.h)
ms.assetid: 948c63f5-a94d-4e55-9aa4-a320452fc29f
keywords:
- Funzione glTexCoord4s OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4s
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6e3ff71a0dcd48e22a1adee364343fcd7db5c80320a11bac3cf63402722110f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118613760"
---
# <a name="gltexcoord4s-function"></a>Funzione glTexCoord4s

Imposta le coordinate della trama corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glTexCoord4s(
   GLshort s,
   GLshort t,
   GLshort r,
   GLshort q
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

</dd> <dt>

*r* 
</dt> <dd>

Coordinata della trama r.

</dd> <dt>

*D* 
</dt> <dd>

Coordinata q della trama.

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

 

 





