---
description: Fornisce informazioni sulla connettività di rete per una macchina virtuale.
ms.assetid: 59503c1b-203b-46ec-8a65-f21a746f170f
title: Classe Msvm_NetworkConnectionDiagnosticInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NetworkConnectionDiagnosticInformation
- Msvm_NetworkConnectionDiagnosticInformation.RoundTripTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 416392702e5bc06e54fe5a23b6784b87e98b7027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968466"
---
# <a name="msvm_networkconnectiondiagnosticinformation-class"></a>\_Classe MSVM NetworkConnectionDiagnosticInformation

Fornisce informazioni sulla connettività di rete per una macchina virtuale.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[AMENDMENT]
class Msvm_NetworkConnectionDiagnosticInformation
{
  uint32 RoundTripTime;
};
```

## <a name="members"></a>Members

La **classe \_ NetworkConnectionDiagnosticInformation di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ NetworkConnectionDiagnosticInformation di MSVM** dispone di queste proprietà.

<dl> <dt>

**RoundTripTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Round trip tempo per la richiesta di ping.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1703 \[\]<br/>                                               |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




