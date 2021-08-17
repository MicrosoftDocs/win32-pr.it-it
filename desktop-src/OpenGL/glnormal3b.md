---
title: Funzione glNormal3b (Gl.h)
description: Imposta il vettore normale corrente. | Funzione glNormal3b (Gl.h)
ms.assetid: b6976143-bc9a-4766-9f7e-5380c3a24173
keywords:
- Funzione glNormal3b OpenGL
topic_type:
- apiref
api_name:
- glNormal3b
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff27f8082d384c5c244951b5dd237f21cb60875c0912cf742c4f8b2d3ea1f018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358694"
---
# <a name="glnormal3b-function"></a>Funzione glNormal3b

Imposta il vettore normale corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glNormal3b(
   GLbyte nx,
   GLbyte ny,
   GLbyte nz
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

La normale corrente viene impostata alle coordinate specificate ogni volta che si chiama **la funzione glNormal3b.**

Gli argomenti byte, short o integer vengono convertiti nel formato a virgola mobile usando un mapping lineare che esegue il mapping del valore intero rappresentabile più positivo a 1,0 e del valore intero rappresentabile più negativo a -1,0.

Le normali specificate con **glNormal3b** non devono avere lunghezza unità. Se la normalizzazione è abilitata, le normali specificate con **glNormal3b** vengono normalizzate dopo la trasformazione. È possibile controllare la normalizzazione usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) con l'argomento GL \_ NORMALIZE. Per impostazione predefinita, la normalizzazione è disabilitata. È possibile aggiornare la normale corrente in qualsiasi momento. In particolare, è possibile chiamare **glNormal3b** tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). Le funzioni seguenti recuperano informazioni correlate a **glNormal3b**:

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

 

 





