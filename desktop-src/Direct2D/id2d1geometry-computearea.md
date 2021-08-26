---
title: Metodi ID2D1Geometry ComputeArea
description: Calcola l'area della geometria.
ms.assetid: 655f11bc-7435-4d23-b4b1-3d7c2110aa48
keywords:
- Metodi ComputeArea Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 344cb55314c3cafc2e84479944342633c74bd5a35754c9f7a4f6d53a30da58fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044171"
---
# <a name="id2d1geometrycomputearea-methods"></a>Metodi ID2D1Geometry::ComputeArea

Calcola l'area della geometria.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                      | Descrizione                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComputeArea(D2D1 \_ MATRIX \_ 3X2 \_ F&,FLOAT \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float))              | Calcola l'area della geometria dopo che è stata trasformata dalla matrice specificata e appiattita usando la tolleranza predefinita.<br/>    |
| [**ComputeArea(D2D1 \_ MATRIX \_ 3X2 \_ \* F,FLOAT \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))             | Calcola l'area della geometria dopo che è stata trasformata dalla matrice specificata e appiattita usando la tolleranza predefinita.<br/> |
| [**ComputeArea(D2D1 \_ MATRIX \_ 3X2 \_ F&,FLOAT,FLOAT \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float_float))  | Calcola l'area della geometria dopo che è stata trasformata dalla matrice specificata e appiattita usando la tolleranza specificata.<br/>  |
| [**ComputeArea(D2D1 \_ MATRIX \_ 3X2 \_ \* F,FLOAT,FLOAT \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float)) | Calcola l'area della geometria dopo che è stata trasformata dalla matrice specificata e appiattita usando la tolleranza specificata.<br/>  |



## <a name="examples"></a>Esempio

L'esempio di codice seguente usa **ComputeArea** per calcolare l'area di un cerchio specificato (**m \_ pCircleGeometry1**).


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

