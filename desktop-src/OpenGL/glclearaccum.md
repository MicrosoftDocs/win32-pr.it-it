---
title: funzione glClearAccum (GL. h)
description: La funzione glClearAccum specifica i valori Clear per il buffer di accumulo.
ms.assetid: 77d8f340-be47-43f4-96fc-31025a4c8b4e
keywords:
- funzione glClearAccum OpenGL
topic_type:
- apiref
api_name:
- glClearAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3098e87a47509b8c05035171a8f31e57d8618424
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120070"
---
# <a name="glclearaccum-function"></a>glClearAccum (funzione)

La funzione **glClearAccum** specifica i valori Clear per il buffer di accumulo.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glClearAccum(
   GLfloat red,
   GLfloat green,
   GLfloat blue,
   GLfloat alpha
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Red* 
</dt> <dd>

Valore rosso utilizzato quando il buffer di accumulo viene cancellato. Il valore predefinito è zero.

</dd> <dt>

*verde* 
</dt> <dd>

Valore verde utilizzato quando il buffer di accumulo viene cancellato. Il valore predefinito è zero.

</dd> <dt>

*blu* 
</dt> <dd>

Valore blu utilizzato quando il buffer di accumulo viene cancellato. Il valore predefinito è zero.

</dd> <dt>

*Alfa* 
</dt> <dd>

Valore alfa utilizzato quando il buffer di accumulo viene cancellato. Il valore predefinito è zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glClearAccum** specifica i valori rosso, verde, blu e alfa usati da [**glClear**](glclear.md) per cancellare il buffer di accumulo.

I valori specificati da **glClearAccum** vengono bloccati nell'intervallo \[ 1, 1 \] .

La funzione seguente recupera le informazioni correlate a **glClearAccum**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con l'argomento contabilità GL \_ \_ Clear \_ value

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

[**glClear**](glclear.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





