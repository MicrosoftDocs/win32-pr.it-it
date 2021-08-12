---
title: Funzione glTexCoord3iv (Gl.h)
description: Imposta le coordinate della trama corrente. | Funzione glTexCoord3iv (Gl.h)
ms.assetid: 1d2f551a-d920-4020-bd51-bff28af83d44
keywords:
- Funzione glTexCoord3iv OpenGL
topic_type:
- apiref
api_name:
- glTexCoord3iv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50acbf96dda96d97ca6c570724b3fc29234d106478db3341a83516842bffdfaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118613770"
---
# <a name="gltexcoord3iv-function"></a>Funzione glTexCoord3iv

Imposta le coordinate della trama corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glTexCoord3iv(
   const GLint *v
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*v* 
</dt> <dd>

Puntatore a una matrice di tre elementi, che a sua volta specifica le coordinate della trama s, t e r.

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

 

 





