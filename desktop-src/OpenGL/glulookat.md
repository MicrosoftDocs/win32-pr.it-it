---
title: Funzione gluLookAt (Glu.h)
description: La funzione gluLookAt definisce una trasformazione di visualizzazione.
ms.assetid: 1fd87701-19c2-49b9-99ac-10e70aaedbfd
keywords:
- Funzione gluLookAt OpenGL
topic_type:
- apiref
api_name:
- gluLookAt
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b21d0cb2fac6573ab2999eb96b2af8b1ecb670f4e51d1ffd2ad91ba001c9ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675301"
---
# <a name="glulookat-function"></a>Funzione gluLookAt

La **funzione gluLookAt** definisce una trasformazione di visualizzazione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluLookAt(
   GLdouble eyex,
   GLdouble eyey,
   GLdouble eyez,
   GLdouble centerx,
   GLdouble centery,
   GLdouble centerz,
   GLdouble upx,
   GLdouble upy,
   GLdouble upz
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*eyex* 
</dt> <dd>

Posizione del punto dell'occhio.

</dd> <dt>

*eyey* 
</dt> <dd>

Posizione del punto dell'occhio.

</dd> <dt>

*eyez* 
</dt> <dd>

Posizione del punto dell'occhio.

</dd> <dt>

*Centerx* 
</dt> <dd>

Posizione del punto di riferimento.

</dd> <dt>

*Centery* 
</dt> <dd>

Posizione del punto di riferimento.

</dd> <dt>

*centerz* 
</dt> <dd>

Posizione del punto di riferimento.

</dd> <dt>

*Upx* 
</dt> <dd>

Direzione del vettore verso l'alto.

</dd> <dt>

*upy* 
</dt> <dd>

Direzione del vettore verso l'alto.

</dd> <dt>

*Upz* 
</dt> <dd>

Direzione del vettore verso l'alto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione gluLookAt** crea una matrice di visualizzazione derivata da un punto dell'occhio, un punto di riferimento che indica il centro della scena e un vettore verso l'alto. La matrice esegue il mapping del punto di riferimento all'asse z negativo e del punto dell'occhio all'origine, in modo che quando si usa una tipica matrice di proiezione, il centro della scena viene mappato al centro del viewport. Analogamente, la direzione descritta dal vettore verso l'alto proiettata sul piano di visualizzazione viene mappata all'asse y positivo in modo che punti verso l'alto nel viewport. Il vettore up non deve essere parallelo alla linea di vista dall'occhio al punto di riferimento.

La matrice generata da **gluLookAt** postmultipla la matrice corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





