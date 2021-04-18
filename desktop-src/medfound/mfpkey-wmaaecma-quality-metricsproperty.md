---
description: Recupera le metriche qualitative nell'annullamento dell'eco acustico (AEC) dal DSP di acquisizione voce.
ms.assetid: de2e86ae-0469-471f-9105-0bb38a59b428
title: Proprietà MFPKEY_WMAAECMA_QUALITY_METRICS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3740630bc23c4e3e0e824e55b4e34bcd8b1347f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309116"
---
# <a name="mfpkey_wmaaecma_quality_metrics-property"></a>\_ \_ Proprietà metrica qualità MFPKEY WMAAECMA \_

Recupera le metriche qualitative nell'annullamento dell'eco acustico (AEC) dal DSP di acquisizione voce.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

\_BLOB VT

## <a name="remarks"></a>Commenti

Il valore di questa proprietà è una struttura dello [ \_ struct AecQualityMetrics](/windows/win32/api/wmcodecdsp/ns-wmcodecdsp-aecqualitymetrics_struct) . Questa proprietà è di sola lettura.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP di acquisizione vocale](voicecapturedmo.md)
</dt> </dl>

 

 
