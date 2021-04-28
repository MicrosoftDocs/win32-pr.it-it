---
description: 'Metodo ID3DXSkinInfo::GetFVF: ottiene il valore del vertice della funzione fissa.'
ms.assetid: 9b80c4b9-2e5b-4965-99b9-ad6c459ef413
title: Metodo ID3DXSkinInfo::GetFVF (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3415f86f778fbb6fb3592927277e399584bc49a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107159"
---
# <a name="id3dxskininfogetfvf-method"></a>Metodo ID3DXSkinInfo::GetFVF

Ottiene il valore del vertice della funzione fissa.

## <a name="syntax"></a>Sintassi


```C++
DWORD GetFVF();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Restituisce i codici FVF (Flexible Vertex Format).

## <a name="remarks"></a>Commenti

Questo metodo può restituire 0 se il formato del vertice non può essere mappato direttamente a un codice FVF. Ciò si verifica per una mesh creata da una dichiarazione di vertice che non ha lo stesso ordine e gli elementi supportati dai codici FVF.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetFVF**](id3dxskininfo--setfvf.md)
</dt> </dl>

 

 
