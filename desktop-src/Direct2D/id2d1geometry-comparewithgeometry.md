---
title: Metodi ID2D1Geometry CompareWithGeometry
description: Descrive l'intersezione tra questa geometria e la geometria specificata.
ms.assetid: 75ddd674-b50b-4d34-b291-9e7e65828304
keywords:
- Metodi CompareWithGeometry Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 09978c38c3e4be7ad8a86ccfccb43387ed4ac48232e39e1ed19001d806362c88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119304801"
---
# <a name="id2d1geometrycomparewithgeometry-methods"></a>Metodi ID2D1Geometry::CompareWithGeometry

Descrive l'intersezione tra questa geometria e la geometria specificata.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                            | Descrizione                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CompareWithGeometry(ID2D1Geometry \* ,D2D1 \_ MATRIX \_ 3X2 \_ F&,D2D1 \_ GEOMETRY RELATION \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f__d2d1_geometry_relation))              | Descrive l'intersezione tra questa geometria e la geometria specificata. Il confronto viene eseguito usando la tolleranza di appiattimento predefinita.<br/>      |
| [**CompareWithGeometry(ID2D1Geometry \* ,D2D1 \_ MATRIX \_ 3X2 \_ F \* ,D2D1 \_ GEOMETRY RELATION \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f_d2d1_geometry_relation))             | Descrive l'intersezione tra questa geometria e la geometria specificata. Il confronto viene eseguito usando la tolleranza di appiattimento predefinita.<br/>      |
| [**CompareWithGeometry(ID2D1Geometry \* ,D2D1 \_ MATRIX \_ 3X2 \_ F&,FLOAT,D2D1 \_ GEOMETRY RELATION \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f__float_d2d1_geometry_relation))  | Descrive l'intersezione tra questa geometria e la geometria specificata. Il confronto viene eseguito usando la tolleranza di appiattimento specificata.<br/>    |
| [**CompareWithGeometry(ID2D1Geometry \* ,D2D1 \_ MATRIX \_ 3X2 \_ \* F,FLOAT,D2D1 \_ GEOMETRY RELATION \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f_float_d2d1_geometry_relation)) | Descrive l'intersezione tra questa geometria e la geometria specificata. Il confronto viene eseguito utilizzando la tolleranza di appiattimento specificata.<br/> |



## <a name="remarks"></a>Commenti

Quando si interpreta  il valore di relazione restituito, è importante ricordare che il membro [**D2D1 \_ GEOMETRY RELATION \_ \_ IS \_ CONTAINED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) del tipo di enumerazione **D2D1 \_ GEOMETRY \_ RELATION** significa che questa geometria è contenuta all'interno di *inputGeometry*, non che questa geometria contiene *inputGeometry*.

Per altre informazioni su come interpretare altri possibili valori restituiti, vedere [**D2D1 \_ GEOMETRY \_ RELATION.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

