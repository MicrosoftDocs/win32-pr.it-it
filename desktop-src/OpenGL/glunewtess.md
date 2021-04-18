---
title: funzione gluNewTess (Glu. h)
description: La funzione gluNewTess crea un oggetto a mosaico.
ms.assetid: dfc9fce8-ecab-493b-85ee-6d7487814186
keywords:
- funzione gluNewTess OpenGL
topic_type:
- apiref
api_name:
- gluNewTess
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0573ead0cf9b81568c4bf2101e317bef7faf148
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301458"
---
# <a name="glunewtess-function"></a>gluNewTess (funzione)

La funzione **gluNewTess** crea un oggetto a mosaico.

## <a name="syntax"></a>Sintassi


```C++
GLUtesselator* WINAPI gluNewTess(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="remarks"></a>Commenti

La funzione **gluNewTess** crea e restituisce un puntatore a un nuovo oggetto a mosaico. Fare riferimento a questo oggetto quando si chiamano le funzioni a mosaico. Un valore restituito pari a zero indica che la memoria disponibile non è sufficiente per allocare all'oggetto.

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

[**gluDeleteTess**](gludeletetess.md)
</dt> <dt>

[**gluTessBeginPolygon**](glubeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> </dl>

 

 





