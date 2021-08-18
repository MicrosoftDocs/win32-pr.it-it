---
description: Tipo opaco e portabile per supportare l'uso della sintassi dell'inizializzatore C/C++ per caricare valori Integer in un'istanza del tipo XMVECTOR.
ms.assetid: 6564030e-b6e9-0c4f-4e2a-4132e4264c94
title: Tipo di dati XMVECTORI32 (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b4bb03dffb4c77575aab8c2a2680ecd821fea627f49325c6748ede607ef81f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739760"
---
# <a name="xmvectori32-data-type"></a>Tipo di dati XMVECTORI32

Tipo opaco e portabile per supportare l'uso della sintassi dell'inizializzatore C/C++ per caricare valori Integer in un'istanza del [**tipo XMVECTOR.**](xmvector-data-type.md)


```C++
typedef XMVECTORI32 vectori32;
```



## <a name="remarks"></a>Commenti

Per un elenco di funzionalità aggiuntive, ad esempio costruttori e operatori, disponibili tramite durante la programmazione `XMVECTORI32` in C++, vedere [Estensioni XMVECTORI32.](ovw-xmvectori32-extensions.md)

Le strutture [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), **XMVECTORI32** e [**XMVECTORU8**](xmvectoru8-data-type.md) vengono fornite come meccanismo per la creazione [**di XMVECTOR**](xmvector-data-type.md) da tipi di dati costanti diversi (virgola mobile, intero senza segno, integer e byte) usando inizializzatori.

Questa operazione è necessaria per supportare [**XMVECTOR,**](xmvector-data-type.md)perché non supporta inizializzatori, per motivi di portabilità e ottimizzazione.

Esempio:


```
XMVECTOR data;
XMVECTORI32 intVector = { -1, 5, 33, 0 };
data = intVector;
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

[**Tipo di dati XMVECTORU32**](xmvectoru32-data-type.md)
</dt> <dt>

[**Tipo di dati XMVECTORU8**](xmvectoru8-data-type.md)
</dt> <dt>

[**Tipo di dati XMVECTORI32**](xmvectori32-data-type.md)
</dt> </dl>

 

 




