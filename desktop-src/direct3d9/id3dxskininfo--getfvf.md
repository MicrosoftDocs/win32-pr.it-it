---
description: Ottiene il valore del vertice della funzione fissa.
ms.assetid: 9b80c4b9-2e5b-4965-99b9-ad6c459ef413
title: 'Metodo ID3DXSkinInfo:: GetFVF (D3DX9Mesh. h)'
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
ms.openlocfilehash: 6d48cd9cea6efd6cb43e6da6877a7aaf42909c71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354069"
---
# <a name="id3dxskininfogetfvf-method"></a>Metodo ID3DXSkinInfo:: GetFVF

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

Questo metodo può restituire 0 se non è possibile eseguire il mapping diretto del formato vertex a un codice FVF. Ciò si verifica per una mesh creata da una dichiarazione di vertice che non ha lo stesso ordine e gli stessi elementi supportati dai codici FVF.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetFVF**](id3dxskininfo--setfvf.md)
</dt> </dl>

 

 
