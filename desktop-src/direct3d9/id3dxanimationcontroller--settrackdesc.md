---
description: Imposta la descrizione della traccia.
ms.assetid: bc3324b3-ca23-4035-958d-9763a70071f2
title: Metodo ID3DXAnimationController::SetTrackDesc (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e25536f3e36e07a7145623efb6a6515f3f77c11177204f5213539c69f454b705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122082"
---
# <a name="id3dxanimationcontrollersettrackdesc-method"></a>Metodo ID3DXAnimationController::SetTrackDesc

Imposta la descrizione della traccia.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetTrackDesc(
  [in] UINT             Track,
  [in] LPD3DXTRACK_DESC pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tenere traccia* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificatore della traccia da modificare.

</dd> <dt>

*pDesc* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXTRACK \_ DESC**](d3dxtrack-desc.md)**

Descrizione della traccia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
