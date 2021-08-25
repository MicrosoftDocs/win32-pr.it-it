---
description: La proprietà PKEY \_ AudioEndpoint ControlPanelPageProvider specifica il CLSID del provider registrato dell'estensione \_ device-properties per il dispositivo endpoint audio.
ms.assetid: 429a7572-b609-46fd-946e-ee34ddd6cc5e
title: PKEY_AudioEndpoint_ControlPanelPageProvider (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc39f471649487dcdbfc2fa94371466eabd9ec59a8f9de19bdeafcec9d4283b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695351"
---
# <a name="pkey_audioendpoint_controlpanelpageprovider"></a>PKEY \_ AudioEndpoint \_ ControlPanelPageProvider

La **proprietà PKEY \_ AudioEndpoint \_ ControlPanelPageProvider** specifica il CLSID del provider registrato dell'estensione device-properties per il dispositivo endpoint audio. L'estensione fornisce le proprietà dell'endpoint audio visualizzate nella pagina delle proprietà del dispositivo del pannello Windows di controllo multimediale, Mmsys.cpl. Per altre informazioni sui Mmsys.cpl, vedere la documentazione Windows DDK.

Il **membro vt** della **struttura PROPVARIANT** è impostato su VT \_ LPWSTR.

Il **membro pwszVal** della struttura **PROPVARIANT** punta a una stringa di caratteri wide con terminazione Null che contiene un GUID che identifica il provider dell'estensione del pannello di controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà dell'endpoint audio**](audio-endpoint-properties.md)
</dt> <dt>

[Proprietà audio principali](core-audio-properties.md)
</dt> </dl>

 

 




