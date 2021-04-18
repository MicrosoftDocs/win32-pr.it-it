---
description: Restituisce il numero di set di animazioni attualmente registrati nel controller di animazione.
ms.assetid: 1aacc84d-5025-4601-9a6c-84b3d9b06012
title: 'Metodo ID3DXAnimationController:: GetNumAnimationSets (D3dx9anim. h)'
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
ms.openlocfilehash: b5baedb0ea30d51cbd659e597cb000a434ec1632
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322147"
---
# <a name="id3dxanimationcontrollergetnumanimationsets-method"></a>Metodo ID3DXAnimationController:: GetNumAnimationSets

Restituisce il numero di set di animazioni attualmente registrati nel controller di animazione.

## <a name="syntax"></a>Sintassi


```C++
UINT GetNumAnimationSets();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di set di animazioni.

## <a name="remarks"></a>Commenti

Il controller contiene un numero qualsiasi di set di animazioni e tracce. I set di animazioni possono essere registrati con [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md). Un controller di animazione creato da una chiamata a [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) registrerà automaticamente i set di animazioni caricati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
