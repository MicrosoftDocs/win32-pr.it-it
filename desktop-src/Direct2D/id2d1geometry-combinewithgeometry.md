---
title: Metodi ID2D1Geometry CombineWithGeometry
description: Combina questa geometria con la geometria specificata e archivia il risultato in id2D1SimplifiedGeometrySink.
ms.assetid: 5bb45c54-c551-4b54-ae91-41d2c57b9570
keywords:
- Metodi CombineWithGeometry Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 7bcd7cb18c9a2748e0c30264bc1b2593057dd9d8c1f891f854ea9afe71d0a312
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342891"
---
# <a name="id2d1geometrycombinewithgeometry-methods"></a>Metodi ID2D1Geometry::CombineWithGeometry

Combina questa geometria con la geometria specificata e archivia il risultato in [**id2D1SimplifiedGeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                                                                          | Descrizione                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CombineWithGeometry(ID2D1Geometry \* ,D2D1 \_ COMBINE \_ MODE,D2D1 \_ MATRIX \_ 3X2 \_ F&,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))              | Combina questa geometria con la geometria specificata e archivia il risultato in [**id2D1SimplifiedGeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)<br/>  |
| [**CombineWithGeometry(ID2D1Geometry \* ,D2D1 \_ COMBINE \_ MODE,D2D1 \_ MATRIX \_ 3X2 \_ \* F,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f_id2d1simplifiedgeometrysink))             | Combina questa geometria con la geometria specificata e archivia il risultato in [**id2D1SimplifiedGeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)<br/>  |
| [**CombineWithGeometry(ID2D1Geometry \* ,D2D1 \_ COMBINE \_ MODE,D2D1 \_ MATRIX \_ 3X2 \_ F&,FLOAT,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f__float_id2d1simplifiedgeometrysink))  | Combina questa geometria con la geometria specificata e archivia il risultato in [**id2D1SimplifiedGeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)<br/>  |
| [**CombineWithGeometry(ID2D1Geometry \* ,D2D1 \_ COMBINE \_ MODE,D2D1 \_ MATRIX \_ 3X2 \_ \* F,FLOAT,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink)) | Combina questa geometria con la geometria specificata e archivia il risultato in [**id2D1SimplifiedGeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) <br/> |



## <a name="examples"></a>Esempio

Il codice seguente usa ognuna delle diverse modalità di combinazione per combinare [**due oggetti ID2D1EllipseGeometry.**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)


```C++
HRESULT DemoApp::CreateGeometryResources()
{
    HRESULT hr = S_OK;
    ID2D1GeometrySink *pGeometrySink = NULL;

    // Create the first ellipse geometry to merge.
    const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
        D2D1::Point2F(75.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(
        circle1,
        &m_pCircleGeometry1
        );

    if (SUCCEEDED(hr))
    {
        // Create the second ellipse geometry to merge.
        const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
            D2D1::Point2F(125.0f, 75.0f),
            50.0f,
            50.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
    }


    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_UNION to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryUnion);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryUnion->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_UNION,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_INTERSECT to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryIntersect);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryIntersect->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_INTERSECT,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_XOR to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryXOR);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryXOR->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_XOR,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_EXCLUDE to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryExclude);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryExclude->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_EXCLUDE,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    return hr;
}
```



Questo codice produce l'output illustrato nella figura seguente.

![illustrazione di due ellissi combinate usando quattro modalità di combinazione di geometria (unione, intersezione, xor ed esclusione)](images/combine-modes.png)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

