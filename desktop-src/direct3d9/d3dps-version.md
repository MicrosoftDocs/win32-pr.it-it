---
description: Creare un token di versione di pixel shader.
ms.assetid: 70089a93-83df-4ac4-8d98-4e1bb6ad2581
title: D3DPS_VERSION macro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c3f30d673145ec9dfe38bd8e2a636ac04c9a195a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355049"
---
# <a name="d3dps_version-macro"></a>D3DPS \_ versione macro

Creare un token di versione di pixel shader.

## <a name="syntax"></a>Sintassi


```C++
DWORD D3DPS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*\_Principali* 
</dt> <dd>

Versione principale del pixel shader.

</dd> <dt>

*\_Minorenne* 
</dt> <dd>

Versione secondaria del pixel shader.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore DWORD che è una versione pixel shader.

## <a name="remarks"></a>Commenti

Numeri di versione

Il numero di versione è una combinazione della versione principale e dei numeri di versione di vertex shader secondari. I numeri validi sono visualizzati nella tabella.



| Principale | Minorenne | Esempio             |
|-------|-------|---------------------|
| 1     | 1     | \_Versione di D3DPS (1,1) |
| 1     | 2     | \_Versione di D3DPS (1, 2) |
| 1     | 3     | \_Versione di D3DPS (1,3) |
| 1     | 4     | \_Versione di D3DPS (1,4) |
| 2     | 0     | \_Versione di D3DPS (2, 0) |
| 3     | 0     | \_Versione di D3DPS (3, 0) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[D3DCAPS9](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> </dl>

 

 




