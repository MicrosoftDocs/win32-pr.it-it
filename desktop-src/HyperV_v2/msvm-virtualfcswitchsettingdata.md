---
description: Rappresenta la configurazione di un'opzione di Fibre Channel virtuale.
ms.assetid: da2918a9-6e7f-4fee-9c13-7e75bbc6821f
title: Classe Msvm_VirtualFcSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualFcSwitchSettingData
- Msvm_VirtualFcSwitchSettingData.InstanceID
- Msvm_VirtualFcSwitchSettingData.Caption
- Msvm_VirtualFcSwitchSettingData.Description
- Msvm_VirtualFcSwitchSettingData.ElementName
- Msvm_VirtualFcSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualFcSwitchSettingData.VirtualSystemType
- Msvm_VirtualFcSwitchSettingData.Notes
- Msvm_VirtualFcSwitchSettingData.CreationTime
- Msvm_VirtualFcSwitchSettingData.ConfigurationID
- Msvm_VirtualFcSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualFcSwitchSettingData.ConfigurationFile
- Msvm_VirtualFcSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualFcSwitchSettingData.SuspendDataRoot
- Msvm_VirtualFcSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualFcSwitchSettingData.LogDataRoot
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualFcSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualFcSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualFcSwitchSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 67b6008ba1f5ba9849d6fcd9127c1a55c1da8290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525218"
---
# <a name="msvm_virtualfcswitchsettingdata-class"></a>\_Classe MSVM VirtualFcSwitchSettingData

Rappresenta la configurazione di un'opzione di Fibre Channel virtuale.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualFcSwitchSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
};
```

## <a name="members"></a>Members

La **classe \_ VirtualFcSwitchSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ VirtualFcSwitchSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Azione da eseguire per la macchina virtuale quando il software eseguito dalla macchina virtuale ha esito negativo. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Azione da eseguire per la macchina virtuale quando l'host viene arrestato. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Azione da eseguire per la macchina virtuale all'avvio dell'host. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tempo di ritardo prima che la macchina virtuale venga avviata automaticamente. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero che indica la sequenza relativa di attivazione della macchina virtuale all'avvio del sistema host. Un numero inferiore indica l'attivazione precedente. Se una o più configurazioni mostrano lo stesso valore, la sequenza è dipendente dall'implementazione. Il valore 0 indica che la sequenza è dipendente dall'implementazione. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso di una directory in cui vengono archiviate le informazioni sulla configurazione della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Il percorso relativo e il nome file di un file in cui vengono archiviate le informazioni sulla configurazione della macchina virtuale. Questo percorso è relativo alla proprietà **ConfigurationDataRoot** . Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore univoco della configurazione. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora in cui sono state create le impostazioni. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso di una directory in cui vengono archiviate le informazioni di log per la macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.

</dd> <dt>

**Note**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Note fornite dall'utente correlate alla macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso completo di un file in cui sono archiviate le informazioni relative al ripristino per la macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso di una directory in cui vengono archiviate le informazioni sugli snapshot della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso di una directory in cui vengono archiviate informazioni sulle informazioni relative alla sospensione della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso di una directory in cui vengono archiviati i file di scambio per la macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.

</dd> <dt>

**VirtualSystemIdentifier**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome dell'oggetto [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) a cui appartengono i dati dell'impostazione. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il tipo di macchina virtuale rappresentata dai dati di impostazione. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

