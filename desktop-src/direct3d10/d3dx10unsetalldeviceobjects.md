---
description: Rimuove tutte le risorse dal dispositivo impostando i relativi puntatori su NULL. Questa operazione deve essere chiamata durante l'arresto dell'applicazione. Consente di assicurarsi che, quando si rilasciano tutte le risorse, nessuna di esse sia associata al dispositivo.
ms.assetid: f41ce97e-5a81-43a4-a8c7-7411b43c0d61
title: Funzione D3DX10UnsetAllDeviceObjects (D3DX10Core.h)
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
ms.openlocfilehash: 079c5f1b437c2755bf7125dee6be10baed1a91b4a37276997e70543c72904036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128343"
---
# <a name="d3dx10unsetalldeviceobjects-function"></a>Funzione D3DX10UnsetAllDeviceObjects

Rimuove tutte le risorse dal dispositivo impostando i relativi puntatori su **NULL.** Questa operazione deve essere chiamata durante l'arresto dell'applicazione. Consente di assicurarsi che, quando si rilasciano tutte le risorse, nessuna di esse sia associata al dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10UnsetAllDeviceObjects(
  _In_ ID3D10Device *pDevice
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Puntatore al dispositivo. Vedere [**ID3D10 InterfaceDevice**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[per utilizzo generico funzioni](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




