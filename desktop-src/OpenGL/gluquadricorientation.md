---
title: funzione gluQuadricOrientation (Glu. h)
description: La funzione gluQuadricOrientation specifica l'orientamento all'interno o all'esterno di quadriche.
ms.assetid: 4e3fc6d3-5a39-455b-bd24-8eb497333096
keywords:
- funzione gluQuadricOrientation OpenGL
topic_type:
- apiref
api_name:
- gluQuadricOrientation
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05ffb1eeff199297943e678783731a26a38092a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739791"
---
# <a name="gluquadricorientation-function"></a>gluQuadricOrientation (funzione)

La funzione **gluQuadricOrientation** specifica l'orientamento all'interno o all'esterno di quadriche.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluQuadricOrientation(
   GLUquadric *quadObject,
   GLenum     orientation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*quadObject* 
</dt> <dd>

Oggetto quadrica (creato con [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*orientamento* 
</dt> <dd>

Orientamento desiderato. I valori seguenti sono validi.



| Valore                                                                                                                                                   | Significato                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="GLU_OUTSIDE"></span><span id="glu_outside"></span><dl> <dt>**GLU \_ esterno**</dt> </dl> | Creare quadriche con normali che puntano verso l'esterno. Si tratta del valore predefinito.<br/> |
| <span id="GLU_INSIDE"></span><span id="glu_inside"></span><dl> <dt>**GLU \_ all'interno**</dt> </dl>    | Creare quadriche con normali che puntano verso l'interno.<br/>                             |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **gluQuadricOrientation** specifica il tipo di orientamento desiderato per il rendering di quadriche con **quadObject**. L'interpretazione di verso l'esterno e verso l'interno dipende dal quadrica che si sta disegnando.

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

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluQuadricDrawStyle**](gluquadricdrawstyle.md)
</dt> <dt>

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





