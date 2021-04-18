---
description: Le \_ costanti del flag di bit PHONEHOOKSWITCHDEV descrivono i vari dispositivi di I/O audio ognuno con il proprio hookswitch controllabile dal computer.
ms.assetid: b3272a75-87b0-4afc-b2e2-2d65e4b49300
title: Costanti PHONEHOOKSWITCHDEV_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a6727bf8103c35402bebc048de4ed9286650be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333948"
---
# <a name="phonehookswitchdev_-constants"></a>\_Costanti PHONEHOOKSWITCHDEV

Le costanti del flag di bit **PHONEHOOKSWITCHDEV \_** descrivono i vari dispositivi di I/O audio ognuno con il proprio hookswitch controllabile dal computer.

<dl> <dt>

<span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**PHONEHOOKSWITCHDEV \_ portatile**
</dt> <dd> <dl> <dt>



Si tratta di un telefono auricolare e di un Bocchino standard.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**\_auricolare PHONEHOOKSWITCHDEV**
</dt> <dd> <dl> <dt>



Si tratta di un auricolare connesso al set di telefono.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**PHONEHOOKSWITCHDEV \_ speaker**
</dt> <dd> <dl> <dt>



Si tratta di un altoparlante e microfono incorporato. Potrebbe anche trattarsi di un altoparlante aggiuntivo collegato esternamente al set telefonico.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

Queste costanti vengono usate nella struttura dei dati [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) per indicare le funzionalità del dispositivo hookswitch di un dispositivo telefonico. La struttura [**PHONESTATUS**](/windows/desktop/api/Tapi/ns-tapi-phonestatus) segnala lo stato dei dispositivi hookswitch del telefono. La funzione [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) e [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) lo usano come parametro per selezionare il dispositivo di i/O del telefono.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




