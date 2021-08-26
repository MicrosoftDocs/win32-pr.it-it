---
description: Abilita o disabilita una traccia nel controller di animazione.
ms.assetid: 8d06287b-e076-4553-962c-5c423e355101
title: Metodo ID3DXAnimationController::SetTrackEnable (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 61078a40e13ee1422c29de091e1758444e2bafa1586bb443e763e50d57457ad5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026581"
---
# <a name="id3dxanimationcontrollersettrackenable-method"></a>Metodo ID3DXAnimationController::SetTrackEnable

Abilita o disabilita una traccia nel controller di animazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetTrackEnable(
  [in] UINT Track,
  [in] BOOL Enable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Traccia* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificatore della traccia da misto.

</dd> <dt>

*Abilita* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Abilita valore. Impostare su **TRUE** per abilitare questa traccia nel controller o su **FALSE** per impedire che venga mista.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Per combinare una traccia con altre tracce, il flag Enable deve essere impostato su **TRUE.** Al contrario, l'impostazione del flag **su FALSE** impedisce che la traccia venga mista ad altre tracce.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
