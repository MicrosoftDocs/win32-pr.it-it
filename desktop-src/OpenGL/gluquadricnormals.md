---
title: funzione gluQuadricNormals (Glu. h)
description: La funzione gluQuadricNormals specifica il tipo di normali da usare per quadriche.
ms.assetid: 945759ec-ed4a-480f-8243-49fc785867c1
keywords:
- funzione gluQuadricNormals OpenGL
topic_type:
- apiref
api_name:
- gluQuadricNormals
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f11f9d8cd1884d7a5d1bc4cd03797517ba484126
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478017"
---
# <a name="gluquadricnormals-function"></a>gluQuadricNormals (funzione)

La funzione **gluQuadricNormals** specifica il tipo di normali da usare per quadriche.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluQuadricNormals(
   GLUquadric *quadObject,
   GLenum     normals
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*quadObject* 
</dt> <dd>

Oggetto quadrica (creato con [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*normali* 
</dt> <dd>

Tipo desiderato di normali. I valori seguenti sono validi.



| Valore                                                                                                                                                | Significato                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="GLU_NONE"></span><span id="glu_none"></span><dl> <dt>**GLU \_ None**</dt> </dl>       | Non viene generato alcun normale.<br/>                                                         |
| <span id="GLU_FLAT"></span><span id="glu_flat"></span><dl> <dt>**GLU \_ Flat**</dt> </dl>       | Viene generato un normale per ogni facet di un quadrica.<br/>                             |
| <span id="GLU_SMOOTH"></span><span id="glu_smooth"></span><dl> <dt>**GLU \_ smussato**</dt> </dl> | Viene generato un normale per ogni vertice di un quadrica. Si tratta del valore predefinito.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **gluQuadricNormals** specifica il tipo di normali da usare per il rendering quadriche con **quadObject**.

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

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





