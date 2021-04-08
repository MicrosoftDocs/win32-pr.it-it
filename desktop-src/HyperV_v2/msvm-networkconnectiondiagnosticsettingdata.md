---
description: Rappresenta le impostazioni utilizzate per testare la connettività di rete di una macchina virtuale.
ms.assetid: d719d9c9-7ca9-40a0-ada8-185b8cd44c22
title: Classe Msvm_NetworkConnectionDiagnosticSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NetworkConnectionDiagnosticSettingData
- Msvm_NetworkConnectionDiagnosticSettingData.IsSender
- Msvm_NetworkConnectionDiagnosticSettingData.SenderIP
- Msvm_NetworkConnectionDiagnosticSettingData.ReceiverIP
- Msvm_NetworkConnectionDiagnosticSettingData.ReceiverMac
- Msvm_NetworkConnectionDiagnosticSettingData.IsolationId
- Msvm_NetworkConnectionDiagnosticSettingData.SequenceNumber
- Msvm_NetworkConnectionDiagnosticSettingData.PayloadSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ec0df1957df6c925cf12ce363c89a0bdad52d3e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058242"
---
# <a name="msvm_networkconnectiondiagnosticsettingdata-class"></a>\_Classe MSVM NetworkConnectionDiagnosticSettingData

Rappresenta le impostazioni utilizzate per testare la connettività di rete di una macchina virtuale. Utilizzato dal metodo [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[AMENDMENT]
class Msvm_NetworkConnectionDiagnosticSettingData : CIM_SettingData
{
  boolean IsSender;
  string  SenderIP;
  string  ReceiverIP;
  string  ReceiverMac;
  uint32  IsolationId;
  uint32  SequenceNumber;
  uint32  PayloadSize;
};
```

## <a name="members"></a>Members

La **classe \_ NetworkConnectionDiagnosticSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ NetworkConnectionDiagnosticSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**IsolationId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

ID isolamento.

</dd> <dt>

**IsSender**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se questo metodo viene richiamato al mittente o al ricevitore.

</dd> <dt>

**PayloadSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Dimensioni del payload.

</dd> <dt>

**ReceiverIP**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indirizzo IP del destinatario.

</dd> <dt>

**ReceiverMac**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indirizzo MAC del destinatario.

</dd> <dt>

**SenderIP**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indirizzo IP del mittente.

</dd> <dt>

**SequenceNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Numero di sequenza.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1703 \[\]<br/>                                               |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

 




