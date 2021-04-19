---
description: Ruota il vettore a destra di un numero specificato di elementi a 32 bit.
ms.assetid: 7493c1fe-2c3d-4eb6-bec1-02c066a70b9f
title: Modello XMVectorRotateRight (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2c4e623a75015e8051a5a9ccf32f4715016b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333229"
---
# <a name="xmvectorrotateright-template"></a>Modello XMVectorRotateRight

Ruota il vettore a destra di un numero specificato di elementi a 32 bit.

## <a name="syntax"></a>Sintassi

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateRight(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="V"></span><span id="v"></span>*V*
</dt> <dd>

\[in \] Vector per ruotare a destra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il [**XMVECTOR**](xmvector-data-type.md)ruotato.

## <a name="remarks"></a>Commenti

Questa funzione è una versione modello di [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) in cui l'argomento *elements* è un valore di modello.

> [!Note]  
> Il `XMVectorRotateRight` modello è una novità di DirectXMath e non è disponibile per XNAMath 2. x.

 

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
</dt> <dt>

[**XMVectorRotateLeft**](xmvectorrotateleft-template.md)
</dt> <dt>

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
