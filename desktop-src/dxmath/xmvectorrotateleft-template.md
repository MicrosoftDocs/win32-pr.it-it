---
description: Ruota il vettore lasciato da un determinato numero di elementi a 32 bit.
ms.assetid: ba3698ed-212d-4ef0-846a-4099d0e1abec
title: Modello XMVectorRotateLeft (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b52fccebeb93803fdc33346fa4ee5e873c1d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329180"
---
# <a name="xmvectorrotateleft-template"></a>Modello XMVectorRotateLeft

Ruota il vettore lasciato da un determinato numero di elementi a 32 bit.

## <a name="syntax"></a>Sintassi

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateLeft(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="V"></span><span id="v"></span>*V*
</dt> <dd>

\[in \] Vector per ruotare verso sinistra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il [**XMVECTOR**](xmvector-data-type.md)ruotato.

## <a name="remarks"></a>Commenti

Questa funzione è una versione modello di [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) in cui l'argomento *elements* è un valore di modello.

> [!Note]  
> Il `XMVectorRotateLeft` modello è una novità di DirectXMath e non è disponibile per XNAMath 2. x.

 

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

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> <dt>

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
