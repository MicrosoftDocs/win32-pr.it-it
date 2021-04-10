---
description: Proprietà PKEY \_ deviceinterface \_ FriendlyName.
ms.assetid: beef2153-489f-4ff5-a161-b4e2cd4ac1fa
title: PKEY_DeviceInterface_FriendlyName (Functiondiscoverykeys \_ devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7590e9254e336bf9dbfe0fdeb3349bf19c0b8c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125757"
---
# <a name="pkey_deviceinterface_friendlyname"></a>PKEY \_ deviceinterface \_ FriendlyName

La proprietà **pkey \_ deviceinterface \_ FriendlyName** contiene il nome descrittivo della scheda audio a cui è collegato il dispositivo endpoint (ad esempio, "scheda audio XYZ").

Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ LPWSTR.

Il membro **pwszVal** della struttura **PROPVARIANT** punta a una stringa di caratteri wide con terminazione null che contiene il nome descrittivo.

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

 

 




