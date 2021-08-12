---
description: Imposta le proprietà di campionamento usate dal simulatore PRT (Precomputed Radiance Transfer).
ms.assetid: a33963a7-fbcb-4e1c-a4f3-fb20a99fcf9f
title: Metodo ID3DXPRTEngine::SetSamplingInfo (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetSamplingInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: db15bc2120f90cf52aa4f3c41eccecc7d308cc8392ae368cd4423a90f218f6ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293365"
---
# <a name="id3dxprtenginesetsamplinginfo-method"></a>Metodo ID3DXPRTEngine::SetSamplingInfo

Imposta le proprietà di campionamento usate dal simulatore PRT (Precomputed Radiance Transfer).

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSamplingInfo(
  [in] UINT  NumRays,
  [in] BOOL  UseSphere,
  [in] BOOL  UseCosine,
  [in] BOOL  Adaptive,
  [in] FLOAT AdaptiveThresh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NumRays* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di raggi di luce da indirizzare a ogni campione. Deve essere maggiore di zero.

</dd> <dt>

*UseSphere* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Se **TRUE,** gli esempi verranno calcolati su una sfera completa. Se **FALSE,** gli esempi verranno calcolati su un emisfero.

</dd> <dt>

*UseCosine* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Se **TRUE,** usare un peso coseno dei campioni. Se useCosine e UseSphere sono **entrambi TRUE,** il metodo avrà esito negativo e verrà restituito un errore.

</dd> <dt>

*Adattiva* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Deve essere **FALSE.** Il campionamento adattivo non è attualmente implementato.

</dd> <dt>

*AdaptiveThresh* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ NOTIMPL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
