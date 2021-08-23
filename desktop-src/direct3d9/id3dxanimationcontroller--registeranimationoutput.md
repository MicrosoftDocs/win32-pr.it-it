---
description: Aggiunge un output dell'animazione al controller di animazione e registra i puntatori per le trasformazioni di ridimensionamento, rotazione e traslazione (SRT).
ms.assetid: 8c3197bc-9d03-40ba-869b-151f9c8e96ba
title: Metodo ID3DXAnimationController::RegisterAnimationOutput (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationOutput
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc48eb9f2fd6ee5fee6c04936801997145a5ea21542b9b5ff8ec6d257eee80e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987821"
---
# <a name="id3dxanimationcontrollerregisteranimationoutput-method"></a>Metodo ID3DXAnimationController::RegisterAnimationOutput

Aggiunge un output dell'animazione al controller di animazione e registra i puntatori per le trasformazioni di ridimensionamento, rotazione e traslazione (SRT).

## <a name="syntax"></a>Sintassi


```C++
HRESULT RegisterAnimationOutput(
  [in] LPCSTR         Name,
  [in] D3DXMATRIX     *pMatrix,
  [in] D3DXVECTOR3    *pScale,
  [in] D3DXQUATERNION *pRotation,
  [in] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome dell'output dell'animazione.

</dd> <dt>

*pMatrix* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore a una [**struttura D3DXMATRIX**](d3dxmatrix.md) contenente i dati di trasformazione SRT. Può essere **NULL.**

</dd> <dt>

*pScale* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore a un [**vettore D3DXVECTOR3**](d3dxvector3.md) che descrive la scala del set di animazioni. Può essere **NULL.**

</dd> <dt>

*pRotation* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntatore a [**un quaternione D3DXQUATERNION**](d3dxquaternion.md) che descrive la rotazione del set di animazioni. Può essere **NULL.**

</dd> <dt>

*pTranslation* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore a un [**vettore D3DXVECTOR3**](d3dxvector3.md) che descrive la traslazione del set di animazioni. Può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Se l'output dell'animazione è già registrato, pMatrix verrà riempito con i dati di trasformazione di input.

I set di animazioni creati [**con D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) registrano automaticamente tutti i set di animazioni caricati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
