---
description: "Metodo ID3DXMATRIXStack::LoadIdentity (D3dx9math.h): carica l'identità nella matrice corrente."
ms.assetid: e314a51f-4016-4819-a95d-d91864a54b2e
title: Metodo ID3DXMATRIXStack::LoadIdentity (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 046267b11f1a2aa977eda7f5fe461e5c44a2cf59e1f50ae291cf714f063088c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847741"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx9mathh"></a>Metodo ID3DXMATRIXStack::LoadIdentity (D3dx9math.h)

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
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::LoadMatrix**](id3dxmatrixstack--loadmatrix.md)
</dt> </dl>

 

 




