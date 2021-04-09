---
description: La \_ Proprietà Device \_ FriendlyName di pkey contiene il nome descrittivo del dispositivo endpoint (ad esempio, &\# 0034; Altoparlanti (scheda audio XYZ) &\# 0034;).
ms.assetid: 3ccd6a78-8bc3-4a46-8f11-7c2ae8a23c63
title: PKEY_Device_FriendlyName (Functiondiscoverykeys \_ devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fab8b8f30e04ae66356fb0910e3767d74b7b697a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877181"
---
# <a name="pkey_device_friendlyname"></a>PKEY \_ Device \_ FriendlyName

La **proprietà \_ Device \_ FriendlyName di pkey** contiene il nome descrittivo del dispositivo endpoint (ad esempio, "Speakers (scheda audio XYZ)").

Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ LPWSTR.

Il membro **pwszVal** della struttura **PROPVARIANT** punta a una stringa di caratteri wide con terminazione null che contiene il nome descrittivo del dispositivo endpoint.

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

 

 




