---
description: Le costanti ENDPOINT \_ HARDWARE SUPPORT XXX sono flag di supporto hardware per un dispositivo endpoint \_ \_ audio.
ms.assetid: 54032f75-2287-4589-bda5-e005ee077c41
title: ENDPOINT_HARDWARE_SUPPORT_XXX costanti (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c975a7bc00229943bb943035bf1fc84609414d83015ce4ae7d84d175b2e18a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053721"
---
# <a name="endpoint_hardware_support_xxx-constants"></a>Costanti \_ XXX DI SUPPORTO HARDWARE \_ \_ ENDPOINT

Le costanti ENDPOINT \_ HARDWARE SUPPORT XXX sono flag di supporto hardware per un dispositivo endpoint \_ \_ audio.



| Costante/valore                                                                                                                                                                                                                                                                           | Descrizione                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="ENDPOINT_HARDWARE_SUPPORT_VOLUME"></span><span id="endpoint_hardware_support_volume"></span><dl> <dt>**ENDPOINT \_ VOLUME \_ DI \_ SUPPORTO**</dt> HARDWARE <dt>0x00000001</dt> </dl> | Il dispositivo endpoint audio supporta un controllo del volume hardware.<br/> |
| <span id="ENDPOINT_HARDWARE_SUPPORT_MUTE"></span><span id="endpoint_hardware_support_mute"></span><dl> <dt>**ENDPOINT \_ SUPPORTO HARDWARE \_ \_ MUTE**</dt> <dt>0x00000002</dt> </dl>       | Il dispositivo endpoint audio supporta un controllo di disattivazione dell'audio hardware.<br/>   |
| <span id="ENDPOINT_HARDWARE_SUPPORT_METER"></span><span id="endpoint_hardware_support_meter"></span><dl> <dt>**ENDPOINT \_ CONTATORE \_ \_ DEL SUPPORTO**</dt> HARDWARE <dt>0x00000004</dt> </dl>    | Il dispositivo endpoint audio supporta un contatore di picco hardware.<br/>     |



## <a name="remarks"></a>Commenti

I [**metodi IAudioEndpointVolume::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) e [**IAudioMeterInformation::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) usano le costanti \_ ENDPOINT HARDWARE SUPPORT \_ \_ XXX.

Una maschera di supporto hardware indica le funzioni implementate da un dispositivo endpoint audio nell'hardware. La maschera può essere 0 o la combinazione OR bit per bit di una o più costanti ENDPOINT \_ HARDWARE \_ SUPPORT \_ XXX. Se nella maschera è impostato un bit che corrisponde a una determinata costante ENDPOINT HARDWARE SUPPORT XXX, significa che la funzione rappresentata da tale costante viene implementata \_ \_ \_ nell'hardware dal dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti audio di base](core-audio-constants.md)
</dt> <dt>

[**IAudioEndpointVolume::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport)
</dt> <dt>

[**IAudioMeterInformation::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport)
</dt> </dl>

 

 




