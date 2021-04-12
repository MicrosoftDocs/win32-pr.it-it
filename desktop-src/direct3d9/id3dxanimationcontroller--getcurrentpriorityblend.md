---
description: Restituisce un handle di evento a un evento di combinazione di priorità attualmente in esecuzione.
ms.assetid: a7184459-7644-4e65-a8ea-13019889e02b
title: 'Metodo ID3DXAnimationController:: GetCurrentPriorityBlend (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: df8b52a5bd5267cf88eaf101a0589000099dd600
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355794"
---
# <a name="id3dxanimationcontrollergetcurrentpriorityblend-method"></a>Metodo ID3DXAnimationController:: GetCurrentPriorityBlend

Restituisce un handle di evento a un evento di combinazione di priorità attualmente in esecuzione.

## <a name="syntax"></a>Sintassi


```C++
D3DXEVENTHANDLE GetCurrentPriorityBlend();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle dell'evento per l'evento di combinazione di priorità attualmente in esecuzione. Se non è attualmente in esecuzione alcun evento di Blend di priorità, viene restituito **null** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




