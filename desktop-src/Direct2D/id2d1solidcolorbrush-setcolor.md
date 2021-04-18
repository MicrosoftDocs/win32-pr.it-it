---
title: Metodi Secolor ID2D1SolidColorBrush
description: Specifica il colore di questo pennello a tinta unita.
ms.assetid: 2900bf72-9641-419c-b0d7-334f14f8a474
keywords:
- Metodo Secolor Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 580778135e840a69342ff34ffd8e415883317517
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331189"
---
# <a name="id2d1solidcolorbrushsetcolor-methods"></a>Metodi ID2D1SolidColorBrush:: Secolor

Specifica il colore di questo pennello a tinta unita.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                          | Descrizione                                                |
|:--------------------------------------------------------------------------------|:-----------------------------------------------------------|
| [**Secolor (D2D1 \_ Color \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f_))  | Specifica il colore di questo pennello a tinta unita. <br/> |
| [**Secolor (D2D1 \_ Color \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f)) | Specifica il colore di questo pennello a tinta unita. <br/> |



## <a name="remarks"></a>Commenti

Per semplificare la creazione dei colori, Direct2D fornisce la classe [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) . Offre diversi metodi helper per la creazione di colori e fornisce un set o colori predefiniti.

## <a name="examples"></a>Esempio

Il codice seguente illustra come usare questo metodo.


```C++
        m_pSolidColorBrush->SetColor(
            D2D1::ColorF(
                0.0f,
                intensity,
                1.0f - intensity
                ));

        hr = m_pRealization->Fill(
                m_pRT,
                m_pSolidColorBrush,
                m_useRealizations ?
                    REALIZATION_RENDER_MODE_DEFAULT :
                    REALIZATION_RENDER_MODE_FORCE_UNREALIZED
                );
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)
</dt> </dl>

 

