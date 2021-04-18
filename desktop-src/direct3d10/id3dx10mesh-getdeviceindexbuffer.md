---
description: "Accedere al buffer di indice della mesh dopo che è stato eseguito il commit nel dispositivo con ID3DX10Mesh:: CommitToDevice. Questa operazione è diversa da ID3DX10Mesh:: GetIndexBuffer, che restituisce il buffer dell'indice prima che sia stato eseguito il commit nel dispositivo."
ms.assetid: 94d21f50-91b5-4f8d-ac73-7a851bba8685
title: 'Metodo ID3DX10Mesh:: GetDeviceIndexBuffer (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3ec3e65cfc4acb5a903bcf18d2f707d39127e975
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323148"
---
# <a name="id3dx10meshgetdeviceindexbuffer-method"></a>Metodo ID3DX10Mesh:: GetDeviceIndexBuffer

Accedere al buffer di indice della mesh dopo che è stato eseguito il commit nel dispositivo con [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md). Questa operazione è diversa da [**ID3DX10Mesh:: GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), che restituisce il buffer dell'indice prima che sia stato eseguito il commit nel dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDeviceIndexBuffer(
  [out] ID3D10Buffer **ppIndexBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppIndexBuffer* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***

Buffer dell'indice dopo che è stato eseguito il commit nel dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Se non è ancora stato eseguito il commit del buffer di indice della mesh nel dispositivo, questa API eseguirà automaticamente il commit del buffer dell'indice prima di restituire un puntatore al buffer.

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

 

 




