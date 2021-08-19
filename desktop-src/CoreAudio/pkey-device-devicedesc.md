---
description: La proprietà PKEY DeviceDesc contiene la descrizione del dispositivo endpoint( ad \_ \_ esempio, &\# 0034; Altoparlanti&\# 0034;).
ms.assetid: 23715497-a74d-4dab-aade-c7779fe80aa6
title: PKEY_Device_DeviceDesc (Functiondiscoverykeys \_ devpkey.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71c5772029f6c99a86c330f05e3cae3b343e3ee25f39eae4c8d5900e7bf947c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077465"
---
# <a name="pkey_device_devicedesc"></a>PKEY \_ Device \_ DeviceDesc

La **proprietà PKEY \_ \_ DeviceDesc** contiene la descrizione del dispositivo endpoint, ad esempio "Speakers".

Il **membro vt** della **struttura PROPVARIANT** è impostato su VT \_ LPWSTR.

Il **membro pwszVal** della **struttura PROPVARIANT** punta a una stringa di caratteri wide con terminazione Null che contiene la descrizione del dispositivo.

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

 

 




