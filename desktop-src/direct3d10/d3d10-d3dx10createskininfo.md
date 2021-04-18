---
description: Crea un oggetto mesh dell'interfaccia vuota utilizzando un dichiaratore.
ms.assetid: 5356cfe5-de90-462d-9722-72f3618decfb
title: Funzione D3DX10CreateSkinInfo (D3DX10Mesh. h)
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
ms.openlocfilehash: a68da20c2e2e15e3b73d55ee1df70518bba46200
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323273"
---
# <a name="d3dx10createskininfo-function"></a>D3DX10CreateSkinInfo (funzione)

Crea un oggetto mesh dell'interfaccia vuota utilizzando un dichiaratore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10CreateSkinInfo(
  _Out_ LPD3DX10SKININFO *ppSkinInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppSkinInfo* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DX10SKININFO**](id3dx10skininfo.md)\***

Indirizzo di un puntatore a un' [**interfaccia ID3DX10SkinInfo**](id3dx10skininfo.md), che rappresenta l'oggetto mesh interfaccia creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere: E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Usare [**ID3DX10SkinInfo:: SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md) per popolare l'oggetto mesh dell'interfaccia vuota restituito da questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[Funzioni D3DX](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 




