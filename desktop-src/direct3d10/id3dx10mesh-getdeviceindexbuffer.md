---
description: Accedere alla rete index buffer dopo che è stato eseguito il commit nel dispositivo con ID3DX10Mesh::CommitToDevice. Questo è diverso da ID3DX10Mesh::GetIndexBuffer, che restituisce il index buffer prima che ne sia stato eseguito il commit nel dispositivo.
ms.assetid: 94d21f50-91b5-4f8d-ac73-7a851bba8685
title: Metodo ID3DX10Mesh::GetDeviceIndexBuffer (D3DX10.h)
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
ms.openlocfilehash: 869bd40b49801a1469ca08baa3a493cc23e6f6238624380411c8d91de829c79b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990371"
---
# <a name="id3dx10meshgetdeviceindexbuffer-method"></a>Metodo ID3DX10Mesh::GetDeviceIndexBuffer

Accedere alla rete index buffer dopo che è stato eseguito il commit nel dispositivo con [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md). Questo è diverso da [**ID3DX10Mesh::GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), che restituisce il index buffer prima che ne sia stato eseguito il commit nel dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDeviceIndexBuffer(
  [out] ID3D10Buffer **ppIndexBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppIndexBuffer* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***

Il index buffer dopo che è stato eseguito il commit nel dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Se non è già stato index buffer commit della rete nel dispositivo, questa API eseguirà automaticamente il commit del index buffer prima che restituisca un puntatore al buffer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




