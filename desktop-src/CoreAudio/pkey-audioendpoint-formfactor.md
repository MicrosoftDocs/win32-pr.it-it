---
description: La proprietà PKEY \_ AudioEndpoint \_ FormFactor specifica il fattore di forma del dispositivo endpoint audio. Il fattore di forma indica gli attributi fisici del dispositivo endpoint audio modificato dall'utente.
ms.assetid: f49cb7da-3b50-47e2-90b4-1a885001b5d7
title: PKEY_AudioEndpoint_FormFactor (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e76b53b91a03cda5e8484878f62c3c7a205e422f53ed647d29cca6435e0f14f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018339"
---
# <a name="pkey_audioendpoint_formfactor"></a>PKEY \_ AudioEndpoint \_ FormFactor

La **proprietà PKEY \_ AudioEndpoint \_ FormFactor** specifica il fattore di forma del dispositivo endpoint audio. Il fattore di forma indica gli attributi fisici del dispositivo endpoint audio modificato dall'utente.

Il **membro vt** della **struttura PROPVARIANT** è impostato su VT \_ UI4.

Il **membro uintVal** della **struttura PROPVARIANT** contiene un valore di enumerazione di cui viene eseguito il cast al tipo UINT. È impostato su uno dei valori di [**enumerazione EndpointFormFactor**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor) seguenti:

-   RemoteNetworkDevice
-   Altoparlanti
-   LineLevel
-   Cuffie
-   Microfono
-   Cuffie
-   Portatile
-   UnknownDigitalPassthrough
-   Spdif
-   HDMI
-   UnknownFormFactor

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà dell'endpoint audio**](audio-endpoint-properties.md)
</dt> <dt>

[Proprietà audio di base](core-audio-properties.md)
</dt> </dl>

 

 




