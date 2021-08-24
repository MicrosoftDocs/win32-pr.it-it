---
description: Restituisce il numero di set di animazioni attualmente registrati nel controller di animazione.
ms.assetid: 1aacc84d-5025-4601-9a6c-84b3d9b06012
title: Metodo ID3DXAnimationController::GetNumAnimationSets (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetNumAnimationSets
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 07a6eee85c515c4b8e923aa9973eddc648ef95cbc152c27951154a7c41fbcf3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026821"
---
# <a name="id3dxanimationcontrollergetnumanimationsets-method"></a>Metodo ID3DXAnimationController::GetNumAnimationSets

Restituisce il numero di set di animazioni attualmente registrati nel controller di animazione.

## <a name="syntax"></a>Sintassi


```C++
UINT GetNumAnimationSets();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di set di animazione.

## <a name="remarks"></a>Commenti

Il controller contiene un numero qualsiasi di set di animazioni e tracce. I set di animazione possono essere registrati [**con RegisterAnimationOutput.**](id3dxanimationcontroller--registeranimationoutput.md) Un controller di animazione creato da una chiamata a [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) registrerà automaticamente i set di animazione caricati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
