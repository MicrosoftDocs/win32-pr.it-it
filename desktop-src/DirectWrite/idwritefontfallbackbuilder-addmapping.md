---
title: Metodo IDWriteFontFallbackBuilder AddMapping
description: Accoda un singolo mapping all'elenco. Chiamare questa volta per ogni mapping aggiuntivo.
ms.assetid: FCA3CD9C-9FB3-49BD-B4D1-53AEAAAAEE8A
keywords:
- Scrittura diretta Metodo AddMapping
- Metodo AddMapping scrittura diretta, interfaccia IDWriteFontFallbackBuilder
- IDWriteFontFallbackBuilder Interface Direct Write, Metodo AddMapping
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder.AddMapping
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a084aa2a9df0e34741c8bf5f39ae00933d49cfe7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400755"
---
# <a name="idwritefontfallbackbuilderaddmapping-method"></a>Metodo IDWriteFontFallbackBuilder:: AddMapping

Accoda un singolo mapping all'elenco. Chiamare questa volta per ogni mapping aggiuntivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddMapping(
                       DWRITE_UNICODE_RANGE  *ranges,
                       UINT32                rangesCount,
  [in]           const WCHAR                 **targetFamilyNames,
                       UINT32                targetFamilyNamesCount,
  [in, optional]       IDWriteFontCollection fontCollection = nullptr,
  [in, optional] const WCHAR                 *localeName = nullptr,
  [in, optional] const WCHAR                 *baseFamilyName = nullptr,
                       FLOAT                 scale = 1
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*intervalli* 
</dt> <dd>

Tipo: **[**DWrite \_ Unicode \_ Range**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range) \** _

Intervalli Unicode applicabili a questo mapping.

</dd> <dt>

_rangesCount * 
</dt> <dd>

Tipo: **UInt32**

Numero di intervalli Unicode.

</dd> <dt>

*targetFamilyNames* \[ in\]
</dt> <dd>

Tipo: **const \* \* WCHAR**

Elenco delle stringhe del nome della famiglia di destinazione.

</dd> <dt>

*targetFamilyNamesCount* 
</dt> <dd>

Tipo: **UInt32**

Numero di nomi di famiglia di destinazione.

</dd> <dt>

*FontCollection* \[ in, facoltativo\]
</dt> <dd>

Tipo: **[ **IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**

Raccolta di tipi di carattere esplicita facoltativa per questo mapping.

</dd> <dt>

*localeName* \[ in, facoltativo\]
</dt> <dd>

Tipo: **const \* WCHAR* _

Impostazioni locali del contesto.

</dd> <dt>

_baseFamilyName * \[ in, facoltativo\]
</dt> <dd>

Tipo: **const \* WCHAR* _

Nome della famiglia di base in base al quale trovare la corrispondenza, se applicabile.

</dd> <dt>

_scale * 
</dt> <dd>

Tipo: **float**

Fattore di scala per moltiplicare il tipo di carattere di destinazione risultato per.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                     |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                          |
| Telefono minimo supportato<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md)
</dt> </dl>

 

