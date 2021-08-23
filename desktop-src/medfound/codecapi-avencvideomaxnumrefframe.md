---
description: Specifica il numero massimo di fotogrammi di riferimento supportati dal codificatore.
ms.assetid: 023FD791-BD43-41F6-95D0-8BE800F51579
title: CODECAPI_AVEncVideoMaxNumRefFrame proprietà (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e11e7325628f0e7c1e6560d3fc734b34e8a032a3fbf3630aa1fb5959cec33a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606421"
---
# <a name="codecapi_avencvideomaxnumrefframe-property"></a>PROPRIETÀ CODECAPI \_ AVEncVideoMaxNumRefFrame

Specifica il numero massimo di fotogrammi di riferimento supportati dal codificatore.

## <a name="data-type"></a>Tipo di dati

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncVideoMaxNumRefFrame**

## <a name="remarks"></a>Commenti

Per H.264, viene eseguito il mapping alla variabile Sequence Parameter Set **max \_ num ref \_ \_ frames** come definito nella specifica H.264.

**Codificatori H.264/AVC:**

I codificatori possono usare un numero inferiore di fotogrammi di riferimento per rispettare il livello specificato nel flusso di bit.

I codificatori devono [**supportare GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRangee**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).

Si tratta di una proprietà statica che indica che può essere impostata solo prima dell'avvio della sessione di codifica.

Il valore predefinito consigliato è 2.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                   |
| Server minimo supportato<br/> | Windows Server 2012 App \[ UWP per app desktop \| R2\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

