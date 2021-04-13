---
description: Definisce gli schemi di bit che abilitano i piani di ritaglio definiti dall'utente. Queste macro sono definite come praticità quando si impostano i valori per lo \_ stato di rendering CLIPPLANEENABLE di D3DRS.
ms.assetid: 5bca2401-a3fb-4b1c-bb59-621b15da10f1
title: Macro D3DCLIPPLANEn (D3D9Types. h)
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
ms.openlocfilehash: 4508f1654a357eb80b3847b7562e230c6a9be4d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401942"
---
# <a name="d3dclipplanen-macro"></a>D3DCLIPPLANEn (macro)

Definisce gli schemi di bit che abilitano i piani di ritaglio definiti dall'utente. Queste macro sono definite come praticità quando si impostano i valori per lo \_ stato di rendering CLIPPLANEENABLE di D3DRS.

## <a name="syntax"></a>Sintassi


```C++
void D3DCLIPPLANEn(void);
```



## <a name="parameters"></a>Parametri

Questa macro non contiene parametri.

## <a name="return-value"></a>Valore restituito

Questa macro non restituisce un valore.

## <a name="remarks"></a>Commenti

I piani di ritaglio definiti dall'utente sono abilitati quando il valore impostato nello \_ stato di rendering CLIPPLANEENABLE di D3DRS contiene uno o più bit impostati, ovvero non è 0. Il valore dello stato di rendering non è importante; il sistema non interpreta il valore come numero. Il valore Abilita invece il piano di ritaglio il cui bit corrispondente è impostato. Il bit 0 controlla lo stato del primo piano di ritaglio (in corrispondenza dell'indice 0), il bit 1 il secondo piano e così via.

Gli schemi di bit creati da queste macro possono essere combinati utilizzando un'operazione OR logica per abilitare simultaneamente più piani di ritaglio. Se si omette una di queste macro dalla combinazione, il piano di ritaglio viene disabilitato in corrispondenza di tale indice.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




