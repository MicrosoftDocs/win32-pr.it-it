---
description: Le \_ costanti xxx del supporto hardware dell'endpoint \_ \_ sono flag di supporto hardware per un dispositivo endpoint audio.
ms.assetid: 54032f75-2287-4589-bda5-e005ee077c41
title: Costanti ENDPOINT_HARDWARE_SUPPORT_XXX (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffb5b2255330b205519ce3065ccb5f7eebb6b65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127666"
---
# <a name="endpoint_hardware_support_xxx-constants"></a>\_ \_ Costanti xxx supporto hardware endpoint \_

Le \_ costanti xxx del supporto hardware dell'endpoint \_ \_ sono flag di supporto hardware per un dispositivo endpoint audio.



| Costante/valore                                                                                                                                                                                                                                                                           | Descrizione                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="ENDPOINT_HARDWARE_SUPPORT_VOLUME"></span><span id="endpoint_hardware_support_volume"></span><dl> <dt>**Endpoint \_ di \_ \_ Volume di supporto hardware**</dt> <dt>0x00000001</dt> </dl> | Il dispositivo dell'endpoint audio supporta un controllo volume hardware.<br/> |
| <span id="ENDPOINT_HARDWARE_SUPPORT_MUTE"></span><span id="endpoint_hardware_support_mute"></span><dl> <dt>**Endpoint \_ di Supporto HARDWARE 0x00000002 \_ \_ mute**</dt> <dt></dt> </dl>       | Il dispositivo dell'endpoint audio supporta un controllo di silenziamento hardware.<br/>   |
| <span id="ENDPOINT_HARDWARE_SUPPORT_METER"></span><span id="endpoint_hardware_support_meter"></span><dl> <dt>**Endpoint \_ di 0x00000004 \_ di \_ misurazione del supporto hardware**</dt> <dt></dt> </dl>    | Il dispositivo dell'endpoint audio supporta un contatore hardware di picco.<br/>     |



## <a name="remarks"></a>Commenti

I metodi [**IAudioEndpointVolume:: QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) e [**IAudioMeterInformation:: QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) usano le \_ \_ costanti xxx del supporto hardware dell'endpoint \_ .

Una maschera di supporto hardware indica le funzioni implementate da un dispositivo dell'endpoint audio nell'hardware. La maschera può essere 0 o la combinazione bit per bit di uno o più \_ componenti hardware endpoint \_ supporta le \_ costanti xxx. Se nella maschera è impostato un bit che corrisponde a una particolare \_ costante del supporto hardware di un endpoint \_ \_ , significa che la funzione rappresentata da tale costante è implementata nell'hardware dal dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti audio Core](core-audio-constants.md)
</dt> <dt>

[**IAudioEndpointVolume::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport)
</dt> <dt>

[**IAudioMeterInformation::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport)
</dt> </dl>

 

 




