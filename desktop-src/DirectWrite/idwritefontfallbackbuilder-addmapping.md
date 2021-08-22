---
title: Metodo AddMapping di IDWriteFontFallbackBuilder
description: Aggiunge un singolo mapping all'elenco. Chiamare questa operazione una volta per ogni mapping aggiuntivo.
ms.assetid: FCA3CD9C-9FB3-49BD-B4D1-53AEAAAAEE8A
keywords:
- Metodo AddMapping Direct Write
- Metodo AddMapping Direct Write, interfaccia IDWriteFontFallbackBuilder
- Interfaccia IDWriteFontFallbackBuilder Direct Write , metodo AddMapping
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
ms.openlocfilehash: 0b6496ac9ef9bdfa574cc2c4710ed4620fd855dbf5eff2b22885b32bf343d141
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650441"
---
# <a name="idwritefontfallbackbuilderaddmapping-method"></a>Metodo IDWriteFontFallbackBuilder::AddMapping

Aggiunge un singolo mapping all'elenco. Chiamare questa operazione una volta per ogni mapping aggiuntivo.

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

*Gamme* 
</dt> <dd>

Tipo: **[ **DWRITE \_ UNICODE \_ RANGE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range)\***

Intervalli Unicode applicabili a questo mapping.

</dd> <dt>

*rangesCount* 
</dt> <dd>

Tipo: **UINT32**

Numero di intervalli Unicode.

</dd> <dt>

*targetFamilyNames* \[ Pollici\]
</dt> <dd>

Tipo: **const \* \* WCHAR**

Elenco di stringhe del nome della famiglia di destinazione.

</dd> <dt>

*targetFamilyNamesCount* 
</dt> <dd>

Tipo: **UINT32**

Numero di nomi di famiglie di destinazione.

</dd> <dt>

*fontCollection* \[ in, facoltativo\]
</dt> <dd>

Tipo: **[ **IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**

Raccolta di caratteri esplicita facoltativa per questo mapping.

</dd> <dt>

*localeName* \[ in, facoltativo\]
</dt> <dd>

Tipo: **const \* WCHAR**

Impostazioni locali del contesto.

</dd> <dt>

*baseFamilyName* \[ in, facoltativo\]
</dt> <dd>

Tipo: **const \* WCHAR**

Nome della famiglia di base con cui trovare la corrispondenza, se applicabile.

</dd> <dt>

*scale* 
</dt> <dd>

Tipo: **FLOAT**

Fattore di scala per moltiplicare il tipo di carattere di destinazione del risultato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                     |
| Server minimo supportato<br/> | Windows Server 2012 App \[ UWP per app desktop \| R2\]<br/>                          |
| Telefono minimo supportato<br/>  | Windows Phone 8.1 \[ Windows Phone silverlight 8.1 e Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md)
</dt> </dl>

 

