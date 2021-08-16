---
description: Creare un oggetto dispositivo.
ms.assetid: 5b9b00de-c744-43c7-b383-1d3358c80741
title: Metodo ID3DX10DataProcessor::CreateDeviceObject (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor.CreateDeviceObject
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ca20de85e867cc8c444f05ea187fb314a6b983ad8c72a5f8ae921c0747bd9ce8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540419"
---
# <a name="id3dx10dataprocessorcreatedeviceobject-method"></a>Metodo ID3DX10DataProcessor::CreateDeviceObject

Creare un oggetto dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateDeviceObject(
  [out] void **ppDataObject
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDataObject* \[ Cambio\]
</dt> <dd>

Tipo: **\* \* void**

Indirizzo di un puntatore all'oggetto dispositivo creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10DataProcessor](id3dx10dataprocessor.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




