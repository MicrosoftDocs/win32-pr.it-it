---
title: Funzione glNormal3d (Gl.h)
description: Imposta il vettore normale corrente. | Funzione glNormal3d (Gl.h)
ms.assetid: d256aef0-3ad5-4e70-b1c8-6402434b1e67
keywords:
- Funzione glNormal3d OpenGL
topic_type:
- apiref
api_name:
- glNormal3d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53eb5950b34b9f3fa838e773f7e3e6438caa603162ca8f8181534e67e8540191
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128191"
---
# <a name="glnormal3d-function"></a>Funzione glNormal3d

Imposta il vettore normale corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glNormal3d(
   GLdouble nx,
   GLdouble ny,
   GLdouble nz
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nx* 
</dt> <dd>

Specifica la coordinata x per il nuovo vettore normale corrente.

</dd> <dt>

*Ny* 
</dt> <dd>

Specifica la coordinata y per il nuovo vettore normale corrente.

</dd> <dt>

*Nz* 
</dt> <dd>

Specifica la coordinata z per il nuovo vettore normale corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La normale corrente viene impostata su coordinate specificate ogni volta che si chiama la **funzione glNormal3d.**

Gli argomenti byte, short o integer vengono convertiti in formato a virgola mobile usando un mapping lineare che esegue il mapping del valore integer rappresentabile più positivo a 1,0 e del valore integer rappresentabile più negativo a -1,0.

Le normali specificate tramite **glNormal3d** non devono avere lunghezza unità. Se la normalizzazione è abilitata, le normali specificate con **glNormal3d** vengono normalizzate dopo la trasformazione. È possibile controllare la normalizzazione usando [**glEnable**](glenable.md) e [**glDisable con**](gldisable.md) l'argomento GL \_ NORMALIZE. Per impostazione predefinita, la normalizzazione è disabilitata. È possibile aggiornare la normale corrente in qualsiasi momento. In particolare, è possibile chiamare **glNormal3d** tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). Le funzioni seguenti recuperano informazioni correlate a **glNormal3d**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ CURRENT \_ NORMAL

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

 

 





