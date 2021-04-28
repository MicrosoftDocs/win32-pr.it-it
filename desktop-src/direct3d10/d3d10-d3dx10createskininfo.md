---
description: "Funzione D3DX10CreateSkinInfo: crea un oggetto mesh dell'interfaccia vuota usando un dichiaratore."
ms.assetid: 5356cfe5-de90-462d-9722-72f3618decfb
title: Funzione D3DX10CreateSkinInfo (D3DX10Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSkinInfo
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 17d6ec99d3f43c41d56deebef81a021c81ec1d69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103599"
---
# <a name="d3dx10createskininfo-function"></a>Funzione D3DX10CreateSkinInfo

Crea un oggetto mesh dell'interfaccia vuota usando un dichiaratore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10CreateSkinInfo(
  _Out_ LPD3DX10SKININFO *ppSkinInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppSkinInfo* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DX10SKININFO**](id3dx10skininfo.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DX10SkinInfo**](id3dx10skininfo.md)che rappresenta l'oggetto mesh dell'interfaccia creata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Usare [**ID3DX10SkinInfo::SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md) per popolare l'oggetto mesh dell'interfaccia vuota restituito da questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[Funzioni D3DX](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 




