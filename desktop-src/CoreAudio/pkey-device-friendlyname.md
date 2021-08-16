---
description: La proprietà PKEY Device FriendlyName contiene il nome descrittivo del dispositivo endpoint, ad esempio \_ \_ &\# 0034; Altoparlanti (scheda audio XYZ)&\# 0034;).
ms.assetid: 3ccd6a78-8bc3-4a46-8f11-7c2ae8a23c63
title: PKEY_Device_FriendlyName (Functiondiscoverykeys \_ devpkey.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148a9d7f87b32b7175aa794f769d2fa67b42c86c44e8cc7bf773d3fa6b09d106
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406427"
---
# <a name="pkey_device_friendlyname"></a>PKEY \_ Device \_ FriendlyName

La **proprietà PKEY \_ Device \_ FriendlyName** contiene il nome descrittivo del dispositivo endpoint, ad esempio "Speakers (XYZ Audio Adapter)".

Il **membro vt** della **struttura PROPVARIANT** è impostato su VT \_ LPWSTR.

Il **membro pwszVal** della struttura **PROPVARIANT** punta a una stringa di caratteri wide con terminazione Null che contiene il nome descrittivo del dispositivo endpoint.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Functiondiscoverykeys \_ devpkey.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà audio di base](core-audio-properties.md)
</dt> <dt>

[Proprietà dispositivo](device-properties.md)
</dt> </dl>

 

 




