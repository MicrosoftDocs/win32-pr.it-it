---
title: Funzione glNormal3s (Gl.h)
description: Imposta il vettore normale corrente. | Funzione glNormal3s (Gl.h)
ms.assetid: 4fd98ad5-266d-4ef1-9c1f-2b5166ee65d7
keywords:
- Funzione glNormal3s OpenGL
topic_type:
- apiref
api_name:
- glNormal3s
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a21ce2ff4c780e19e0849730db5fb7831343a32961e0e673b355124f799c61c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795254"
---
# <a name="glnormal3s-function"></a>Funzione glNormal3s

Imposta il vettore normale corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glNormal3s(
   GLshort nx,
   GLshort ny,
   GLshort nz
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nx* 
</dt> <dd>

Specifica la coordinata x del nuovo vettore normale corrente.

</dd> <dt>

*Ny* 
</dt> <dd>

Specifica la coordinata y del nuovo vettore normale corrente.

</dd> <dt>

*Nz* 
</dt> <dd>

Specifica la coordinata z del nuovo vettore normale corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La normale corrente viene impostata su coordinate specificate ogni volta che si chiama la **funzione glNormal3s.**

Gli argomenti byte, short o integer vengono convertiti in formato a virgola mobile con un mapping lineare che esegue il mapping del valore integer rappresentabile più positivo a 1,0 e del valore intero rappresentabile più negativo a -1,0.

Le normali specificate tramite **glNormal3s** non devono avere una lunghezza di unità. Se la normalizzazione è abilitata, le normali specificate con **glNormal3s** vengono normalizzate dopo la trasformazione. È possibile controllare la normalizzazione usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) con l'argomento GL \_ NORMALIZE. Per impostazione predefinita, la normalizzazione è disabilitata. È possibile aggiornare la normale corrente in qualsiasi momento. In particolare, è possibile chiamare **glNormal3s** tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). Le funzioni seguenti recuperano informazioni correlate **a glNormal3s:**

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

 

 





