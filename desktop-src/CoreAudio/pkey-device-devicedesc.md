---
description: La \_ Proprietà DeviceDesc del dispositivo pkey \_ contiene la descrizione del dispositivo dell'endpoint, ad esempio &\# 0034; Speakers&\# 0034;).
ms.assetid: 23715497-a74d-4dab-aade-c7779fe80aa6
title: PKEY_Device_DeviceDesc (Functiondiscoverykeys \_ devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb68f874979e660fec0cd563db9bcaceb7d5b74
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877189"
---
# <a name="pkey_device_devicedesc"></a>\_DeviceDesc del dispositivo pkey \_

La **proprietà \_ \_ DeviceDesc del dispositivo pkey** contiene la descrizione del dispositivo dell'endpoint (ad esempio, "Speakers").

Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ LPWSTR.

Il membro **pwszVal** della struttura **PROPVARIANT** punta a una stringa di caratteri wide con terminazione null che contiene la descrizione del dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Functiondiscoverykeys \_ devpkey. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà audio principali](core-audio-properties.md)
</dt> <dt>

[Proprietà dispositivo](device-properties.md)
</dt> </dl>

 

 




