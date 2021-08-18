---
description: Tipo portabile opaco per supportare l'uso della sintassi dell'inizializzatore C/C++ per caricare valori a virgola mobile in un'istanza del tipo XMVECTOR.
ms.assetid: bafaa59f-fd1b-e252-cbbd-903df796fde0
title: Tipo di dati XMVECTORF32 (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1a39de246e3e0e4ab9a96197dbe4a286cb6ecabe327d60e5c506795af79dd11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739781"
---
# <a name="xmvectorf32-data-type"></a>Tipo di dati XMVECTORF32

Tipo portabile opaco per supportare l'uso della sintassi dell'inizializzatore C/C++ per caricare valori a virgola mobile in un'istanza del [**tipo XMVECTOR.**](xmvector-data-type.md)


```C++
typedef XMVECTORF32 vectorf32;
```



## <a name="remarks"></a>Commenti

Per un elenco di funzionalità aggiuntive, ad esempio costruttori e operatori, disponibili tramite durante la programmazione `XMVECTORF32` in C++, vedere [Estensioni XMVECTORF32](ovw-xmvectorf32-extensions.md).

Le strutture **XMVECTORF32**, [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md)e [**XMVECTORU8**](xmvectoru8-data-type.md) vengono fornite come meccanismo per la creazione [**di XMVECTOR**](xmvector-data-type.md) da tipi di dati costanti diversi (virgola mobile, intero senza segno, integer e byte) tramite inizializzatori.

Questa operazione è necessaria per supportare [**XMVECTOR,**](xmvector-data-type.md)perché non supporta gli inizializzatori, per motivi di portabilità e ottimizzazione.

Esempio:


```
XMVECTOR data;
XMVECTORF32 floatingVector = { 0.f, 0.f, 0.1f, 1.f };
data = floatingVector;
```



**Spazio dei** nomi: usare DirectX

### <a name="platform-requirements"></a>Requisiti della piattaforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con Windows SDK per Windows 8. Supportato per app desktop Win32, app Windows Store e Windows Phone 8 app.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DirectXMath.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di libreria DirectXMath](ovw-xnamath-reference-types.md)
</dt> <dt>

[**Tipo di dati XMVECTORI32**](xmvectori32-data-type.md)
</dt> <dt>

[**Tipo di dati XMVECTOR**](xmvector-data-type.md)
</dt> <dt>

[**Tipo di dati XMVECTORU32**](xmvectoru32-data-type.md)
</dt> <dt>

[**Tipo di dati XMVECTORU8**](xmvectoru8-data-type.md)
</dt> <dt>

[**Tipo di dati XMVECTORF32**](xmvectorf32-data-type.md)
</dt> </dl>

 

 




