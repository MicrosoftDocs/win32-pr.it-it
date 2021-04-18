---
title: Metodo IDWriteFontFallback MapCharacters
description: Determina un tipo di carattere appropriato da utilizzare per eseguire il rendering dell'intervallo iniziale del testo.
ms.assetid: 9D3DBBF7-72D4-473D-A321-E64BC94493D5
keywords:
- Scrittura diretta metodo MapCharacters
- Metodo MapCharacters scrittura diretta, interfaccia IDWriteFontFallback
- IDWriteFontFallback Interface Direct Write, metodo MapCharacters
topic_type:
- apiref
api_name:
- IDWriteFontFallback.MapCharacters
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 428778afc12c668d284dffb5a8a6f734c03f0705
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340833"
---
# <a name="idwritefontfallbackmapcharacters-method"></a>Metodo IDWriteFontFallback:: MapCharacters

Determina un tipo di carattere appropriato da utilizzare per eseguire il rendering dell'intervallo iniziale del testo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT MapCharacters(
                       IDWriteTextAnalysisSource *source,
                       UINT32                    textPosition,
                       UINT32                    textLength,
  [in, optional]       IDWriteFontCollection     *baseFontCollection,
  [in, optional] const wchar_t                   *baseFamilyName,
                       DWRITE_FONT_WEIGHT        baseWeight,
                       DWRITE_FONT_STYLE         baseStyle,
                       DWRITE_FONT_STRETCH       baseStretch,
  [out]                UINT32                    *mappedLength,
  [out]                IDWriteFont               **mappedFont,
  [out]                FLOAT                     *scale
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*source* 
</dt> <dd>

Tipo: **[**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) \** _

L'implementazione di origine del testo include il testo e le impostazioni locali.

</dd> <dt>

_textPosition * 
</dt> <dd>

Tipo: **UInt32**

Posizione iniziale da analizzare.

</dd> <dt>

*textLength* 
</dt> <dd>

Tipo: **UInt32**

Lunghezza del testo da analizzare.

</dd> <dt>

*baseFontCollection* \[ in, facoltativo\]
</dt> <dd>

Tipo: **[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) \** _

Raccolta dei tipi di carattere predefinita da utilizzare.

</dd> <dt>

_baseFamilyName * \[ in, facoltativo\]
</dt> <dd>

Tipo: **const \_ WCHAR \* t* _

Nome della famiglia del tipo di carattere di base. Se si passa null, non verrà eseguita alcuna corrispondenza per la famiglia.

</dd> <dt>

_baseWeight * 
</dt> <dd>

Tipo: **[ **\_ \_ Spessore carattere DWrite**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**

Spessore desiderato.

</dd> <dt>

*baseStyle* 
</dt> <dd>

Tipo: stile del tipo di **[ **\_ carattere \_ DWrite**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**

Stile desiderato.

</dd> <dt>

*baseStretch* 
</dt> <dd>

Tipo: estensione del tipo di **[ **\_ carattere \_ DWrite**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**

Estensione desiderata.

</dd> <dt>

*mappedLength* \[ out\]
</dt> <dd>

Tipo: **UInt32 \** _

Lunghezza del testo mappato al tipo di carattere mappato. Sarà sempre minore o uguale alla lunghezza del testo e maggiore di zero (se la lunghezza del testo è diversa da zero), in modo che il chiamante anticipi almeno un carattere.

</dd> <dt>

_mappedFont * \[ out\]
</dt> <dd>

Tipo: **[ **IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***

Il tipo di carattere da utilizzare per eseguire il rendering dei primi caratteri *mappedLength* del testo. Se restituisce NULL, significa che nessun carattere può eseguire il rendering del testo e *mappedLength* è il numero di caratteri da ignorare (sottoposto a rendering con un glifo mancante).

</dd> <dt>

*Ridimensiona* \[ out\]
</dt> <dd>

Tipo: **float \** _

Fattore di scala per moltiplicare le dimensioni em del tipo di carattere restituito da.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                 |
| Telefono minimo supportato<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)
</dt> </dl>

 

