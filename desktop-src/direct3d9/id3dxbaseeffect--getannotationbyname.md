---
description: Ottiene l'handle di un'annotazione cercandone il nome.
ms.assetid: da4e2805-5f06-4a9b-836f-85a8c154c502
title: 'Metodo ID3DXBaseEffect:: GetAnnotationByName (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotationByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 00698030488b8f4ae788367f87b8d569476292ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323613"
---
# <a name="id3dxbaseeffectgetannotationbyname-method"></a>Metodo ID3DXBaseEffect:: GetAnnotationByName

Ottiene l'handle di un'annotazione cercandone il nome.

## <a name="syntax"></a>Sintassi


```C++
D3DXHANDLE GetAnnotationByName(
  [in] D3DXHANDLE hObject,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hObject* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle di una tecnica, un passaggio o un parametro di primo livello. Vedere [handle (Direct3D 9)](handles.md).

</dd> <dt>

*pname* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Stringa contenente il nome dell'annotazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Restituisce l'handle dell'annotazione specificata o **null** se il nome non è stato trovato. Vedere [handle (Direct3D 9)](handles.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
