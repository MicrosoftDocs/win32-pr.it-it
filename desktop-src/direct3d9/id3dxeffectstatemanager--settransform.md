---
description: Funzione di callback che deve essere implementata da un utente per impostare una trasformazione.
ms.assetid: 5d886554-ddb6-4b8a-a7fd-453e94b9516f
title: 'Metodo ID3DXEffectStateManager:: setransform (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTransform
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b19a060cfeb09d5d1a92e5e7a1a1f25b58e64f4d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969416"
---
# <a name="id3dxeffectstatemanagersettransform-method"></a>Metodo ID3DXEffectStateManager:: setransform

Funzione di callback che deve essere implementata da un utente per impostare una trasformazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetTransform(
  [in]       D3DTRANSFORMSTATETYPE State,
  [in] const D3DMATRIX             *pMatrix
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Stato* \[ di in\]
</dt> <dd>

Tipo: **[ **D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md)**

Tipo di trasformazione a cui applicare la matrice. Vedere [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md).

</dd> <dt>

*pmatrix* \[ in\]
</dt> <dd>

Tipo: **const [**D3DMATRIX**](d3dmatrix.md) \***

Matrice di trasformazione. Vedere [**D3DMATRIX**](d3dmatrix.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il metodo implementato dall'utente deve restituire S \_ OK. Se il callback ha esito negativo quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:

-   L'effetto avrà esito negativo durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).
-   La chiamata allo stato dell'effetto dinamico, ad esempio [**IDirect3DDevice9:: setransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform), avrà esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
