---
description: Tipo opaco e portabile per supportare l'utilizzo della sintassi dell'inizializzatore C/C++ per caricare \_ i valori UInt32 t in un'istanza di tipo XMVECTOR.
ms.assetid: 1ac1f48a-cd7f-7741-933f-c341fc42a21c
title: Tipo di dati XMVECTORU32 (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90c7a64d42bc4638573b987642c0cd77c37cc12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329170"
---
# <a name="xmvectoru32-data-type"></a>Tipo di dati XMVECTORU32

Tipo opaco e portabile per supportare l'utilizzo della sintassi dell'inizializzatore C/C++ per caricare \_ i valori UInt32 t in un'istanza di tipo [**XMVECTOR**](xmvector-data-type.md) .


```C++
typedef XMVECTOR32 vectoru32;
```



## <a name="remarks"></a>Commenti

Per un elenco di funzionalità aggiuntive, ad esempio costruttori e operatori, disponibili con XMVECTORU32 durante la programmazione in C++, vedere [estensioni di XMVECTORU32](ovw-xmvectoru32-extensions.md).

Le strutture [**XMVECTORF32**](xmvectorf32-data-type.md), **XMVECTORU32**, [**XMVECTORI32**](xmvectori32-data-type.md)e [**XMVECTORU8**](xmvectoru8-data-type.md) sono fornite come meccanismo per la creazione di [**XMVECTOR**](xmvector-data-type.md) da diversi tipi di dati costanti (a virgola mobile, Unsigned Integer, Integer e byte) tramite inizializzatori.

Questa operazione è necessaria per supportare [**XMVECTOR**](xmvector-data-type.md), in quanto non supporta gli inizializzatori, per motivi di portabilità e di ottimizzazione.

Ad esempio:

``` syntax
XMVECTOR data;
XMVECTORU32 uintVector = { 0xf7000000, 0x8310000, 0x1000000, 0 };
data = uintVector;
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

[**Tipo di dati XMVECTORI32**](xmvectori32-data-type.md)
</dt> <dt>

[**Tipo di dati XMVECTORF32**](xmvectorf32-data-type.md)
</dt> <dt>

[**Tipo di dati XMVECTOR**](xmvector-data-type.md)
</dt> <dt>

[**Tipo di dati XMVECTORU8**](xmvectoru8-data-type.md)
</dt> <dt>

[Estensioni XMVECTORU32](ovw-xmvectoru32-extensions.md)
</dt> </dl>

 

 




