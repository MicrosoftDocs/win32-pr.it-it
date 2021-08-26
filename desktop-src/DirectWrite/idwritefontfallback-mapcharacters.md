---
title: Metodo IDWriteFontFallback MapCharacters
description: Determina un tipo di carattere appropriato da usare per eseguire il rendering dell'intervallo di testo iniziale.
ms.assetid: 9D3DBBF7-72D4-473D-A321-E64BC94493D5
keywords:
- Metodo MapCharacters Direct Write
- Metodo MapCharacters Direct Write, interfaccia IDWriteFontFallback
- Interfaccia IDWriteFontFallback Direct Write, metodo MapCharacters
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
ms.openlocfilehash: 99f18932121d44f61d67c8124faa2d26638035bdcff473ad26c4222ceea9a85b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048791"
---
# <a name="idwritefontfallbackmapcharacters-method"></a>Metodo IDWriteFontFallback::MapCharacters

Determina un tipo di carattere appropriato da usare per eseguire il rendering dell'intervallo di testo iniziale.

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

Tipo: **[ **IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource)\***

L'implementazione dell'origine testo contiene il testo e le impostazioni locali.

</dd> <dt>

*textPosition* 
</dt> <dd>

Tipo: **UINT32**

Posizione iniziale da analizzare.

</dd> <dt>

*textLength* 
</dt> <dd>

Tipo: **UINT32**

Lunghezza del testo da analizzare.

</dd> <dt>

*baseFontCollection* \[ in, facoltativo\]
</dt> <dd>

Tipo: **[ **IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)\***

Raccolta di caratteri predefinita da usare.

</dd> <dt>

*baseFamilyName* \[ in, facoltativo\]
</dt> <dd>

Tipo: **const wchar \_ t \***

Nome della famiglia del tipo di carattere di base. Se si passa null, non verrà eseguita alcuna corrispondenza per la famiglia.

</dd> <dt>

*baseWeight* 
</dt> <dd>

Tipo: **[ **SPESSORE DEL \_ CARATTERE \_ DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**

Peso desiderato.

</dd> <dt>

*baseStyle* 
</dt> <dd>

Tipo: **[ **STILE \_ \_ CARATTERE DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**

Stile desiderato.

</dd> <dt>

*baseStretch* 
</dt> <dd>

Tipo: **[ **DWRITE \_ FONT \_ STRETCH**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**

Estensione desiderata.

</dd> <dt>

*mappedLength* \[ Cambio\]
</dt> <dd>

Tipo: **UINT32 \***

Lunghezza del testo mappato al tipo di carattere mappato. Sarà sempre minore o uguale alla lunghezza del testo e maggiore di zero (se la lunghezza del testo è diversa da zero), quindi il chiamante avanza almeno un carattere.

</dd> <dt>

*mappedFont* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***

Tipo di carattere che deve essere usato per eseguire il rendering dei primi *caratteri mappedLength* del testo. Se restituisce NULL, significa che nessun tipo di carattere può eseguire il rendering del testo e *mappedLength* è il numero di caratteri da ignorare (di cui viene eseguito il rendering con un glifo mancante).

</dd> <dt>

*scalabilità* \[ Cambio\]
</dt> <dd>

Tipo: **\* FLOAT**

Fattore di scala per moltiplicare le dimensioni em del tipo di carattere restituito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                 |
| Telefono minimo supportato<br/>  | Windows Phone 8.1 \[ Windows Phone silverlight 8.1 e Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)
</dt> </dl>

 

