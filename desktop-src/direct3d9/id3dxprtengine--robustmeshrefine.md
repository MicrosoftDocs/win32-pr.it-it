---
description: Suddivide i visi su una mesh, consentendo il campionamento adattivo conservativo che non eliminerà le funzionalità sulla rete.
ms.assetid: 0d74a01a-de67-4607-99eb-ed98e239f199
title: 'Metodo ID3DXPRTEngine:: RobustMeshRefine (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.RobustMeshRefine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65d49fcec3072956365ce1ed8dc5d7a11ce6c826
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323437"
---
# <a name="id3dxprtenginerobustmeshrefine-method"></a>Metodo ID3DXPRTEngine:: RobustMeshRefine

Suddivide i visi su una mesh, consentendo il campionamento adattivo conservativo che non eliminerà le funzionalità sulla rete.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RobustMeshRefine(
  [in] FLOAT MinEdgeLength,
  [in] UINT  MaxSubdiv
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*MinEdgeLength* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Lunghezza minima del bordo della superficie che verrà generata nel campionamento adattivo. Se è zero, verrà sostituito un valore predefinito ragionevole.

</dd> <dt>

*MaxSubdiv* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Livello massimo di suddivisione di una faccia che verrà utilizzata nel campionamento adattivo. Se è zero, verrà sostituito un valore predefinito di 5.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeBounceAdaptive**](id3dxprtengine--computebounceadaptive.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md)
</dt> </dl>

 

 
