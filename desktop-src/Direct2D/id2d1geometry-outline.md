---
title: Metodi id2D1Geometry Outline
description: Calcola la struttura della geometria e scrive il risultato in id2D1SimplifiedGeometrySink.
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
ms.openlocfilehash: 3c10a777d33e0a8c9a9fa033ca2615ce2d45b2badd292757e90f88074e131549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917911"
---
# <a name="id2d1geometryoutline-methods"></a>Metodi ID2D1Geometry::Outline

Calcola la struttura della geometria e scrive il risultato in [**id2D1SimplifiedGeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                          | Descrizione                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Outline(D2D1 \_ MATRIX \_ 3X2 \_ F&,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))              | Calcola la struttura della geometria e scrive il risultato in [**id2D1SimplifiedGeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) <br/> |
| [**Outline(D2D1 \_ MATRIX \_ 3X2 \_ \* F,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f_id2d1simplifiedgeometrysink))             | Calcola la struttura della geometria e scrive il risultato in [**id2D1SimplifiedGeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)<br/>  |
| [**Outline(D2D1 \_ MATRIX \_ 3X2 \_ F&,FLOAT,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__float_id2d1simplifiedgeometrysink))  | Calcola la struttura della geometria e scrive il risultato in [**id2D1SimplifiedGeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)<br/>  |
| [**Outline(D2D1 \_ MATRIX \_ 3X2 \_ \* F, FLOAT,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink)) | Calcola la struttura della geometria e scrive il risultato in [**id2D1SimplifiedGeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)<br/>  |



## <a name="remarks"></a>Commenti

Il [**metodo Outline**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) consente al chiamante di produrre una geometria con un riempimento equivalente alla geometria di input, con le proprietà aggiuntive seguenti:

-   La geometria di output non contiene intersezioni trasversali. in altri, i segmenti possono toccare, ma non si incrociano mai.
-   Le figure più esterne nella geometria di output sono tutte orientate in senso antiorario.
-   La geometria di output è invariante in modalità di riempimento. ciò significa che il riempimento della geometria non dipende dalla scelta della modalità di riempimento. Per altre informazioni sulla modalità di riempimento, vedere [**D2D1 \_ FILL \_ MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode).

Inoltre, il [**metodo Outline**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) può essere utile per rimuovere parti ridondanti delle geometrie per semplificare geometrie complesse. Può anche essere utile in combinazione con [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) per creare unioni tra diverse geometrie contemporaneamente.

## <a name="examples"></a>Esempio

Il codice seguente illustra come usare **Outline per** costruire una geometria equivalente senza auto-intersezioni. Usa la tolleranza di appiattimento predefinita e pertanto non deve essere usata con geometrie molto piccole.


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
| Libreria<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

