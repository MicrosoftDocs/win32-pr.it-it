---
description: Swizzles un vettore.
ms.assetid: 75608e80-5911-45a8-beca-ceac1f4d2c1c
title: Modello XMVectorSwizzle (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8e872d76f3251eccc8616c143c645b388e2dca4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333228"
---
# <a name="xmvectorswizzle-template"></a>Modello XMVectorSwizzle

Swizzles un vettore.

## <a name="syntax"></a>Sintassi

``` syntax
template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW> XMVECTOR XMVectorSwizzle(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="V"></span><span id="v"></span>*V*
</dt> <dd>

\[\]da Vector a Swizzle.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il [**XMVECTOR**](xmvector-data-type.md)swizzled.

## <a name="remarks"></a>Commenti

Questa funzione è una versione modello di [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) in cui gli argomenti di *swizzle \** sono valori di modello.

`XM_SWIZZLE_X`, `XM_SWIZZLE_Y` , `XM_SWIZZLE_Z` e `XM_SWIZZLE_W` sono costanti che restituiscono rispettivamente 0, 1, 2 e 3 per l'uso con `XMVectorSwizzle` . Questo è identico a `XM_PERMUTE_0X` , `XM_PERMUTE_0Y` , `XM_PERMUTE_0Z` e `XM_PERMUTE_0W` .

> [!Note]  
> Il `XMVectorSwizzle` modello è una novità di DirectXMath e non è disponibile per XNAMath 2. x.

 

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

[**XMVectorPermute**](xmvectorpermute-template.md)
</dt> </dl>

 

 
