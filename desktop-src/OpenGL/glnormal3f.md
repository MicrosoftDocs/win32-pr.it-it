---
title: Funzione glNormal3f (Gl.h)
description: Imposta il vettore normale corrente. | Funzione glNormal3f (Gl.h)
ms.assetid: 8407996e-47fd-4c30-91f6-53d4341a1fca
keywords:
- Funzione glNormal3f OpenGL
topic_type:
- apiref
api_name:
- glNormal3f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de6edaab0f83c9b05a561eb8f857086fea76f41a84a4869d5d9f99149482df1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128151"
---
# <a name="glnormal3f-function"></a>Funzione glNormal3f

Imposta il vettore normale corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glNormal3f(
   GLfloat nx,
   GLfloat ny,
   GLfloat nz
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

La normale corrente viene impostata su coordinate specificate ogni volta che si chiama **la funzione glNormal3f.**

Gli argomenti byte, short o integer vengono convertiti in formato a virgola mobile con un mapping lineare che esegue il mapping del valore integer rappresentabile più positivo a 1,0 e del valore intero rappresentabile più negativo a -1,0.

Le normali specificate tramite **glNormal3f** non devono avere una lunghezza di unità. Se la normalizzazione è abilitata, le normali specificate con **glNormal3f** vengono normalizzate dopo la trasformazione. È possibile controllare la normalizzazione usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) con l'argomento GL \_ NORMALIZE. Per impostazione predefinita, la normalizzazione è disabilitata. È possibile aggiornare la normale corrente in qualsiasi momento. In particolare, è possibile chiamare **glNormal3f** tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). Le funzioni seguenti recuperano informazioni correlate **a glNormal3f**:

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

 

 





