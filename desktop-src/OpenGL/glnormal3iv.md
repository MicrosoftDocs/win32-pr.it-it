---
title: funzione glNormal3iv (GL. h)
description: Imposta il vettore normale corrente. | funzione glNormal3iv (GL. h)
ms.assetid: cf50e801-a34c-43bd-b7eb-facb84a6472d
keywords:
- funzione glNormal3iv OpenGL
topic_type:
- apiref
api_name:
- glNormal3iv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5629a12d6c388da2aa133fbe72177646b4f95d63
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969266"
---
# <a name="glnormal3iv-function"></a>glNormal3iv (funzione)

Imposta il vettore normale corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glNormal3iv(
   const GLint *v
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*v* 
</dt> <dd>

Puntatore a una matrice di tre elementi, ovvero le coordinate x, y e z della nuova normale corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Il normale corrente viene impostato sulle coordinate specificate ogni volta che si chiama la funzione **glNormal3iv**.

Gli argomenti byte, short o Integer vengono convertiti in formato a virgola mobile con un mapping lineare che esegue il mapping del valore intero rappresentabile più positivo a 1,0 e il valore intero rappresentabile più negativo a-1,0.

I normali specificati tramite **glNormal3iv** non devono avere la lunghezza dell'unità. Se la normalizzazione è abilitata, le normali specificate con **glNormal3iv** vengono normalizzate dopo la trasformazione. È possibile controllare la normalizzazione usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) con l'argomento GL \_ Normalize. Per impostazione predefinita, la normalizzazione è disabilitata. È possibile aggiornare la normale corrente in qualsiasi momento. In particolare, è possibile chiamare **glNormal3iv** tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). Le funzioni seguenti consentono di recuperare informazioni correlate a **glNormal3iv**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ Normal

[**glIsEnable**](glisenabled.md) con argomento GL \_ Normalize

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





