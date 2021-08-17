---
description: 'Struttura D3DCOLORVALUE (D3D9Types.h): descrive i valori dei colori.'
ms.assetid: 6af8c2ec-bc79-4dc6-b56d-7a7676a50b39
title: Struttura D3DCOLORVALUE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b8c188e1b50905abd61184c7e1fe67d4253e920aa26d5d1782c1633d843bd282
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733353"
---
# <a name="d3dcolorvalue-structure-d3d9typesh"></a>Struttura D3DCOLORVALUE (D3D9Types.h)

Descrive i valori dei colori.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a>Members

<dl> <dt>

**r**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valore a virgola mobile che specifica il componente rosso di un colore. Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0. Il valore 0,0 indica l'assenza completa del componente rosso, mentre il valore 1,0 indica che il rosso è completamente presente.

</dd> <dt>

**G**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valore a virgola mobile che specifica il componente verde di un colore. Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0. Il valore 0,0 indica l'assenza completa del componente verde, mentre il valore 1,0 indica che il verde è completamente presente.

</dd> <dt>

**b**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valore a virgola mobile che specifica il componente blu di un colore. Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0. Il valore 0,0 indica l'assenza completa del componente blu, mentre il valore 1,0 indica che il blu è completamente presente.

</dd> <dt>

**Un**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valore a virgola mobile che specifica il componente alfa di un colore. Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0. Il valore 0,0 indica completamente trasparente, mentre un valore pari a 1,0 indica completamente opaco.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile impostare i membri di questa struttura su valori esterni all'intervallo compreso tra 0 e 1 per implementare alcuni effetti insoliti. I valori maggiori di 1 producono luci forti che tendono a lavare una scena. I valori negativi producono luci scure che rimuovono effettivamente la luce da una scena.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 




