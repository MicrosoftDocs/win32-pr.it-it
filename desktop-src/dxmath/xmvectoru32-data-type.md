---
description: Tipo portabile opaco per supportare l'uso della sintassi dell'inizializzatore C/C++ per caricare i valori uint32 t in un'istanza del \_ tipo XMVECTOR.
ms.assetid: 1ac1f48a-cd7f-7741-933f-c341fc42a21c
title: Tipo di dati XMVECTORU32 (Directxmath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13d37a5630df37021637bed978943a48a665db16301f2067c82f050a8231bbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891681"
---
# <a name="xmvectoru32-data-type"></a>Tipo di dati XMVECTORU32

Tipo portabile opaco per supportare l'uso della sintassi dell'inizializzatore C/C++ per caricare i valori uint32 t in un'istanza del \_ [**tipo XMVECTOR.**](xmvector-data-type.md)


```C++
typedef XMVECTOR32 vectoru32;
```



## <a name="remarks"></a>Commenti

Per un elenco di funzionalità aggiuntive, ad esempio costruttori e operatori, disponibili con XMVECTORU32 durante la programmazione in C++, vedere [Estensioni XMVECTORU32](ovw-xmvectoru32-extensions.md).

Le strutture [**XMVECTORF32**](xmvectorf32-data-type.md), **XMVECTORU32**, [**XMVECTORI32**](xmvectori32-data-type.md)e [**XMVECTORU8**](xmvectoru8-data-type.md) vengono fornite come meccanismo per la creazione [**di XMVECTOR**](xmvector-data-type.md) da tipi di dati costanti diversi (virgola mobile, intero senza segno, integer e byte) tramite inizializzatori.

Questa operazione è necessaria per supportare [**XMVECTOR,**](xmvector-data-type.md)perché non supporta gli inizializzatori, per motivi di portabilità e ottimizzazione.

Esempio:

``` syntax
XMVECTOR data;
XMVECTORU32 uintVector = { 0xf7000000, 0x8310000, 0x1000000, 0 };
data = uintVector;
```

**Spazio dei** nomi: usare DirectX

### <a name="platform-requirements"></a>Requisiti della piattaforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con Windows SDK per Windows 8. Supportato per app desktop Win32, app Windows Store e Windows Phone 8 app.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Directxmath.h</dt> </dl> |



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

 

 




