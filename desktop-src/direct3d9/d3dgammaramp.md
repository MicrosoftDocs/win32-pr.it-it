---
description: Contiene i dati di rampa rossa, verde e blu.
ms.assetid: c596f47a-6c09-4b97-ab2f-b1da3d851aa4
title: Struttura D3DGAMMARAMP (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DGAMMARAMP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: fbd3acc35b7fd4998f5ba536c1fe4a28cf2a17153bf24aacde1f9f39bbbcd09e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751001"
---
# <a name="d3dgammaramp-structure"></a>Struttura D3DGAMMARAMP

Contiene i dati di rampa rossa, verde e blu.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DGAMMARAMP {
  WORD red[256];
  WORD green[256];
  WORD blue[256];
} D3DGAMMARAMP, *LPD3DGAMMARAMP;
```



## <a name="members"></a>Members

<dl> <dt>

**Rosso**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Matrice di 256 elementi WORD che descrive la rampa gamma rossa.

</dd> <dt>

**Verde**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Matrice di 256 elementi WORD che descrive la rampa gamma verde.

</dd> <dt>

**Blu**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Matrice di 256 elementi WORD che descrive la rampa gamma blu.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
</dt> <dt>

[**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
</dt> </dl>

 

 
