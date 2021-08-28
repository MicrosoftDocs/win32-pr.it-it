---
description: Permuta i componenti di due vettori per creare un nuovo vettore.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorpermute(xmvector,xmvector)
title: Modello XMVectorPermute (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd3f7071edaf659991c1294d29a154d3a319d5faee982537025e107cf9621f55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978671"
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

\[in \] Primo vettore.

</dd> <dt>

<span id="V2"></span><span id="v2"></span>*V2*
</dt> <dd>

\[in \] Secondo vettore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il vettore permutato risultante dalla combinazione dei vettori di origine.

## <a name="remarks"></a>Commenti

Se tutti e 4 gli indici fanno riferimento a un solo vettore, ovvero sono tutti nell'intervallo 0-3 o tutti nell'intervallo 4-7, usare [**XMVectorSwizzle**](xmvectorswizzle-template.md) per ottenere prestazioni migliori.

Si noti che la libreria usa le specializzazioni dei modelli in alcune piattaforme per migliorare le prestazioni. Non tutti i possibili casi mirror vengono implementati per questi casi speciali, pertanto preferire le permute in cui l'elemento X del vettore risultante proviene dal parametro V1 anziché dal parametro V2. Ad esempio, preferire l'uso `XMVectorPermute<0,1,4,5>(A,B);` di a `XMVectorPermute(4,5,0,1)(B,A);` .

Questa funzione è una versione modello di [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) in cui gli *argomenti Permute \** sono valori di modello.

Vengono [fornite le costanti \_ XM \_ PERMUTE](ovw-xnamath-reference-constants.md) da usare come valori di input per *PermuteX,**PermuteY,**PermuteZ* e *PermuteW.*

> [!Note]  
> Il `XMVectorPermute` modello è nuovo per DirectXMath e non è disponibile per XNAMath 2.x.

 

**Spazio dei** nomi: usare DirectX

### <a name="platform-requirements"></a>Requisiti della piattaforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con Windows SDK per Windows 8. Supportato per app desktop Win32, app Windows Store e Windows Phone 8 app.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DirectXMath.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni del modello della libreria DirectXMath](ovw-xnamath-templates.md)
</dt> <dt>

[**XMVectorSwizzle**](xmvectorswizzle-template.md)
</dt> </dl>

 

 
