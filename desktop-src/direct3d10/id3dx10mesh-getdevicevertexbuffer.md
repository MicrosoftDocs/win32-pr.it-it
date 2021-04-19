---
description: 'Accedere al buffer dei vertici della mesh dopo che è stato eseguito il commit nel dispositivo con ID3DX10Mesh:: CommitToDevice. Questa operazione è diversa da ID3DX10Mesh:: GetVertexBuffer, che restituisce il buffer dei vertici prima che sia stato eseguito il commit nel dispositivo.'
ms.assetid: 621d9105-e55d-47b8-8557-8adb7db19d66
title: 'Metodo ID3DX10Mesh:: GetDeviceVertexBuffer (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9943050d174acb4e8f8e676f56a95cfdcde88f5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323147"
---
# <a name="id3dx10meshgetdevicevertexbuffer-method"></a>Metodo ID3DX10Mesh:: GetDeviceVertexBuffer

Accedere al buffer dei vertici della mesh dopo che è stato eseguito il commit nel dispositivo con [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md). Questa operazione è diversa da [**ID3DX10Mesh:: GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), che restituisce il buffer dei vertici prima che sia stato eseguito il commit nel dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDeviceVertexBuffer(
  [in]  UINT         iBuffer,
  [out] ID3D10Buffer **ppVertexBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IBuffer* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice che identifica il buffer dei vertici a cui accedere.

</dd> <dt>

*ppVertexBuffer* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***

Buffer dei vertici dopo che è stato eseguito il commit nel dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
