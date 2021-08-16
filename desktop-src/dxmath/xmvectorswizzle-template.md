---
description: Scorre un vettore.
ms.assetid: 75608e80-5911-45a8-beca-ceac1f4d2c1c
title: Modello XMVectorSwizzle (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 800d976d63480f88defea7f1db07651563df44e8985ae5925810617b44302e87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984481"
---
# <a name="xmvectorswizzle-template"></a>Modello XMVectorSwizzle

Scorre un vettore.

## <a name="syntax"></a>Sintassi

``` syntax
template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW> XMVECTOR XMVectorSwizzle(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="V"></span><span id="v"></span>*Presso*
</dt> <dd>

\[in \] Vector to swizzle( Vettore da swizzle).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'oggetto [**XMVECTOR con**](xmvector-data-type.md)swizzle.

## <a name="remarks"></a>Commenti

Questa funzione è una versione modello di [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) in cui gli *argomenti di Swizzle \** sono valori di modello.

`XM_SWIZZLE_X`, `XM_SWIZZLE_Y` `XM_SWIZZLE_Z` , e sono costanti `XM_SWIZZLE_W` che restituiscono rispettivamente 0, 1, 2 e 3 per l'uso con `XMVectorSwizzle` . È identico a `XM_PERMUTE_0X` , `XM_PERMUTE_0Y` , e `XM_PERMUTE_0Z` `XM_PERMUTE_0W` .

> [!Note]  
> Il `XMVectorSwizzle` modello è una novità di DirectXMath e non è disponibile per XNAMath 2.x.

 

**Spazio dei** nomi: usare DirectX

### <a name="platform-requirements"></a>Requisiti della piattaforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con Windows SDK per Windows 8. Supportato per app desktop Win32, app Windows Store e app Windows Phone 8.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DirectXMath.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni del modello della libreria DirectXMath](ovw-xnamath-templates.md)
</dt> <dt>

[**XMVectorPermute**](xmvectorpermute-template.md)
</dt> </dl>

 

 
