---
description: Tipo opaco e portabile per supportare l'uso della sintassi dell'inizializzatore C/C++ per caricare \_ i valori Uint8 in un'istanza di tipo XMVECTOR.
ms.assetid: ab73ac2c-f178-1bb9-910d-9eef5fc6f5df
title: Tipo di dati XMVECTORU8 (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4428cdd78206bfa17c295a9578653bb0a66f0c6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324358"
---
# <a name="xmvectoru8-data-type"></a>Tipo di dati XMVECTORU8

Tipo opaco e portabile per supportare l'uso della sintassi dell'inizializzatore C/C++ per caricare \_ i valori Uint8 in un'istanza di tipo [**XMVECTOR**](xmvector-data-type.md) .


```C++
typedef XMVECTORU8 vectoru8;
```



## <a name="remarks"></a>Commenti

Per un elenco di funzionalità aggiuntive, ad esempio costruttori e operatori, disponibili con XMVECTORU8 durante la programmazione in C++, vedere [estensioni di XMVECTORU8](ovw-xmvectoru8-extensions.md).

Le strutture [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md)e **XMVECTORU8** sono fornite come meccanismo per la creazione di [**XMVECTOR**](xmvector-data-type.md) da diversi tipi di dati costanti (a virgola mobile, Unsigned Integer, Integer e byte) tramite inizializzatori.

Questa operazione è necessaria per supportare [**XMVECTOR**](xmvector-data-type.md), in quanto non supporta gli inizializzatori, per motivi di portabilità e di ottimizzazione.

Ad esempio:

``` syntax
XMVECTOR data;
XMVECTORU8  byteVector = { (uint8_t)  1,(uint8_t) 16,(uint8_t)101,(uint8_t) 62,
                           (uint8_t)  4,(uint8_t)  0,(uint8_t)  2,(uint8_t) 99,
                           (uint8_t)  9,(uint8_t) 18,(uint8_t)  0,(uint8_t)  0,
                           (uint8_t)100,(uint8_t) 51,(uint8_t) 23,(uint8_t)117};

data = floatingVector;
```

**Spazio dei nomi**: usare DirectX

### <a name="platform-requirements"></a>Requisiti della piattaforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con la Windows SDK per Windows 8. Supportato per le app desktop Win32, le app di Windows Store e le app Windows Phone 8.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DirectXMath. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di libreria DirectXMath](ovw-xnamath-reference-types.md)
</dt> <dt>

[**Tipo di dati XMVECTOR**](xmvector-data-type.md)
</dt> <dt>

[**Tipo di dati XMVECTORF32**](xmvectorf32-data-type.md)
</dt> <dt>

[**Tipo di dati XMVECTORI32**](xmvectori32-data-type.md)
</dt> <dt>

[**Tipo di dati XMVECTORU32**](xmvectoru32-data-type.md)
</dt> <dt>

[Estensioni XMVECTORU8](ovw-xmvectoru8-extensions.md)
</dt> </dl>

 

 




