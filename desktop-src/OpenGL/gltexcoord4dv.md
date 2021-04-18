---
title: funzione glTexCoord4dv (GL. h)
description: Imposta le coordinate di trama correnti. | funzione glTexCoord4dv (GL. h)
ms.assetid: 43d3fb1c-c1cf-4f81-aac2-24a5b4c5b29d
keywords:
- funzione glTexCoord4dv OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4dv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7b2ffb9f14ad0827ff37e4dd057892eb5abea8a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321512"
---
# <a name="gltexcoord4dv-function"></a>glTexCoord4dv (funzione)

Imposta le coordinate di trama correnti.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glTexCoord4dv(
   const GLdouble *v
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*v* 
</dt> <dd>

Puntatore a una matrice di quattro elementi, che a sua volta specifica le coordinate di trama s, t, r e q.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione [**glTexCoord**](gltexcoord-functions.md) imposta le coordinate di trama correnti che fanno parte dei dati associati ai vertici del poligono. La funzione **glTexCoord** specifica le coordinate di trama in una, due, tre o quattro dimensioni. La funzione glTexCoord1 imposta le coordinate di trama correnti su (s, 0, 0, 1); una chiamata a glTexCoord2 le imposta su (s, t, 0, 1). Analogamente, glTexCoord3 specifica le coordinate di trama come (s, t, r, 1) e glTexCoord4 definisce tutti e quattro i componenti in modo esplicito come (s, t, r, q). È possibile aggiornare le coordinate di trama correnti in qualsiasi momento. In particolare, è possibile chiamare glTexCoord tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). La funzione seguente recupera le informazioni correlate a **glTexCoord**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ \_ coordinate di trama correnti \_

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

[glVertex](glvertex-functions.md)
</dt> </dl>

 

 





