---
description: Abilita o Disabilita una traccia nel controller animazione.
ms.assetid: 8d06287b-e076-4553-962c-5c423e355101
title: 'Metodo ID3DXAnimationController:: SetTrackEnable (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 920576cbf630e061cd4d460315e905bdabf31ff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058660"
---
# <a name="id3dxanimationcontrollersettrackenable-method"></a>Metodo ID3DXAnimationController:: SetTrackEnable

Abilita o Disabilita una traccia nel controller animazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetTrackEnable(
  [in] UINT Track,
  [in] BOOL Enable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Traccia* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificatore della traccia da combinare.

</dd> <dt>

*Abilita* \[ in\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Abilita valore. Impostare su **true** per abilitare questa traccia nel controller oppure su **false** per impedire che venga mescolata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Per combinare una traccia con altre tracce, il flag di abilitazione deve essere impostato su **true**. Viceversa, se si imposta il flag su **false** , la traccia non verrà mescolata con altre tracce.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
