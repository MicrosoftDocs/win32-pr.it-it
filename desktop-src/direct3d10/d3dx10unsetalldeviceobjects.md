---
description: Rimuove tutte le risorse dal dispositivo impostando i relativi puntatori su NULL. Questa operazione deve essere chiamata durante l'arresto dell'applicazione. Consente di assicurare che, quando si rilasciano tutte le relative risorse, nessuna delle quali è associata al dispositivo.
ms.assetid: f41ce97e-5a81-43a4-a8c7-7411b43c0d61
title: Funzione D3DX10UnsetAllDeviceObjects (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10UnsetAllDeviceObjects
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4d3a113be935f77dbd62b2f3fac4c16c7cac9881
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322764"
---
# <a name="d3dx10unsetalldeviceobjects-function"></a>D3DX10UnsetAllDeviceObjects (funzione)

Rimuove tutte le risorse dal dispositivo impostando i relativi puntatori su **null**. Questa operazione deve essere chiamata durante l'arresto dell'applicazione. Consente di assicurare che, quando si rilasciano tutte le relative risorse, nessuna delle quali è associata al dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10UnsetAllDeviceObjects(
  _In_ ID3D10Device *pDevice
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Puntatore al dispositivo. Vedere [**interfaccia ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per utilizzo generico](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




