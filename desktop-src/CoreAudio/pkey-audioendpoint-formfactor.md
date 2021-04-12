---
description: La \_ Proprietà pkey AudioEndpoint \_ FormFactor specifica il fattore di forma del dispositivo dell'endpoint audio. Il fattore di forma indica gli attributi fisici del dispositivo dell'endpoint audio modificato dall'utente.
ms.assetid: f49cb7da-3b50-47e2-90b4-1a885001b5d7
title: PKEY_AudioEndpoint_FormFactor (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5833470e2a2848f9454f3b5eefbf852f452f033
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483684"
---
# <a name="pkey_audioendpoint_formfactor"></a>PKEY \_ AudioEndpoint \_ FormFactor

La proprietà **pkey \_ AudioEndpoint \_ FormFactor** specifica il fattore di forma del dispositivo dell'endpoint audio. Il fattore di forma indica gli attributi fisici del dispositivo dell'endpoint audio modificato dall'utente.

Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ UI4.

Il membro **uintVal** della struttura **PROPVARIANT** contiene un valore di enumerazione di cui è stato eseguito il cast al tipo uint. Viene impostato su uno dei seguenti valori di enumerazione [**EndpointFormFactor**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor) :

-   RemoteNetworkDevice
-   Altoparlanti
-   LineLevel
-   Cuffie
-   Microfono
-   Cuffie
-   Portatile
-   UnknownDigitalPassthrough
-   SPDIF
-   HDMI
-   UnknownFormFactor

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà endpoint audio**](audio-endpoint-properties.md)
</dt> <dt>

[Proprietà audio principali](core-audio-properties.md)
</dt> </dl>

 

 




