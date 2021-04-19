---
description: Permuta i componenti di due vettori per creare un nuovo vettore.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorpermute(xmvector,xmvector)
title: Modello XMVectorPermute (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37271cbb165f1e9c1769ef3a55e47f1e07310a81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333231"
---
# <a name="xmvectorpermute-template"></a>Modello XMVectorPermute

Permuta i componenti di due vettori per creare un nuovo vettore.

## <a name="syntax"></a>Sintassi

``` syntax
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW> XMVECTOR XMVectorPermute(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="V1"></span><span id="v1"></span>*V1*
</dt> <dd>

\[nel \] primo vettore.

</dd> <dt>

<span id="V2"></span><span id="v2"></span>*V2*
</dt> <dd>

\[nel \] secondo vettore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il vettore permutati risultante dalla combinazione dei vettori di origine.

## <a name="remarks"></a>Commenti

Se tutti i 4 indici fanno riferimento solo a un singolo vettore (ovvero sono tutti compresi nell'intervallo 0-3 o tutti nell'intervallo 4-7), usare [**XMVectorSwizzle**](xmvectorswizzle-template.md) invece per ottenere prestazioni migliori.

Nota la libreria usa le specializzazioni dei modelli in alcune piattaforme per migliorare le prestazioni. Non ogni possibile mirror case è implementato per questi casi speciali, quindi preferisce permuta in cui l'elemento X del vettore risultante deriva dal parametro V1 anziché dal parametro V2. Si preferisce, ad esempio, usare `XMVectorPermute<0,1,4,5>(A,B);` a `XMVectorPermute(4,5,0,1)(B,A);` .

Questa funzione è una versione modello di [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) in cui gli argomenti di *permute \** sono valori di modello.

Le [costanti \_ permute \_ XM](ovw-xnamath-reference-constants.md) vengono fornite da usare come valori di input per *PermuteX*,*PermuteY*,*PermuteZ* e *PermuteW*.

> [!Note]  
> Il `XMVectorPermute` modello è una novità di DirectXMath e non è disponibile per XNAMath 2. x.

 

**Spazio dei nomi**: usare DirectX

### <a name="platform-requirements"></a>Requisiti della piattaforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con la Windows SDK per Windows 8. Supportato per le app desktop Win32, le app di Windows Store e le app Windows Phone 8.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DirectXMath. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni del modello di libreria DirectXMath](ovw-xnamath-templates.md)
</dt> <dt>

[**XMVectorSwizzle**](xmvectorswizzle-template.md)
</dt> </dl>

 

 
