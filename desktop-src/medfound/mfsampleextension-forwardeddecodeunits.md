---
description: Ottiene un oggetto di tipo IMFCollection contenente oggetti IMFSample che contengono unità del livello di astrazione di rete (NALU) e unità SEI (Supplemental Enhancement Information) inoltrate da un decodificatore.
ms.assetid: F9FD7959-A78A-4C72-8326-EE8FF9066E6C
title: MFSampleExtension_ForwardedDecodeUnits attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2298a29d722c118fb79d5f0b49aa9d3d94fd735150a65772eb15e6da7638445
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713731"
---
# <a name="mfsampleextension_forwardeddecodeunits-attribute"></a>Attributo MFSampleExtension \_ ForwardedDecodeUnits

Ottiene un oggetto di tipo [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) contenente oggetti [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) contenenti unità del livello di astrazione di rete (NALU) e unità SEI (Supplemental Enhancement Information) inoltrate da un decodificatore.

## <a name="data-type"></a>Tipo di dati

**IUnknown**

## <a name="remarks"></a>Commenti

La raccolta contiene tutte le unità NALU/SEI personalizzate dal frame precedente con byte di prevenzione dell'emulazione rimossi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                          |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




