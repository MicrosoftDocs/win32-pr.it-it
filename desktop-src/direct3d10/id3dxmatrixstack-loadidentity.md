---
description: "Metodo ID3DXMATRIXStack::LoadIdentity (D3DX10.h): carica l'identità nella matrice corrente."
ms.assetid: 324b49c2-3aca-4bbb-90f3-62f3ffb2fa45
title: Metodo ID3DXMATRIXStack::LoadIdentity (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadIdentity
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 26d52ca8bd8ebccf04a3f2e4f36e35a1ac4e5b2b74d8c0e0a79bd9b85568cfc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736060"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx10h"></a>Metodo ID3DXMATRIXStack::LoadIdentity (D3DX10.h)

Carica l'identità nella matrice corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

La matrice di identità è una matrice in cui tutti i coefficienti sono 0,0 ad eccezione dei \[ coefficienti 1,1 \] \[ 2,2 \] \[ 3,3 \] \[ 4,4, impostati su \] 1,0. La matrice di identità è speciale in quanto, quando viene applicata ai vertici, rimane invariata. La matrice di identità viene usata come punto iniziale per le matrici che modificheranno i valori dei vertici per creare rotazioni, traslazioni ed eventuali altre trasformazioni che possono essere rappresentate da una matrice 4x4.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




