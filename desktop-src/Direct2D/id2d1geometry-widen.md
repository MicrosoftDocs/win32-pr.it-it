---
title: Metodi Widen ID2D1Geometry
description: Amplia la geometria in base al tratto specificato e scrive il risultato in id2D1SimplifiedGeometrySink.
ms.assetid: c951ab85-7980-41e3-95c4-291d2fb046c8
keywords:
- Metodi widen Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: ebdae7ba4fd9eca96e422ae62274b4b9934040d4c4249bc9e1c78b81b62589dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342811"
---
# <a name="id2d1geometrywiden-methods"></a>Metodi ID2D1Geometry::Widen

Amplia la geometria in base al tratto specificato e scrive il risultato in un [**id2D1SimplifiedGeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                          | Descrizione                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Widen(FLOAT,ID2D1StrokeStyle \* ,D2D1 \_ MATRIX \_ 3X2 \_ \* F,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))             | Amplia la geometria in base al tratto specificato e scrive il risultato in [**id2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) dopo essere stato trasformato dalla matrice specificata e appiattito usando la tolleranza predefinita.<br/>   |
| [**Widen(FLOAT,ID2D1StrokeStyle \* ,D2D1 \_ MATRIX \_ 3X2 \_ F&,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f_id2d1simplifiedgeometrysink))              | Amplia la geometria in base al tratto specificato e scrive il risultato in [**id2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) dopo essere stato trasformato dalla matrice specificata e appiattito usando la tolleranza predefinita.<br/>   |
| [**Widen(FLOAT,ID2D1StrokeStyle \* ,D2D1 \_ MATRIX \_ 3X2 \_ \* F,FLOAT,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink)) | Amplia la geometria in base al tratto specificato e scrive il risultato in [**id2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) dopo essere stato trasformato dalla matrice specificata e appiattito usando la tolleranza specificata.<br/> |
| [**Widen(FLOAT,ID2D1StrokeStyle \* ,D2D1 \_ MATRIX \_ 3X2 \_ F&,FLOAT,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))  | Amplia la geometria in base al tratto specificato e scrive il risultato in [**id2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) dopo essere stato trasformato dalla matrice specificata e appiattito usando la tolleranza specificata.<br/> |



## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come usare **Widen** per ampliare la geometria in base al tratto specificato e quindi scrivere il risultato in un oggetto [**ID2D1SimplifiedGeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)


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

 

