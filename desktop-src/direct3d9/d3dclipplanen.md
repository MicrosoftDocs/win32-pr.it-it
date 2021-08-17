---
description: Definisce modelli di bit che abilitano i piani di ritaglio definiti dall'utente. Queste macro vengono definite per praticità quando si impostano i valori per lo stato di rendering D3DRS \_ CLIPPLANEENABLE.
ms.assetid: 5bca2401-a3fb-4b1c-bb59-621b15da10f1
title: Macro D3DCLIPPLANEn (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPPLANEn
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 315f1cdd8f8835b869f04edd9869243f3e05a9c2c9a08a41eeffc014727b3fc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805468"
---
# <a name="d3dclipplanen-macro"></a>Macro D3DCLIPPLANEn

Definisce modelli di bit che abilitano i piani di ritaglio definiti dall'utente. Queste macro vengono definite per praticità quando si impostano i valori per lo stato di rendering D3DRS \_ CLIPPLANEENABLE.

## <a name="syntax"></a>Sintassi


```C++
void D3DCLIPPLANEn(void);
```



## <a name="parameters"></a>Parametri

Questa macro non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa macro non restituisce un valore.

## <a name="remarks"></a>Commenti

I piani di ritaglio definiti dall'utente sono abilitati quando il valore impostato nello stato di rendering D3DRS CLIPPLANEENABLE contiene uno o più bit impostati ,ovvero non è \_ 0. Il valore dello stato di rendering non è importante. il sistema non interpreta il valore come numero. Il valore abilita invece il piano di ritaglio di cui è impostato il bit corrispondente. Il bit 0 controlla lo stato del primo piano di ritaglio (in corrispondenza dell'indice 0), il bit 1 del secondo piano e così via.

I modelli di bit creati da queste macro possono essere combinati usando un'operazione OR logica per abilitare contemporaneamente più piani di ritaglio. Se si omette una di queste macro dalla combinazione, il piano di ritaglio in corrispondenza dell'indice viene disabilitato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




