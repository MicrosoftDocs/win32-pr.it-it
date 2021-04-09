---
description: La \_ Proprietà pkey AudioEndpoint \_ ControlPanelPageProvider specifica il CLSID del provider registrato dell'estensione delle proprietà del dispositivo per il dispositivo dell'endpoint audio.
ms.assetid: 429a7572-b609-46fd-946e-ee34ddd6cc5e
title: PKEY_AudioEndpoint_ControlPanelPageProvider (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205ccdfba799652d9b09af21eefbedd3c3049533
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877797"
---
# <a name="pkey_audioendpoint_controlpanelpageprovider"></a>PKEY \_ AudioEndpoint \_ ControlPanelPageProvider

La proprietà **pkey \_ AudioEndpoint \_ CONTROLPANELPAGEPROVIDER** specifica il CLSID del provider registrato dell'estensione delle proprietà del dispositivo per il dispositivo dell'endpoint audio. L'estensione fornisce le proprietà dell'endpoint audio visualizzate nella pagina dispositivo-proprietà del pannello di controllo multimediale di Windows, Mmsys.cpl. Per ulteriori informazioni su Mmsys.cpl, vedere la documentazione di Windows DDK.

Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ LPWSTR.

Il membro **pwszVal** della struttura **PROPVARIANT** punta a una stringa di caratteri wide con terminazione null contenente un GUID che identifica il provider dell'estensione del pannello di controllo.

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

 

 




