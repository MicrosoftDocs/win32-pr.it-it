---
description: Tipo portabile usato per rappresentare un vettore di quattro componenti integer o a virgola mobile a 32 bit, ognuno allineato in modo ottimale e mappato a un registro vettoriale hardware.
ms.assetid: 1a044094-444d-e787-fa6a-76e88531aef1
title: Tipo di dati XMVECTOR (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0a65c7da346163c3cbfaab7c68982f56eb6c424b7f74a3ec01c754eb4104a5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094481"
---
# <a name="xmvector-data-type"></a>Tipo di dati XMVECTOR

Tipo portabile usato per rappresentare un vettore di quattro componenti integer o a virgola mobile a 32 bit, ognuno allineato in modo ottimale e mappato a un registro vettoriale hardware.

## <a name="remarks"></a>Commenti

Per un elenco di funzionalità aggiuntive, ad esempio costruttori e operatori, disponibili tramite durante la programmazione `XMVECTOR` in C++, vedere [Estensioni XMVECTOR.](ovw-xmvector-extensions.md)

Nella libreria DirectXMath, per supportare completamente la portabilità e l'ottimizzazione, `XMVECTOR` è, per impostazione predefinita, un tipo opaco. L'implementazione effettiva di `XMVECTOR` dipende dalla piattaforma.

In generale, il codice non deve basarsi sulle specifiche di una determinata implementazione specifica della piattaforma di `XMVECTOR` . Le implementazioni specifiche della piattaforma hanno queste caratteristiche:

-   Non sono portabili.
-   Possono cambiare tra le versioni.
-   L'uso ingiudito dei dettagli di implementazione può non essere efficace.

Gli sviluppatori devono usare la funzione di [](ovw-xnamath-reference-functions-load.md)accesso [](ovw-xnamath-reference-functions-storage.md) [,](ovw-xnamath-reference-functions-accessors.md)il caricamento e l'archiviazione della libreria DirectXMath per ottenere e impostare i vettori e le funzioni vettoriali 4D della libreria [DirectXMath](ovw-xnamath-reference-functions-vector4.md) per modificarli.

Per i progetti che necessitano di informazioni dettagliate su come implementare `XMVECTOR` in piattaforme diverse, vedere [Elementi interni della libreria.](pg-xnamath-internals.md)

### <a name="compiler-aliases"></a>Alias del compilatore

Il file di intestazione DirectXMath.h usa alias per l'oggetto , in `XMVECTOR` **particolare CXMVECTOR** **e FXMVECTOR**. L'intestazione usa questi alias per rispettare le convenzioni di chiamata inline ottimali di compilatori diversi. Per la maggior parte dei progetti che usano DirectXMath è sufficiente considerare questi tipi come alias esatto di `XMVECTOR` .

Esempio:


```
[CDATA[
typedef const XMVECTOR FXMVECTOR;
typedef const XMVECTOR CXMVECTOR;
]]
```



Per i progetti che necessitano di informazioni dettagliate sul modo in cui le diverse piattaforme gestiscono le convenzioni di chiamata, vedere [Elementi interni della libreria.](pg-xnamath-internals.md)

Per XNAMATH 2.x, il tipo di dati ha membri elemento `XMVECTOR` .x, .y, .z, .e .w, che in genere causano prestazioni scarse. L'uso del tipo XM STRICT VECTOR4 fornisce il consenso esplicito della \_ \_ definizione DirectXMath di un tipo di dati opaco.

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

[**Tipo di dati XMVECTORI32**](xmvectori32-data-type.md)
</dt> <dt>

[**Tipo di dati XMVECTORF32**](xmvectorf32-data-type.md)
</dt> <dt>

[**Tipo di dati XMVECTORU32**](xmvectoru32-data-type.md)
</dt> <dt>

[**Tipo di dati XMVECTORU8**](xmvectoru8-data-type.md)
</dt> <dt>

[**Tipo di dati XMVECTOR**](xmvector-data-type.md)
</dt> </dl>

 

 




