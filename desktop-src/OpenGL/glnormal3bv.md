---
title: Funzione glNormal3bv (Gl.h)
description: Imposta il vettore normale corrente. | Funzione glNormal3bv (Gl.h)
ms.assetid: 1d9be974-93c9-45ac-89f1-92c14ff1c242
keywords:
- Funzione glNormal3bv OpenGL
topic_type:
- apiref
api_name:
- glNormal3bv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10578bbf22aa2cb0e3415715999018db4a3aefd39933cd802e1abbc196d5b706
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795605"
---
# <a name="glnormal3bv-function"></a>Funzione glNormal3bv

Imposta il vettore normale corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glNormal3bv(
   const GLbyte *v
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*v* 
</dt> <dd>

Puntatore a una matrice di tre elementi: le coordinate x, y e z della nuova normale corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La normale corrente viene impostata alle coordinate specificate ogni volta che si chiama **la funzione glNormal3bv.**

Gli argomenti byte, short o integer vengono convertiti nel formato a virgola mobile usando un mapping lineare che esegue il mapping del valore intero rappresentabile più positivo a 1,0 e del valore intero rappresentabile più negativo a -1,0.

Le normali specificate tramite **glNormal3bv** non devono avere una lunghezza di unità. Se la normalizzazione è abilitata, le normali specificate tramite **glNormal3bv** vengono normalizzate dopo la trasformazione. È possibile controllare la normalizzazione usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) con l'argomento GL \_ NORMALIZE. Per impostazione predefinita, la normalizzazione è disabilitata. È possibile aggiornare la normale corrente in qualsiasi momento. In particolare, è possibile chiamare **glNormal3bv** tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). Le funzioni seguenti recuperano informazioni correlate a **glNormal3bv**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ CURRENT \_ NORMAL

[**glIsEnable con**](glisenabled.md) l'argomento GL \_ NORMALIZE

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

[**glEnd**](glend.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





