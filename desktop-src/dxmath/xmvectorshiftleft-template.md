---
description: Sposta un vettore lasciato da un numero specificato di elementi a 32 bit, riempiendo gli elementi sgomberati con elementi da un secondo vettore.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorshiftleft(xmvector,xmvector)
title: Modello XMVectorShiftLeft (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115604871d9e8402157a82bf3c420e5762b3a424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329172"
---
# <a name="xmvectorshiftleft-template"></a>Modello XMVectorShiftLeft

Sposta un vettore lasciato da un numero specificato di elementi a 32 bit, riempiendo gli elementi sgomberati con elementi da un secondo vettore.

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

\[in \] Vector per spostare verso sinistra.

</dd> <dt>

<span id="V2"></span><span id="v2"></span>*V2*
</dt> <dd>

\[in \] vector usato per compilare i componenti sgomberati di V1 dopo che è stato spostato verso sinistra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'oggetto spostato e compilato in [**XMVECTOR**](xmvector-data-type.md).

## <a name="remarks"></a>Commenti

Questa funzione è una versione modello di [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) in cui l'argomento *elements* è un valore di modello.

> [!Note]  
> Il `XMVectorShiftLeft` modello è una novità di DirectXMath e non è disponibile per XNAMath 2. x.

 

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

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> </dl>

 

 
