---
title: funzione gluLookAt (Glu. h)
description: La funzione gluLookAt definisce una trasformazione di visualizzazione.
ms.assetid: 1fd87701-19c2-49b9-99ac-10e70aaedbfd
keywords:
- funzione gluLookAt OpenGL
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
ms.openlocfilehash: 5866f3c06ef6969c95eeef4b23fff7a4e7852eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874614"
---
# <a name="glulookat-function"></a>gluLookAt (funzione)

La funzione **gluLookAt** definisce una trasformazione di visualizzazione.

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

Posizione del punto d'occhio.

</dd> <dt>

*eyey* 
</dt> <dd>

Posizione del punto d'occhio.

</dd> <dt>

*Eyez* 
</dt> <dd>

Posizione del punto d'occhio.

</dd> <dt>

*CenterX* 
</dt> <dd>

Posizione del punto di riferimento.

</dd> <dt>

*CenterY* 
</dt> <dd>

Posizione del punto di riferimento.

</dd> <dt>

*CenterZ* 
</dt> <dd>

Posizione del punto di riferimento.

</dd> <dt>

*UPX* 
</dt> <dd>

Direzione del vettore verso l'alto.

</dd> <dt>

*upy* 
</dt> <dd>

Direzione del vettore verso l'alto.

</dd> <dt>

*UPZ* 
</dt> <dd>

Direzione del vettore verso l'alto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **gluLookAt** crea una matrice di visualizzazione derivata da un punto d'occhio, un punto di riferimento che indica il centro della scena e un vettore up. La matrice esegue il mapping del punto di riferimento all'asse z negativo e il punto d'occhio all'origine, in modo che quando si usa una matrice di proiezione tipica, il centro della scena viene mappato al centro del viewport. Analogamente, la direzione descritta dal vettore up proiettata sul piano di visualizzazione viene mappata all'asse y positivo in modo che punti verso l'alto nel viewport. Il vettore up non deve essere parallelo alla linea di vista dall'occhio al punto di riferimento.

La matrice generata da **gluLookAt** moltiplica la matrice corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





