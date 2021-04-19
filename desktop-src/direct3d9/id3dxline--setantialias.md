---
description: Consente di abilitare l'anti-aliasing della linea.
ms.assetid: 9c212823-2dc6-40dd-b1aa-9fc4a2c540f4
title: 'Metodo ID3DXLine:: SetAntialias (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetAntialias
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893e2061beedb6d45dc86e87903613984e3d1785
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323726"
---
# <a name="id3dxlinesetantialias-method"></a>Metodo ID3DXLine:: SetAntialias

Consente di abilitare l'anti-aliasing della linea.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetAntialias(
  [in] BOOL bAntiAlias
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bAntiAlias* \[ in\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Attiva e disattiva l'anti-aliasing. **True** attiva l'anti-aliasing e **false** disattiva l'anti-aliasing.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine::GetAntialias**](id3dxline--getantialias.md)
</dt> </dl>

 

 
