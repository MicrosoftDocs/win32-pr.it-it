---
title: Metodo IDWriteFontFace GetGdiCompatibleMetrics
description: Ottiene le unità di progettazione e le metriche comuni per il viso del tipo di carattere. Queste metriche sono applicabili a tutti i glifi all'interno di un carattere tipo di carattere e vengono usate dalle applicazioni per i calcoli del layout.
ms.assetid: 9e132ec0-64cb-4681-b079-02a0047badd5
keywords:
- Metodo GetGdiCompatibleMetrics Direct Write
- Metodo GetGdiCompatibleMetrics Direct Write, interfaccia IDWriteFontFace
- Interfaccia IDWriteFontFace Direct Write, metodo GetGdiCompatibleMetrics
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
ms.openlocfilehash: fce5080edc44501290672bf0db0ebac69ef4856ec0b7163821cf60ac63d384ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290711"
---
# <a name="idwritefontfacegetgdicompatiblemetrics-method"></a>Metodo IDWriteFontFace::GetGdiCompatibleMetrics

Ottiene le unità di progettazione e le metriche comuni per il viso del tipo di carattere. Queste metriche sono applicabili a tutti i glifi all'interno di un carattere tipo di carattere e vengono usate dalle applicazioni per i calcoli del layout.

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

Tipo: **FLOAT**

Dimensione logica del tipo di carattere in unità DIP.

</dd> <dt>

*pixelsPerDip* 
</dt> <dd>

Tipo: **FLOAT**

Numero di pixel fisici per DIP.

</dd> <dt>

*trasformazione* \[ in, facoltativo\]
</dt> <dd>

Tipo: **const [**DWRITE \_ MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

Trasformazione facoltativa applicata ai glifi e alle relative posizioni. Questa trasformazione viene applicata dopo il ridimensionamento specificato dalle dimensioni del carattere e *pixelPerDip*.

</dd> <dt>

*fontFaceMetrics* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWRITE \_ FONT \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***

Puntatore a una [**struttura DWRITE \_ FONT \_ METRIC**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)S da compilare. Le metriche restituite da questa funzione sono in unità di progettazione dei tipi di carattere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Codice di errore HRESULT standard.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

