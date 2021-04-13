---
title: Metodo IDWriteFactory2 GetSystemFontFallback
description: Crea un oggetto fallback del tipo di carattere dall'elenco di fallback dei tipi di carattere di sistema.
ms.assetid: 7F2BDB39-2CB4-4DB7-BBBA-74B0C07E7420
keywords:
- Scrittura diretta metodo GetSystemFontFallback
- Metodo GetSystemFontFallback scrittura diretta, interfaccia IDWriteFactory2
- IDWriteFactory2 Interface Direct Write, metodo GetSystemFontFallback
topic_type:
- apiref
api_name:
- IDWriteFactory2.GetSystemFontFallback
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3f0eb73ee80dc3e6195267d25f6043225b8613ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399472"
---
# <a name="idwritefactory2getsystemfontfallback-method"></a>Metodo IDWriteFactory2:: GetSystemFontFallback

Crea un oggetto fallback del tipo di carattere dall'elenco di fallback dei tipi di carattere di sistema.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSystemFontFallback(
  [out] IDWriteFontFallback **fontFallback
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fontFallback* \[ out\]
</dt> <dd>

Tipo: **[ **IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***

Contiene un indirizzo di un puntatore all'oggetto fallback del tipo di carattere appena creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

 