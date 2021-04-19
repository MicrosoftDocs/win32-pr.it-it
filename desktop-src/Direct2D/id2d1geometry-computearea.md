---
title: Metodi ComputeArea di ID2D1Geometry
description: Calcola l'area della geometria.
ms.assetid: 655f11bc-7435-4d23-b4b1-3d7c2110aa48
keywords:
- Metodo ComputeArea Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: f6b79e8434a2174bcb05659f6656a46cc2d43cbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333514"
---
# <a name="id2d1geometrycomputearea-methods"></a>Metodi ID2D1Geometry:: ComputeArea

Calcola l'area della geometria.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                      | Descrizione                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComputeArea (D2D1 \_ Matrix \_ 3X2 \_ F&, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float))              | Calcola l'area della geometria dopo che è stata trasformata dalla matrice specificata e appiattita utilizzando la tolleranza predefinita.<br/>    |
| [**ComputeArea (D2D1 \_ Matrix \_ 3x2 \_ F \* , float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))             | Calcola l'area della geometria dopo che è stata trasformata dalla matrice specificata e appiattita utilizzando la tolleranza predefinita.<br/> |
| [**ComputeArea (D2D1 \_ Matrix \_ 3X2 \_ F&, float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float_float))  | Calcola l'area della geometria dopo che è stata trasformata dalla matrice specificata e appiattita utilizzando la tolleranza specificata.<br/>  |
| [**ComputeArea (D2D1 \_ Matrix \_ 3x2 \_ F \* , float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float)) | Calcola l'area della geometria dopo che è stata trasformata dalla matrice specificata e appiattita utilizzando la tolleranza specificata.<br/>  |



## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene usato **ComputeArea** per calcolare l'area di un cerchio specificato (**m \_ pCircleGeometry1**).


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
| Libreria<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

