---
description: Ruota il vettore a sinistra di un determinato numero di elementi a 32 bit.
ms.assetid: ba3698ed-212d-4ef0-846a-4099d0e1abec
title: Modello XMVectorRotateLeft (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb3d2a06f775e99b275d7333816307f494c5b2a4a7cc0183eaddc4ee4cd8950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118499404"
---
# <a name="xmvectorrotateleft-template"></a>Modello XMVectorRotateLeft

Ruota il vettore a sinistra di un determinato numero di elementi a 32 bit.

## <a name="syntax"></a>Sintassi

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateLeft(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="V"></span><span id="v"></span>*Presso*
</dt> <dd>

\[in \] Vector per ruotare a sinistra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'oggetto [**XMVECTOR ruotato.**](xmvector-data-type.md)

## <a name="remarks"></a>Commenti

Questa funzione è una versione modello di [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) in cui *l'argomento Elements* è un valore di modello.

> [!Note]  
> Il `XMVectorRotateLeft` modello è una novità di DirectXMath e non è disponibile per XNAMath 2.x.

 

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
</dt> <dt>

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> <dt>

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
