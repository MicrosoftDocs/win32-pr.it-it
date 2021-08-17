---
description: Ottiene un elenco di profili DXVA (DirectX Video Acceleration) supportati dal driver video.
ms.assetid: 4adbbac2-a25d-4e17-b62e-a02a67dcdbed
title: Metodo IDirect3DVideoDevice9::GetDXVAGuids (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAGuids
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 6a355c27177a546a2e91e769f72d9f4b9e216b005f711d42b5b7af39b4b78361
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119269241"
---
# <a name="idirect3dvideodevice9getdxvaguids-method"></a>Metodo IDirect3DVideoDevice9::GetDXVAGuids

Ottiene un elenco di profili DXVA (DirectX Video Acceleration) supportati dal driver video.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDXVAGuids(
   DWORD *pNumGuids,
   GUID  *pGuids
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNumGuids* 
</dt> <dd>

Nell'input specifica il numero di elementi nella *matrice pGuids.* Se *pGuids* è **NULL,** il valore di `*pNumGuids` deve essere zero.

Nell'output, se *pGuids* è **NULL,** *pNumGuids* riceve il numero di profili DXVA in modalità limitata. In caso *contrario, pNumGuids* riceve il numero effettivo di GUID copiati nella *matrice pGuids.*

</dd> <dt>

*pGuid* 
</dt> <dd>

Indirizzo di una matrice di GUID o **NULL.** Se il valore è diverso da **NULL,** la matrice riceve un elenco di GUID che specificano profili DXVA in modalità limitata. Questi GUID sono definiti in dxva.h e sono documentati nella specifica [DXVA 1.0.](/windows-hardware/drivers/display/directx-video-acceleration)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Chiamare questo metodo due volte. Alla prima chiamata impostare *pGuids* su **NULL.** Il *parametro pNumGuids* riceve il numero di GUID del profilo DXVA. Allocare una matrice di GUID con le dimensioni richieste e chiamare nuovamente il metodo . Questa volta, impostare *pGuids* sull'indirizzo della matrice. Il metodo riempie la matrice con l'elenco di GUID del profilo DXVA.

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

 

 
