---
description: Descrive una tecnica utilizzata da un effetto.
ms.assetid: 7ba2dbb3-8039-4d1c-ad9d-130d9bf3d80a
title: D3DXTECHNIQUE_DESC struttura (D3dx9effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTECHNIQUE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 7e835c0eac067825942568464df8d5d345a06b530b71b7eaf7f319eae5f5d366
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119630731"
---
# <a name="d3dxtechnique_desc-structure"></a>Struttura D3DXTECHNIQUE \_ DESC

Descrive una tecnica utilizzata da un effetto.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXTECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DXTECHNIQUE_DESC, *LPD3DXTECHNIQUE_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Stringa contenente il nome della tecnica.

</dd> <dt>

**Passa**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di passaggi di rendering necessari per la tecnica. Vedere la sezione Osservazioni.

</dd> <dt>

**Annotazioni**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di annotazioni. Vedere [Aggiungere informazioni ai parametri degli effetti con \_ annotazioni.](using-an-effect.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Alcune schede video possono eseguire il rendering di due trame in un unico passaggio. Tuttavia, se una scheda non ha questa funzionalità, è spesso possibile eseguire il rendering dello stesso effetto in due passaggi, usando una trama per ogni passaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9effect.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture degli effetti](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
