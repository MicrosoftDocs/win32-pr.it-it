---
description: Ottiene l'handle di un'annotazione.
ms.assetid: 433d73b7-9371-4d76-8b34-a64c608eb1a3
title: 'Metodo ID3DXBaseEffect:: GetAnnotation (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotation
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: aad446e436478c8c7673a1919879983437fd9602
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323614"
---
# <a name="id3dxbaseeffectgetannotation-method"></a>Metodo ID3DXBaseEffect:: GetAnnotation

Ottiene l'handle di un'annotazione.

## <a name="syntax"></a>Sintassi


```C++
D3DXHANDLE GetAnnotation(
  [in] D3DXHANDLE hObject,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hObject* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle di una tecnica, un passaggio o un parametro di primo livello. Vedere [handle (Direct3D 9)](handles.md).

</dd> <dt>

*Indice* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice delle annotazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Restituisce l'handle dell'annotazione specificata o **null** se l'indice non è valido. Vedere [handle (Direct3D 9)](handles.md).

## <a name="remarks"></a>Commenti

Le annotazioni sono dati specifici dell'utente che possono essere collegati a qualsiasi tecnica, passaggio o parametro. Vedere [handle (Direct3D 9)](handles.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
