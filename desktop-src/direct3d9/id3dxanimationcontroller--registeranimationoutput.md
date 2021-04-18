---
description: Aggiunge un output di animazione al controller di animazione e registra i puntatori per le trasformazioni di scala, rotazione e conversione (SRT).
ms.assetid: 8c3197bc-9d03-40ba-869b-151f9c8e96ba
title: 'Metodo ID3DXAnimationController:: RegisterAnimationOutput (D3dx9anim. h)'
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
ms.openlocfilehash: 7670f8b311532d096b9957ebbefcf1f6fb15d952
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323290"
---
# <a name="id3dxanimationcontrollerregisteranimationoutput-method"></a>Metodo ID3DXAnimationController:: RegisterAnimationOutput

Aggiunge un output di animazione al controller di animazione e registra i puntatori per le trasformazioni di scala, rotazione e conversione (SRT).

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

*Nome* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome dell'output dell'animazione.

</dd> <dt>

*pmatrix* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) contenente dati di trasformazione SRT. Può essere **null**.

</dd> <dt>

*pScale* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore a un vettore [**D3DXVECTOR3**](d3dxvector3.md) che descrive la scala del set di animazioni. Può essere **null**.

</dd> <dt>

*protazione* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntatore a un quaternione [**D3DXQUATERNION**](d3dxquaternion.md) che descrive la rotazione del set di animazioni. Può essere **null**.

</dd> <dt>

*pTranslation* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore a un vettore [**D3DXVECTOR3**](d3dxvector3.md) che descrive la traduzione del set di animazioni. Può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Se l'output di animazione è già registrato, pMatrix verrà riempito con i dati di trasformazione di input.

I set di animazioni creati con [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) registrano automaticamente tutti i set di animazioni caricati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
