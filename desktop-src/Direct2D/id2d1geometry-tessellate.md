---
title: METODI TESSELLATI ID2D1Geometry
description: Crea un set di triangoli in senso orario che analizza la geometria dopo che è stata trasformata utilizzando la matrice specificata e resa bidimensionale utilizzando la tolleranza specificata.
ms.assetid: 4e0af188-d14b-43c0-be11-16577f054b90
keywords:
- Metodi a tessellate Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: b40602fb38ec2a0834ba202252114f7c0c34a4948e4473703ff4daf8bf2ee97a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917891"
---
# <a name="id2d1geometrytessellate-methods"></a>Metodi ID2D1Geometry::Tessellate

Crea un set di triangoli in senso orario che analizza la geometria dopo che è stata trasformata utilizzando la matrice specificata e resa bidimensionale utilizzando la tolleranza specificata.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                    | Descrizione                                                                                                                                                                          |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Tessellate(D2D1 \_ MATRIX \_ 3X2 \_ \* F,ID2D1TessellationSink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f__id2d1tessellationsink))             | Crea un set di triangoli a scorrimento in senso orario che coprono la geometria dopo che è stata trasformata usando la matrice specificata e appiattita usando la tolleranza predefinita. <br/>   |
| [**Tessellate(D2D1 \_ MATRIX \_ 3X2 \_ F&,ID2D1TessellationSink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f_id2d1tessellationsink))              | Crea un set di triangoli a scorrimento in senso orario che coprono la geometria dopo che è stata trasformata usando la matrice specificata e appiattita usando la tolleranza predefinita. <br/>   |
| [**Tessellate(D2D1 \_ MATRIX \_ 3X2 \_ \* F,FLOAT,ID2D1TessellationSink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f_float_id2d1tessellationsink)) | Crea un set di triangoli in senso orario che analizza la geometria dopo che è stata trasformata utilizzando la matrice specificata e resa bidimensionale utilizzando la tolleranza specificata. <br/> |
| [**Tessellate(D2D1 \_ MATRIX \_ 3X2 \_ F&,FLOAT,ID2D1TessellationSink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f__float_id2d1tessellationsink))  | Crea un set di triangoli in senso orario che analizza la geometria dopo che è stata trasformata utilizzando la matrice specificata e resa bidimensionale utilizzando la tolleranza specificata.<br/>  |



## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come usare Tessellate per creare un set di triangoli in senso orario che coprono la geometria.


```C++
 ID2D1GeometrySink *pGeometrySink = NULL;
 hr = pPathGeometry->Open(&pGeometrySink);
 if (SUCCEEDED(hr))
 {
     hr = pGeometry->Widen(
             strokeWidth,
             pIStrokeStyle,
             pWorldTransform,
             pGeometrySink
             );

     if (SUCCEEDED(hr))
     {
         hr = pGeometrySink->Close();
         if (SUCCEEDED(hr))
         {
             ID2D1Mesh *pMesh = NULL;
             hr = m_pRT->CreateMesh(&pMesh);
             if (SUCCEEDED(hr))
             {
                 ID2D1TessellationSink *pSink = NULL;
                 hr = pMesh->Open(&pSink);
                 if (SUCCEEDED(hr))
                 {
                     hr = pPathGeometry->Tessellate(
                             NULL, // world transform (already handled in Widen)
                             pSink
                             );
                     if (SUCCEEDED(hr))
                     {
                         hr = pSink->Close();
                         if (SUCCEEDED(hr))
                         {
                             SafeReplace(&m_pStrokeMesh, pMesh);
                         }
                     }
                     pSink->Release();
                 }
                 pMesh->Release();
             }
         }
     }
     pGeometrySink->Release();
 }
 pPathGeometry->Release();
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

 

