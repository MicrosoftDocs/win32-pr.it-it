---
title: Metodi CompareWithGeometry di ID2D1Geometry
description: Descrive l'intersezione tra la geometria e la geometria specificata.
ms.assetid: 75ddd674-b50b-4d34-b291-9e7e65828304
keywords:
- Metodo CompareWithGeometry Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: eee64e51d4717a9fe0983be849c78f99602cac9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333515"
---
# <a name="id2d1geometrycomparewithgeometry-methods"></a>Metodi ID2D1Geometry:: CompareWithGeometry

Descrive l'intersezione tra la geometria e la geometria specificata.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                            | Descrizione                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CompareWithGeometry (ID2D1Geometry \* , d2d1 \_ Matrix \_ 3x2 \_ F&, d2d1 \_ Geometry \_ Relation \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f__d2d1_geometry_relation))              | Descrive l'intersezione tra la geometria e la geometria specificata. Il confronto viene eseguito usando la tolleranza di Flat predefinita.<br/>      |
| [**CompareWithGeometry (ID2D1Geometry \* , d2d1 \_ Matrix \_ 3x2 \_ F \* , d2d1 \_ Geometry \_ Relation \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f_d2d1_geometry_relation))             | Descrive l'intersezione tra la geometria e la geometria specificata. Il confronto viene eseguito usando la tolleranza di Flat predefinita.<br/>      |
| [**CompareWithGeometry (ID2D1Geometry \* , d2d1 \_ Matrix \_ 3x2 \_ F&, float, d2d1 \_ Geometry \_ Relation \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f__float_d2d1_geometry_relation))  | Descrive l'intersezione tra la geometria e la geometria specificata. Il confronto viene eseguito usando la tolleranza di Flat specificata.<br/>    |
| [**CompareWithGeometry (ID2D1Geometry \* , d2d1 \_ Matrix \_ 3x2 \_ F \* , float, d2d1 \_ Geometry \_ Relation \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f_float_d2d1_geometry_relation)) | Descrive l'intersezione tra la geometria e la geometria specificata. Il confronto viene eseguito usando la tolleranza di Flat specificata.<br/> |



## <a name="remarks"></a>Commenti

Quando si interpreta il valore di *relazione* restituito, è importante ricordare che la relazione di [**geometria del membro d2d1 \_ \_ \_ è \_ contenuta**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) nel tipo di enumerazione della **\_ \_ relazione di geometria d2d1** significa che questa geometria è contenuta all'interno di *inputGeometry* e non che questa geometria contiene *inputGeometry*.

Per ulteriori informazioni su come interpretare altri possibili valori restituiti, vedere [**d2d1 \_ Geometry \_ Relation**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

