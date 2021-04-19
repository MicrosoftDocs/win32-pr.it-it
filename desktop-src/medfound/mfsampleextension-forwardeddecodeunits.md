---
description: Ottiene un oggetto di tipo IMFCollection contenente gli oggetti IMFSample che contengono le unità di astrazione del livello di rete (NALUs) e le informazioni sul miglioramento supplementare (SEI) che vengono trasmesse da un decodificatore.
ms.assetid: F9FD7959-A78A-4C72-8326-EE8FF9066E6C
title: Attributo MFSampleExtension_ForwardedDecodeUnits (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ab5c10a4a7fb4dfd201f9c494c1bc65e14c162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310241"
---
# <a name="mfsampleextension_forwardeddecodeunits-attribute"></a>\_Attributo ForwardedDecodeUnits di MFSampleExtension

Ottiene un oggetto di tipo [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) contenente gli oggetti [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) che contengono le unità di astrazione del livello di rete (NALUs) e le informazioni sul miglioramento supplementare (sei) che vengono trasmesse da un decodificatore.

## <a name="data-type"></a>Tipo di dati

**IUnknown**

## <a name="remarks"></a>Commenti

La raccolta contiene tutte le unità NALU/SEI personalizzate a partire dal fotogramma precedente con i byte di prevenzione dell'emulazione rimossi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




