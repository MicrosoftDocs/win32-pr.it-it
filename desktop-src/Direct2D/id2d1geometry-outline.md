---
title: Metodi di struttura ID2D1Geometry
description: Calcola il contorno della geometria e scrive il risultato in un ID2D1SimplifiedGeometrySink.
ms.assetid: ec92db79-a1aa-4661-9e75-45a1763af370
keywords:
- Metodi di struttura Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 40d4ff1122d4a00e11ea35914f001b6dc9e06e4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330088"
---
# <a name="id2d1geometryoutline-methods"></a>Metodi ID2D1Geometry:: Outline

Calcola il contorno della geometria e scrive il risultato in un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                          | Descrizione                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Outline (D2D1 \_ Matrix \_ 3X2 \_ F&, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))              | Calcola il contorno della geometria e scrive il risultato in un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink). <br/> |
| [**Outline (D2D1 \_ Matrix \_ 3x2 \_ F \* , ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f_id2d1simplifiedgeometrysink))             | Calcola il contorno della geometria e scrive il risultato in un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).<br/>  |
| [**Outline (D2D1 \_ Matrix \_ 3X2 \_ F&, float, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__float_id2d1simplifiedgeometrysink))  | Calcola il contorno della geometria e scrive il risultato in un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).<br/>  |
| [**Outline (D2D1 \_ Matrix \_ 3x2 \_ F \* , float, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink)) | Calcola il contorno della geometria e scrive il risultato in un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).<br/>  |



## <a name="remarks"></a>Commenti

Il metodo [**Outline**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) consente al chiamante di produrre una geometria con un riempimento equivalente alla geometria di input, con le proprietà aggiuntive seguenti:

-   La geometria di output non contiene intersezioni trasversali; ovvero, i segmenti possono toccare, ma non si incrociano mai.
-   Le figure più esterne nella geometria di output sono tutte orientate in senso antiorario.
-   La geometria di output è invariante in modalità riempimento; ovvero, il riempimento della geometria non dipende dalla scelta della modalità di riempimento. Per ulteriori informazioni sulla modalità di riempimento, vedere [**\_ \_ modalità di riempimento d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode).

Inoltre, il metodo di [**struttura**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) può essere utile per rimuovere parti ridondanti di geometrie per semplificare le geometrie complesse. Può anche essere utile in combinazione con [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) per creare unioni tra più geometrie contemporaneamente.

## <a name="examples"></a>Esempio

Il codice seguente illustra come usare la **struttura** per costruire una geometria equivalente senza intersezioni autoreferenziali. Usa la tolleranza di Flat predefinita e pertanto non deve essere usata con geometrie molto piccole.


```C++
HRESULT D2DOutline(
    ID2D1Geometry *pGeometry,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Outline(NULL, pSink);

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
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

 

