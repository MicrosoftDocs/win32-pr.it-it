---
description: Creare un token pixel shader versione.
ms.assetid: 70089a93-83df-4ac4-8d98-4e1bb6ad2581
title: D3DPS_VERSION macro (D3d9types.h)
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
ms.openlocfilehash: a3958cfaa3afe06e22015a28e8e1ebfd8799c01e89772eb9794dd1249cc0df9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750901"
---
# <a name="d3dps_version-macro"></a>Macro D3DPS \_ VERSION

Creare un token pixel shader versione.

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

La versione pixel shader principale.

</dd> <dt>

*\_Minorenne* 
</dt> <dd>

Versione secondaria pixel shader secondaria.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore DWORD che rappresenta una pixel shader versione.

## <a name="remarks"></a>Commenti

Numeri di versione

Il numero di versione è una combinazione della versione principale e dei numeri di versione del vertex shader secondario. I numeri validi vengono visualizzati nella tabella.



| Principale | Minorenne | Esempio             |
|-------|-------|---------------------|
| 1     | 1     | VERSIONE \_ D3DPS(1,1) |
| 1     | 2     | VERSIONE \_ D3DPS(1,2) |
| 1     | 3     | VERSIONE \_ D3DPS(1,3) |
| 1     | 4     | VERSIONE \_ D3DPS(1,4) |
| 2     | 0     | VERSIONE \_ D3DPS(2,0) |
| 3     | 0     | VERSIONE D3DPS \_ (3,0) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[D3DCAPS9](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> </dl>

 

 




