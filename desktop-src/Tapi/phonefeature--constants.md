---
description: Le \_ costanti PHONEFEATURE elencano le operazioni che possono essere richiamate su un telefono tramite questa API. Ognuno dei valori di PHONEFEATURE \_ (ad eccezione di PHONEFEATURE \_ GENERICPHONE) corrisponde a una funzione TAPI con un nome identico o simile.
ms.assetid: 361b3080-3650-48a2-a1b7-f05d72777f9a
title: Costanti PHONEFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6e0333135df4185348f3471aa4184a0cd93e907
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333950"
---
# <a name="phonefeature_-constants"></a>\_Costanti PHONEFEATURE

Le **costanti \_ PHONEFEATURE** elencano le operazioni che possono essere richiamate su un telefono tramite questa API. Ognuno dei valori di PHONEFEATURE \_ (ad eccezione di PHONEFEATURE \_ GENERICPHONE) corrisponde a una funzione TAPI con un nome identico o simile.



| Costante/valore                                                                                                                                                                                                                                                                            | Descrizione                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="PHONEFEATURE_GETBUTTONINFO"></span><span id="phonefeature_getbuttoninfo"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x00000001</dt> GETBUTTONINFO </dl>                      | [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)<br/>                             |
| <span id="PHONEFEATURE_GETDATA"></span><span id="phonefeature_getdata"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x00000002</dt> GetData </dl>                                        | [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata)<br/>                                         |
| <span id="PHONEFEATURE_GETDISPLAY"></span><span id="phonefeature_getdisplay"></span><dl> <dt>**PHONEFEATURE \_ GetDisplay**</dt> <dt>0x00000004</dt> </dl>                               | [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay)<br/>                                   |
| <span id="PHONEFEATURE_GETGAINHANDSET"></span><span id="phonefeature_getgainhandset"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x00000008</dt> GETGAINHANDSET </dl>                   | [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) PHONEHOOKSWITCHDEV \_ portatile<br/>             |
| <span id="PHONEFEATURE_GETGAINSPEAKER"></span><span id="phonefeature_getgainspeaker"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x00000010</dt> GETGAINSPEAKER </dl>                   | [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) PHONEHOOKSWITCHDEV \_ speaker<br/>             |
| <span id="PHONEFEATURE_GETGAINHEADSET"></span><span id="phonefeature_getgainheadset"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x00000020</dt> GETGAINHEADSET </dl>                   | [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) \_auricolare PHONEHOOKSWITCHDEV<br/>             |
| <span id="PHONEFEATURE_GETHOOKSWITCHHANDSET"></span><span id="phonefeature_gethookswitchhandset"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x00000040</dt> GETHOOKSWITCHHANDSET </dl> | [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) PHONEHOOKSWITCHDEV \_ portatile<br/> |
| <span id="PHONEFEATURE_GETHOOKSWITCHSPEAKER"></span><span id="phonefeature_gethookswitchspeaker"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x00000080</dt> GETHOOKSWITCHSPEAKER </dl> | [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) PHONEHOOKSWITCHDEV \_ portatile<br/> |
| <span id="PHONEFEATURE_GETHOOKSWITCHHEADSET"></span><span id="phonefeature_gethookswitchheadset"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x00000100</dt> GETHOOKSWITCHHEADSET </dl> | [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) PHONEHOOKSWITCHDEV \_ portatile<br/> |
| <span id="PHONEFEATURE_GETLAMP"></span><span id="phonefeature_getlamp"></span><dl> <dt>**PHONEFEATURE \_ Getlamp**</dt> <dt>0x00000200</dt> </dl>                                        | [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp)<br/>                                         |
| <span id="PHONEFEATURE_GETRING"></span><span id="phonefeature_getring"></span><dl> <dt>**PHONEFEATURE \_ Getring**</dt> <dt>0x00000400</dt> </dl>                                        | [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring)<br/>                                         |
| <span id="PHONEFEATURE_GETVOLUMEHANDSET"></span><span id="phonefeature_getvolumehandset"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x00000800</dt> GETVOLUMEHANDSET </dl>             | [**phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) PHONEHOOKSWITCHDEV \_ portatile<br/>         |
| <span id="PHONEFEATURE_GETVOLUMESPEAKER"></span><span id="phonefeature_getvolumespeaker"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x00001000</dt> GETVOLUMESPEAKER </dl>             | [**phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) PHONEHOOKSWITCHDEV \_ speaker<br/>         |
| <span id="PHONEFEATURE_GETVOLUMEHEADSET"></span><span id="phonefeature_getvolumeheadset"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x00002000</dt> GETVOLUMEHEADSET </dl>             | [**phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) \_auricolare PHONEHOOKSWITCHDEV<br/>         |
| <span id="PHONEFEATURE_SETBUTTONINFO"></span><span id="phonefeature_setbuttoninfo"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x00004000</dt> SETBUTTONINFO </dl>                      | [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo)<br/>                             |
| <span id="PHONEFEATURE_SETDATA"></span><span id="phonefeature_setdata"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x00008000</dt> SETDATA </dl>                                        | [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata)<br/>                                         |
| <span id="PHONEFEATURE_SETDISPLAY"></span><span id="phonefeature_setdisplay"></span><dl> <dt>**PHONEFEATURE \_ Visualizza**</dt> <dt>0x00010000</dt> </dl>                               | [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay)<br/>                                   |
| <span id="PHONEFEATURE_SETGAINHANDSET"></span><span id="phonefeature_setgainhandset"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x00020000</dt> SETGAINHANDSET </dl>                   | [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) PHONEHOOKSWITCHDEV \_ portatile<br/>             |
| <span id="PHONEFEATURE_SETGAINSPEAKER"></span><span id="phonefeature_setgainspeaker"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x00040000</dt> SETGAINSPEAKER </dl>                   | [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) PHONEHOOKSWITCHDEV \_ speaker<br/>             |
| <span id="PHONEFEATURE_SETGAINHEADSET"></span><span id="phonefeature_setgainheadset"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x00080000</dt> SETGAINHEADSET </dl>                   | [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) \_auricolare PHONEHOOKSWITCHDEV<br/>             |
| <span id="PHONEFEATURE_SETHOOKSWITCHHANDSET"></span><span id="phonefeature_sethookswitchhandset"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x00100000</dt> SETHOOKSWITCHHANDSET </dl> | [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) PHONEHOOKSWITCHDEV \_ portatile<br/> |
| <span id="PHONEFEATURE_SETHOOKSWITCHSPEAKER"></span><span id="phonefeature_sethookswitchspeaker"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x00200000</dt> SETHOOKSWITCHSPEAKER </dl> | [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) PHONEHOOKSWITCHDEV \_ speaker<br/> |
| <span id="PHONEFEATURE_SETHOOKSWITCHHEADSET"></span><span id="phonefeature_sethookswitchheadset"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x00400000</dt> SETHOOKSWITCHHEADSET </dl> | [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) \_auricolare PHONEHOOKSWITCHDEV<br/> |
| <span id="PHONEFEATURE_SETLAMP"></span><span id="phonefeature_setlamp"></span><dl> <dt>**PHONEFEATURE \_ Selamp**</dt> <dt>0x00800000</dt> </dl>                                        | [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp)<br/>                                         |
| <span id="PHONEFEATURE_SETRING"></span><span id="phonefeature_setring"></span><dl> <dt>**PHONEFEATURE \_ Sering**</dt> <dt>0x01000000</dt> </dl>                                        | [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring)<br/>                                         |
| <span id="PHONEFEATURE_SETVOLUMEHANDSET"></span><span id="phonefeature_setvolumehandset"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x02000000</dt> SETVOLUMEHANDSET </dl>             | [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume) PHONEHOOKSWITCHDEV \_ portatile<br/>         |
| <span id="PHONEFEATURE_SETVOLUMESPEAKER"></span><span id="phonefeature_setvolumespeaker"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x04000000</dt> SETVOLUMESPEAKER </dl>             | [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume) PHONEHOOKSWITCHDEV \_ speaker<br/>         |
| <span id="PHONEFEATURE_SETVOLUMEHEADSET"></span><span id="phonefeature_setvolumeheadset"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x08000000</dt> SETVOLUMEHEADSET </dl>             | [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume) \_auricolare PHONEHOOKSWITCHDEV<br/>         |
| <span id="PHONEFEATURE_GENERICPHONE"></span><span id="phonefeature_genericphone"></span><dl> <dt>**PHONEFEATURE \_**</dt> <dt>0x10000000</dt> GENERICPHONE </dl>                         | (pertinente solo per le applicazioni che usano TAPI 3,0 e versioni successive)<br/>                     |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




