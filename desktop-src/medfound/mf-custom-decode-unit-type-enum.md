---
description: Specifica il tipo di unità contenuta in un IMFSample in una \_ raccolta ForwardedDecodeUnits MFSampleExtension.
ms.assetid: B74890ED-9586-475B-8C77-457ECB893980
title: Enumerazione MF_CUSTOM_DECODE_UNIT_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_CUSTOM_DECODE_UNIT_TYPE
api_type:
- HeaderDef
api_location:
- mfapi.h
ms.openlocfilehash: 406f6b3f6b93ced212ccf06910b69761ac0dfd9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226647"
---
# <a name="mf_custom_decode_unit_type-enumeration"></a>\_Enumerazione del \_ tipo di \_ unità di decodifica personalizzato MF \_

Specifica il tipo di unità contenuta in un [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) in una raccolta [ \_ ForwardedDecodeUnits MFSampleExtension](mfsampleextension-forwardeddecodeunits.md) .

## <a name="members"></a>Membri



| Membro                    | Descrizione                                                             | Valore |
|---------------------------|-------------------------------------------------------------------------|-------|
| **MF \_ Decode \_ unit \_ NAL** | Il tipo di unità è NALU (Network Abstraction Layer Unit). <br/>     | 0     |
| **MF \_ decodifica \_ unità \_ sei** | Il tipo di unità è informazioni aggiuntive sul miglioramento (SEI).<br/> | 1     |



## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




