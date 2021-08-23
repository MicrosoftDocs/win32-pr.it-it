---
title: Metodi SetColor id2D1SolidColorBrush
description: Specifica il colore di questo pennello a tinta unita.
ms.assetid: 2900bf72-9641-419c-b0d7-334f14f8a474
keywords:
- Metodi SetColor Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: eb281265a9567db5da6252944fa1da1a6beb1bd4a0fb2a6a4d80ef1177455fc8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873951"
---
# <a name="id2d1solidcolorbrushsetcolor-methods"></a>Metodi ID2D1SolidColorBrush::SetColor

Specifica il colore di questo pennello a tinta unita.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                          | Descrizione                                                |
|:--------------------------------------------------------------------------------|:-----------------------------------------------------------|
| [**SetColor(D2D1 \_ COLOR \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f_))  | Specifica il colore di questo pennello a tinta unita. <br/> |
| [**SetColor(D2D1 \_ COLOR \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f)) | Specifica il colore di questo pennello a tinta unita. <br/> |



## <a name="remarks"></a>Commenti

Per facilitare la creazione dei colori, Direct2D fornisce la [**classe ColorF.**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) Offre diversi metodi helper per la creazione di colori e fornisce un set o colori predefiniti.

## <a name="examples"></a>Esempio

Nel codice seguente viene illustrato come utilizzare questo metodo.


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
| Libreria<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)
</dt> </dl>

 

