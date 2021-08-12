---
description: Tipo opaco e portabile per supportare l'uso della sintassi dell'inizializzatore C/C++ per caricare i valori uint8 t in un'istanza del \_ tipo XMVECTOR.
ms.assetid: ab73ac2c-f178-1bb9-910d-9eef5fc6f5df
title: Tipo di dati XMVECTORU8 (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff3c335df3e74bc58776883b15d724c65d558bad30fc37e0e28547102260301a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118276197"
---
# <a name="xmvectoru8-data-type"></a>Tipo di dati XMVECTORU8

Tipo opaco e portabile per supportare l'uso della sintassi dell'inizializzatore C/C++ per caricare i valori uint8 t in un'istanza del \_ [**tipo XMVECTOR.**](xmvector-data-type.md)


```C++
typedef XMVECTORU8 vectoru8;
```



## <a name="remarks"></a>Commenti

Per un elenco di funzionalità aggiuntive, ad esempio costruttori e operatori, disponibili con XMVECTORU8 durante la programmazione in C++, vedere [Estensioni XMVECTORU8.](ovw-xmvectoru8-extensions.md)

Le strutture [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md)e **XMVECTORU8** vengono fornite come meccanismo per la creazione [**di XMVECTOR**](xmvector-data-type.md) da tipi di dati costanti diversi (virgola mobile, intero senza segno, integer e byte) usando inizializzatori.

Questa operazione è necessaria per supportare [**XMVECTOR,**](xmvector-data-type.md)perché non supporta inizializzatori, per motivi di portabilità e ottimizzazione.

Ad esempio:

``` syntax
XMVECTOR data;
XMVECTORU8  byteVector = { (uint8_t)  1,(uint8_t) 16,(uint8_t)101,(uint8_t) 62,
                           (uint8_t)  4,(uint8_t)  0,(uint8_t)  2,(uint8_t) 99,
                           (uint8_t)  9,(uint8_t) 18,(uint8_t)  0,(uint8_t)  0,
                           (uint8_t)100,(uint8_t) 51,(uint8_t) 23,(uint8_t)117};

data = floatingVector;
```

**Spazio dei** nomi: usare DirectX

### <a name="platform-requirements"></a>Requisiti della piattaforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con Windows SDK per Windows 8. Supportato per app desktop Win32, app Windows Store e app Windows Phone 8.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DirectXMath.h</dt> </dl> |



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

 

 




