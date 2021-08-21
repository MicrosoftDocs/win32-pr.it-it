---
description: Sposta un vettore a sinistra di un determinato numero di elementi a 32 bit, riempiendo gli elementi liberati con elementi di un secondo vettore.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorshiftleft(xmvector,xmvector)
title: Modello XMVectorShiftLeft (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab92e2fb64a101251a7531ca1d96b8b06f3e9af6e2b7dabe7958673a61bd8c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118499280"
---
# <a name="xmvectorshiftleft-template"></a>Modello XMVectorShiftLeft

Sposta un vettore a sinistra di un determinato numero di elementi a 32 bit, riempiendo gli elementi liberati con elementi di un secondo vettore.

## <a name="syntax"></a>Sintassi

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorShiftLeft(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="V1"></span><span id="v1"></span>*V1*
</dt> <dd>

\[in \] Vector per spostare a sinistra.

</dd> <dt>

<span id="V2"></span><span id="v2"></span>*V2*
</dt> <dd>

\[in \] Vector usato per compilare i componenti liberati di V1 dopo che è stato spostato a sinistra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'oggetto spostato e compilato in [**XMVECTOR.**](xmvector-data-type.md)

## <a name="remarks"></a>Commenti

Questa funzione è una versione modello di [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) in cui *l'argomento Elements* è un valore di modello.

> [!Note]  
> Il `XMVectorShiftLeft` modello è una novità di DirectXMath e non è disponibile per XNAMath 2.x.

 

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

[**XMVectorRotateLeft**](xmvectorrotateleft-template.md)
</dt> <dt>

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> </dl>

 

 
