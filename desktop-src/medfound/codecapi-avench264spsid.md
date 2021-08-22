---
description: Imposta l'identificatore del set di parametri di sequenza (SPS) nell'unità NAL (Network Abstraction Layer) SPS del flusso H.264 bit.
ms.assetid: 583DD539-6EE8-4DD4-A0FE-D2BBE1A4302F
title: CODECAPI_AVEncH264SPSID proprietà (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da06e431a3747e676e3934ac9a261e1d0e1ec37e18bacf01f8a3e623c4257488
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664661"
---
# <a name="codecapi_avench264spsid-property"></a>CODECAPI \_ AVEncH264SPSID - proprietà

Imposta l'identificatore del set di parametri di sequenza (SPS) nell'unità NAL (Network Abstraction Layer) SPS del flusso H.264 bit.

## <a name="data-type"></a>Tipo di dati

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncH264SPSID**

## <a name="property-value"></a>Valore proprietà

Specifica il valore di **seq \_ parameter set \_ \_ id** nell'unità SPS NAL. **L'elemento sintassi seq \_ parameter set \_ \_ id** identifica il set di parametri della sequenza. Il flusso di bit risultante può essere concatenato con altri flussi di bit, per produrre un flusso di bit più lungo che contiene più set di parametri di sequenza con identificatori SPS diversi.

L'intervallo valido è 0 31, come specificato nella specifica H.264/AVC.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                     |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

