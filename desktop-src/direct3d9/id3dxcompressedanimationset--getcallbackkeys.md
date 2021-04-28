---
description: "Metodo ID3DXCompressedAnimationSet::GetCallbackKeys: riempie una matrice con i dati della chiave di callback usati per l'animazione con fotogrammi chiave."
ms.assetid: 0dc30c1f-9ffb-42ec-8074-84293f16c344
title: Metodo ID3DXCompressedAnimationSet::GetCallbackKeys (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d7c430358b5ba7f66c5a79b08ae01925141e659f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115329"
---
# <a name="id3dxcompressedanimationsetgetcallbackkeys-method"></a>Metodo ID3DXCompressedAnimationSet::GetCallbackKeys

Riempie una matrice con i dati della chiave di callback usati per l'animazione con fotogrammi chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCallbackKeys* \[ Cambio\]
</dt> <dd>

Tipo: **[ **CALLBACK LPD3DXKEY \_**](d3dxkey-callback.md)**

Puntatore a una matrice allocata dall'utente [**di strutture \_ CALLBACK D3DXKEY**](d3dxkey-callback.md) che il metodo deve riempire con i dati di callback.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXCompressedAnimationSet](id3dxcompressedanimationset.md)
</dt> <dt>

[**ID3DXCompressedAnimationSet::GetNumCallbackKeys**](id3dxcompressedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




