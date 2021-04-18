---
description: Tipo opaco e portabile per supportare l'utilizzo della sintassi dell'inizializzatore C/C++ per caricare valori a virgola mobile in un'istanza di tipo XMVECTOR.
ms.assetid: bafaa59f-fd1b-e252-cbbd-903df796fde0
title: Tipo di dati XMVECTORF32 (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e56e79ea678ede0afcac3523c09da725ede00d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329183"
---
# <a name="xmvectorf32-data-type"></a>Tipo di dati XMVECTORF32

Tipo opaco e portabile per supportare l'utilizzo della sintassi dell'inizializzatore C/C++ per caricare valori a virgola mobile in un'istanza di tipo [**XMVECTOR**](xmvector-data-type.md) .


```C++
typedef XMVECTORF32 vectorf32;
```



## <a name="remarks"></a>Commenti

Per un elenco di funzionalità aggiuntive, ad esempio costruttori e operatori, disponibili con `XMVECTORF32` durante la programmazione in C++, vedere [XMVECTORF32 Extensions](ovw-xmvectorf32-extensions.md).

Le strutture **XMVECTORF32**, [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md)e [**XMVECTORU8**](xmvectoru8-data-type.md) sono fornite come meccanismo per la creazione di [**XMVECTOR**](xmvector-data-type.md) da diversi tipi di dati costanti (a virgola mobile, Unsigned Integer, Integer e byte) tramite inizializzatori.

Questa operazione è necessaria per supportare [**XMVECTOR**](xmvector-data-type.md), in quanto non supporta gli inizializzatori, per motivi di portabilità e di ottimizzazione.

Ad esempio:


```
XMVECTOR data;
XMVECTORF32 floatingVector = { 0.f, 0.f, 0.1f, 1.f };
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

 

 




