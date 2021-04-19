---
description: Imposta un valore albedo per ogni vertice mesh, sovrascrivendo i valori albedo precedenti.
ms.assetid: 5220dfe3-8d41-480c-a850-b9aad3d2bb2f
title: 'Metodo ID3DXPRTEngine:: SetPerVertexAlbedo (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da7a33a79cc50963e87d0eff15baf22ee8d79ce3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322975"
---
# <a name="id3dxprtenginesetpervertexalbedo-method"></a>Metodo ID3DXPRTEngine:: SetPerVertexAlbedo

Imposta un valore albedo per ogni vertice mesh, sovrascrivendo i valori albedo precedenti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPerVertexAlbedo(
  [in] const VOID *pDataIn,
  [in]       UINT NumChannels,
  [in]       UINT Stride
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDataIn* \[ in\]
</dt> <dd>

Tipo: **const \* void**

Puntatore ai dati di albedo FLOAT del primo campione.

</dd> <dt>

*NumChannels* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di canali dei colori da impostare. Impostare su 1 per specificare i materiali grigi (R = G = B) o 3 per abilitare gli effetti di emorragia del colore.

</dd> <dt>

*Stride* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Stride in byte necessario per ottenere il valore albedo del campione successivo. Vedere [Width e pitch (Direct3D 9)](width-vs--pitch.md).

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
</dt> </dl>

 

 
