---
title: Metodo IDWriteFontFace GetGdiCompatibleMetrics
description: Ottiene le unità di progettazione e le metriche comuni per il tipo di carattere. Queste metriche sono applicabili a tutti i glifi all'interno di una fontFace e vengono usate dalle applicazioni per i calcoli di layout.
ms.assetid: 9e132ec0-64cb-4681-b079-02a0047badd5
keywords:
- Scrittura diretta metodo GetGdiCompatibleMetrics
- Metodo GetGdiCompatibleMetrics scrittura diretta, interfaccia IDWriteFontFace
- IDWriteFontFace interface Direct Write, metodo GetGdiCompatibleMetrics
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81b1c00c872352c984c87ee84f7eaed5baffafd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325904"
---
# <a name="idwritefontfacegetgdicompatiblemetrics-method"></a>Metodo IDWriteFontFace:: GetGdiCompatibleMetrics

Ottiene le unità di progettazione e le metriche comuni per il tipo di carattere. Queste metriche sono applicabili a tutti i glifi all'interno di una fontFace e vengono usate dalle applicazioni per i calcoli di layout.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetGdiCompatibleMetrics(
                       FLOAT               emSize,
                       FLOAT               pixelsPerDip,
  [in, optional] const DWRITE_MATRIX       *transform,
  [out]                DWRITE_FONT_METRICS *fontFaceMetrics
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*emSize* 
</dt> <dd>

Tipo: **float**

Dimensioni logiche del tipo di carattere in unità DIP.

</dd> <dt>

*pixelsPerDip* 
</dt> <dd>

Tipo: **float**

Il numero di pixel fisici per DIP.

</dd> <dt>

*trasformazione* \[ in, facoltativo\]
</dt> <dd>

Tipo: **const [**DWrite \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

Trasformazione facoltativa applicata ai glifi e alle rispettive posizioni. Questa trasformazione viene applicata dopo il ridimensionamento specificato dalle dimensioni del carattere e da *pixelsPerDip*.

</dd> <dt>

*fontFaceMetrics* \[ out\]
</dt> <dd>

Tipo: metrica del tipo di **[ **\_ carattere \_ DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***

Puntatore a una struttura [**della \_ \_ metrica del tipo di carattere DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)da compilare. Le metriche restituite da questa funzione sono in unità di progettazione dei tipi di carattere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Codice di errore HRESULT standard.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>DWrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

