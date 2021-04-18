---
description: Tipo portabile usato per rappresentare un vettore di componenti a virgola mobile o Integer a 4 32 bit, ognuno allineato in modo ottimale e mappato a un registro di vettori hardware.
ms.assetid: 1a044094-444d-e787-fa6a-76e88531aef1
title: Tipo di dati XMVECTOR (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c62cab01098cd95f904ac2e2ee33d420309e8e99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324359"
---
# <a name="xmvector-data-type"></a>Tipo di dati XMVECTOR

Tipo portabile usato per rappresentare un vettore di componenti a virgola mobile o Integer a 4 32 bit, ognuno allineato in modo ottimale e mappato a un registro di vettori hardware.

## <a name="remarks"></a>Commenti

Per un elenco di funzionalità aggiuntive, ad esempio costruttori e operatori, disponibili con `XMVECTOR` durante la programmazione in C++, vedere [XMVECTOR Extensions](ovw-xmvector-extensions.md).

Nella libreria DirectXMath, per supportare completamente la portabilità e l'ottimizzazione, `XMVECTOR` è, per progettazione, un tipo opaco. L'implementazione effettiva di `XMVECTOR` è dipendente dalla piattaforma.

In generale, il codice non deve basarsi sulle specifiche di una determinata implementazione specifica della piattaforma `XMVECTOR` . Le implementazioni specifiche della piattaforma hanno queste caratteristiche:

-   Non sono portabili.
-   Potrebbero variare tra le versioni.
-   L'uso incauto dei dettagli dell'implementazione potrebbe non essere ottimale.

Gli sviluppatori devono usare le funzioni di [accesso](ovw-xnamath-reference-functions-accessors.md), [caricamento](ovw-xnamath-reference-functions-load.md)e [archiviazione](ovw-xnamath-reference-functions-storage.md) della libreria DirectXMath per ottenere e impostare i vettori e le [funzioni di vettore 4D della libreria DirectXMath](ovw-xnamath-reference-functions-vector4.md) per modificarle.

Per i progetti che richiedono informazioni dettagliate su come implementare `XMVECTOR` su piattaforme diverse, vedere elementi [interni della libreria](pg-xnamath-internals.md).

### <a name="compiler-aliases"></a>Alias del compilatore

Il file di intestazione DirectXMath. h usa alias per l' `XMVECTOR` oggetto, in particolare **CXMVECTOR** e **FXMVECTOR**. L'intestazione utilizza questi alias per conformarsi alle convenzioni di chiamata inline ottimali di compilatori diversi. Per la maggior parte dei progetti che usano DirectXMath è sufficiente considerare questi tipi come un alias esatto a `XMVECTOR` .

Ad esempio:


```
[CDATA[
typedef const XMVECTOR FXMVECTOR;
typedef const XMVECTOR CXMVECTOR;
]]
```



Per i progetti che richiedono informazioni dettagliate su come diverse piattaforme gestiscono le convenzioni di chiamata, vedere elementi [interni della libreria](pg-xnamath-internals.md).

Per XNAMATH 2. x, il `XMVECTOR` tipo di dati include i membri dell'elemento. x,. y,. z,. e. w, che in genere provocano una riduzione delle prestazioni. L'uso del tipo XM \_ strict \_ VECTOR4 fornisce un consenso esplicito per la definizione DirectXMath di un tipo di dati opaco.

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

[**Tipo di dati XMVECTORU32**](xmvectoru32-data-type.md)
</dt> <dt>

[**Tipo di dati XMVECTORU8**](xmvectoru8-data-type.md)
</dt> <dt>

[**Tipo di dati XMVECTOR**](xmvector-data-type.md)
</dt> </dl>

 

 




