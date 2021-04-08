---
description: 'Termina la durata del puntatore ppData restituito da ID3DXFileData:: Lock.'
ms.assetid: 6032ea1f-3c73-4157-ba3f-41ce9e73d64c
title: 'Metodo ID3DXFileData:: Unlock (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Unlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8371b87152a6184f34a225b24d2de1b0fd21248f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762142"
---
# <a name="id3dxfiledataunlock-method"></a>Metodo ID3DXFileData:: Unlock

Termina la durata del puntatore *ppData* restituito da [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md).

## <a name="syntax"></a>Sintassi


```C++
BOOL Unlock();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Il valore restituito è S \_ OK.

## <a name="remarks"></a>Commenti

È necessario assicurarsi che il numero di chiamate a [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md) corrisponda al numero di chiamate **ID3DXFileData:: Unlock** . Dopo la chiamata a unlock, il puntatore ppData restituito da **ID3DXFileData:: Lock** non deve più essere utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
