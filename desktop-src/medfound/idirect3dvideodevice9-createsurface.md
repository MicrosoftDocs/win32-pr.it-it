---
description: Crea una superficie compressa per la decodifica DXVA (DirectX Video Acceleration).
ms.assetid: 2bb8c99d-1151-4f6d-869f-2c1a592e76af
title: Metodo IDirect3DVideoDevice9::CreateSurface (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateSurface
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: b5bc624527c7ef3ea2a8bb9c878f1d97e865a54341ae5902449fb8a015374f3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887871"
---
# <a name="idirect3dvideodevice9createsurface-method"></a>Metodo IDirect3DVideoDevice9::CreateSurface

Crea una superficie compressa per la decodifica DXVA (DirectX Video Acceleration).

Per ottenere i requisiti di superficie, chiamare [**IDirect3DVideoDevice9::GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) ed esaminare le strutture [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) restituite.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateSurface(
   UINT              Width,
   UINT              Height,
   UINT              BackBuffers,
   D3DFORMAT         Format,
   D3DPOOL           Pool,
   DWORD             Usage,
   IDirect3DSurface9 **ppSurface,
   HANDLE            *pSharedHandle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Larghezza* 
</dt> <dd>

Larghezza della superficie, in pixel. Impostare questo parametro su **DXVACompBufferInfo.WidthToCreate**.

</dd> <dt>

*Altezza* 
</dt> <dd>

Altezza della superficie, in pixel. Impostare questo parametro su **DXVACompBufferInfo.HeightToCreate**.

</dd> <dt>

*BackBuffers* 
</dt> <dd>

Numero di buffer nascosto. Questo parametro può essere zero.

</dd> <dt>

*Formato* 
</dt> <dd>

Formato pixel, specificato come **valore D3DFORMAT.** Impostare questo parametro su **DXVACompBufferInfo.Format**.

</dd> <dt>

*Pool* 
</dt> <dd>

Pool di memoria in cui creare la superficie, specificato come **valore D3DPOOL.** Impostare questo parametro su **DXVACompBufferInfo.Pool**.

</dd> <dt>

*Utilizzo* 
</dt> <dd>

OR bit per **bit** di una o **più costanti D3DUSAGE.** Impostare questo parametro su **DXVACompBufferInfo.Usage**.

</dd> <dt>

*ppSurface* 
</dt> <dd>

Riceve un puntatore **all'interfaccia IDirect3DSurface9.** Il chiamante deve rilasciare l'interfaccia .

</dd> <dt>

*pSharedHandle* 
</dt> <dd>

Riservato. Impostare su **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                    |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




