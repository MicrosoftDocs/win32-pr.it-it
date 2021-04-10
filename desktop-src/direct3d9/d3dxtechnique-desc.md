---
description: Descrive una tecnica utilizzata da un effetto.
ms.assetid: 7ba2dbb3-8039-4d1c-ad9d-130d9bf3d80a
title: Struttura D3DXTECHNIQUE_DESC (D3dx9effect. h)
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
ms.openlocfilehash: 35dd483a983f17371d6a77e6c020b3a45d9e9360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058598"
---
# <a name="d3dxtechnique_desc-structure"></a>\_Struttura D3DXTECHNIQUE DESC

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

Stringa che contiene il nome della tecnica.

</dd> <dt>

**Passa**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di passaggi di rendering necessari per la tecnica. Vedere la sezione Osservazioni.

</dd> <dt>

**annotazioni**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di annotazioni. Vedere [aggiungere informazioni ai parametri di effetto con le \_ annotazioni](using-an-effect.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Alcune schede video possono eseguire il rendering di due trame in un singolo passaggio. Tuttavia, se una scheda non dispone di questa funzionalità, spesso è possibile eseguire il rendering dello stesso effetto in due passaggi, usando una trama per ogni passaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture degli effetti](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
