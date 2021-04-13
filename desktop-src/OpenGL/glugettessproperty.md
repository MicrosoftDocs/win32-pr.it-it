---
title: funzione gluGetTessProperty (Glu. h)
description: La funzione gluGetTessProperty ottiene una proprietà dell'oggetto mosaico.
ms.assetid: 6aa565d8-2257-4259-a959-b7d806a7ed96
keywords:
- funzione gluGetTessProperty OpenGL
topic_type:
- apiref
api_name:
- gluGetTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482f32b227dbcf0c2a62405e344aa719bb4b9e17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400524"
---
# <a name="glugettessproperty-function"></a>gluGetTessProperty (funzione)

La funzione **gluGetTessProperty** ottiene una proprietà dell'oggetto mosaico.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluGetTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tess* 
</dt> <dd>

Oggetto a mosaico creato con [**gluNewTess**](glunewtess.md).

</dd> <dt>

*che* 
</dt> <dd>

Proprietà di cui è necessario recuperare il valore. Sono validi i valori seguenti: \_ regola di Winding di Glu Tess \_ \_ , Glu \_ Tess \_ \_ solo limite e Glu \_ Tess \_ tolerance.

</dd> <dt>

*value* 
</dt> <dd>

Puntatore alla posizione in cui viene scritto il valore della proprietà denominata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Utilizzare **gluGetTessProperty** per recuperare le proprietà archiviate in un oggetto a mosaico. Queste proprietà influiscono sulla modalità di interpretazione e rendering degli oggetti a mosaico. Per informazioni sulle proprietà e sulle operazioni eseguite, vedere [**gluTessProperty**](glutessproperty.md).

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

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessProperty**](glutessproperty.md)
</dt> </dl>

 

 





