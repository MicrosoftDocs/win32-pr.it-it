---
title: Metodo IDWriteFactory2 GetSystemFontFallback
description: Crea un oggetto di fallback del tipo di carattere dall'elenco di fallback dei tipi di carattere di sistema.
ms.assetid: 7F2BDB39-2CB4-4DB7-BBBA-74B0C07E7420
keywords:
- Metodo GetSystemFontFallback Direct Write
- Metodo GetSystemFontFallback Direct Write, interfaccia IDWriteFactory2
- Interfaccia IDWriteFactory2 Direct Write, metodo GetSystemFontFallback
topic_type:
- apiref
api_name:
- IDWriteFactory2.GetSystemFontFallback
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4513c8ee7fb4e7a3796ec442d4d36bb663a0c8803bb6276a584edcfda306d588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329447"
---
# <a name="idwritefactory2getsystemfontfallback-method"></a>Metodo IDWriteFactory2::GetSystemFontFallback

Crea un oggetto di fallback del tipo di carattere dall'elenco di fallback dei tipi di carattere di sistema.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSystemFontFallback(
  [out] IDWriteFontFallback **fontFallback
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fontFallback* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***

Contiene un indirizzo di un puntatore all'oggetto di fallback del tipo di carattere appena creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

 