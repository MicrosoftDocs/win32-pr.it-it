---
description: Specifica un elenco di stringhe Unicode che rappresentano le funzionalità del dispositivo richieste dalla trasformazione del sensore.
ms.assetid: 4A129FEB-E650-47C9-ABC0-9A512EE4121D
title: Attributo MF_DEVICESTREAM_REQUIRED_CAPABILITIES (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cac47d60c38e41d44ecf0776ea8bf7588559dfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129790"
---
# <a name="mf_devicestream_required_capabilities-attribute"></a>\_Attributo delle \_ \_ funzionalità obbligatorie di MF DEVICESTREAM

Specifica un elenco di stringhe Unicode che rappresentano le funzionalità del dispositivo richieste dalla trasformazione del sensore.

## <a name="data-type"></a>Tipo di dati

**WCHAR \** _

## <a name="remarks"></a>Commenti

Questo attributo è facoltativo ed è necessario solo se la trasformazione del sensore accede a una risorsa protetta. Il valore deve essere un elenco delimitato da punti e virgola di token di stringa definiti in [_ *DeviceCapability* *](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1703 \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
