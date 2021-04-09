---
description: Imposta l'identificatore SPS (Sequence Parameter Set) nell'unità SPS Network Abstraction Layer (NAL) del flusso di bit H. 264.
ms.assetid: 583DD539-6EE8-4DD4-A0FE-D2BBE1A4302F
title: Proprietà CODECAPI_AVEncH264SPSID (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e06fb78fc128b2eec5db2c61faf70ee10a5eba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127982"
---
# <a name="codecapi_avench264spsid-property"></a>Proprietà AVEncH264SPSID di codecapi \_

Imposta l'identificatore SPS (Sequence Parameter Set) nell'unità SPS Network Abstraction Layer (NAL) del flusso di bit H. 264.

## <a name="data-type"></a>Tipo di dati

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncH264SPSID**

## <a name="property-value"></a>Valore proprietà

Specifica il valore dell' **\_ \_ \_ ID set di parametri Seq** nell'unità NAL SPS. L'elemento della sintassi dell' **\_ \_ \_ ID set di parametri Seq** identifica il set di parametri di sequenza. Il flusso di bit risultante può essere concatenato con altri flussi di bit, per produrre un flusso di bit più lungo che contiene più set di parametri di sequenza con identificatori SPS diversi.

L'intervallo valido è 0 31, come specificato nella specifica H. 264/AVC.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                     |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

