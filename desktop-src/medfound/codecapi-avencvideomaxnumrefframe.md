---
description: Specifica il numero massimo di frame di riferimento supportati dal codificatore.
ms.assetid: 023FD791-BD43-41F6-95D0-8BE800F51579
title: Proprietà CODECAPI_AVEncVideoMaxNumRefFrame (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e8f5a7794410012bd1a025e794e1fd23f4b332
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132162"
---
# <a name="codecapi_avencvideomaxnumrefframe-property"></a>Proprietà AVEncVideoMaxNumRefFrame di codecapi \_

Specifica il numero massimo di frame di riferimento supportati dal codificatore.

## <a name="data-type"></a>Tipo di dati

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncVideoMaxNumRefFrame**

## <a name="remarks"></a>Commenti

Per H. 264, viene eseguito il mapping alla variabile del set di parametri Sequence **Max \_ num \_ \_ frame Ref** come definito nella specifica H. 264.

**Codificatori H. 264/AVC:**

I codificatori possono usare un minor numero di frame di riferimento per rispettare il livello specificato nel bitstream.

I codificatori devono supportare [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRangee**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).

Si tratta di una proprietà statica che significa che può essere impostata solo prima dell'avvio della sessione di codifica.

Il valore predefinito consigliato è 2.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                   |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

