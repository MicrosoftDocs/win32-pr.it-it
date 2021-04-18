---
description: Rappresenta un processo di operazione del servizio file Guest.
ms.assetid: 3750707e-e8c8-4188-aed8-1a394d142140
title: Classe Msvm_CopyFileToGuestJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob
- Msvm_CopyFileToGuestJob.StartService
- Msvm_CopyFileToGuestJob.StopService
- Msvm_CopyFileToGuestJob.Caption
- Msvm_CopyFileToGuestJob.CreationClassName
- Msvm_CopyFileToGuestJob.Description
- Msvm_CopyFileToGuestJob.InstallDate
- Msvm_CopyFileToGuestJob.Name
- Msvm_CopyFileToGuestJob.Started
- Msvm_CopyFileToGuestJob.StartMode
- Msvm_CopyFileToGuestJob.Status
- Msvm_CopyFileToGuestJob.SystemCreationClassName
- Msvm_CopyFileToGuestJob.SystemName
- Msvm_CopyFileToGuestJob.CopyFileToGuestSettingData
- Msvm_CopyFileToGuestJob.Cancellable
- Msvm_CopyFileToGuestJob.ErrorSummaryDescription
- Msvm_CopyFileToGuestJob.VirtualSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57e27b4ba610eea4559f3b045b2d823661cf4cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314334"
---
# <a name="msvm_copyfiletoguestjob-class"></a>\_Classe MSVM CopyFileToGuestJob

Rappresenta un processo di operazione del servizio file Guest. Questa classe deriva da [**MSVM \_ GuestFileService**](msvm-guestfileservice.md).

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CopyFileToGuestJob : CIM_ConcreteJob
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  string   CopyFileToGuestSettingData[];
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  string   VirtualSystemName;
};
```

## <a name="members"></a>Members

La **classe \_ CopyFileToGuestJob di MSVM** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ CopyFileToGuestJob di MSVM** dispone di questi metodi.



| Metodo                                                                   | Descrizione                                                           |
|:-------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**CopyFilesToGuest**](copyfilestoguest-msvm-guestfileservice.md)       | Copia i file dall'host Hyper-V alla macchina virtuale.<br/> |
| [**GetError**](geterror-msvm-copyfiletoguestjob.md)                     | Recupera l'oggetto errore per il processo.<br/>                    |
| [**GetErrorEx**](geterrorex-msvm-copyfiletoguestjob.md)                 | Recupera gli oggetti Error per il processo.<br/>                   |
| [**RequestStateChange**](requeststatechange-msvm-copyfiletoguestjob.md) | Modifica lo stato del processo.<br/>                              |
| **StartService**                                                         | Questo metodo non è supportato.<br/>                              |
| **StopService**                                                          | Questo metodo non è supportato.<br/>                              |



 

### <a name="properties"></a>Proprietà

La **classe \_ CopyFileToGuestJob di MSVM** dispone di queste proprietà.

<dl> <dt>

**Annullabili**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il processo può essere annullato. Il valore di questa proprietà non garantisce che una richiesta di annullamento del processo avrà esito positivo. Se **true**, il processo può essere annullato. in caso contrario, **false**.

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione testuale dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**CopyFileToGuestSettingData**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Impostazione dei dati utilizzati per la copia di un file.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di. Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ErrorSummaryDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ processo CIM**](cim-job.md).**ErrorCode**")
</dt> </dl>

Descrizione di riepilogo dell'errore, se presente. Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di installazione dell'oggetto. Questa proprietà non richiede un valore per indicare che l'oggetto è installato. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore univoco per il servizio che fornisce anche un'indicazione della funzionalità gestita. Per ulteriori informazioni sulla funzionalità, vedere la proprietà **Description** dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**Avviato**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, il servizio è stato avviato.

</dd> <dt>

**Modalità avvio**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il servizio viene avviato automaticamente, ad esempio da un sistema operativo, o se è stato avviato solo su richiesta.

Sono inclusi i valori seguenti:

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

**Automatica**
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

**Manuale**
</dt> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato corrente dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

Sono inclusi i valori seguenti:

<dl><span id="OK"></span><span id="ok"></span><dt>

**OK**
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

**Errore**
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

**Degradato**
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

**Sconosciuto**
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

**"Errore di predazione"**
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

**Avvio**
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

**Arresto**
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

**Servizio**
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

**Sottolineato**
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

**"Non ripristino"**
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

**"Nessun contatto"**
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

**"Lost comm"**
</dt> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe di creazione del sistema di ambito.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del sistema che ospita il servizio.

</dd> <dt>

**VirtualSystemName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

GUID del sistema virtuale interessato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_CONCRETEJOB CIM**](cim-concretejob.md)
</dt> <dt>

[**\_GuestFileService MSVM**](msvm-guestfileservice.md)
</dt> <dt>

[**\_GuestService MSVM**](msvm-guestservice.md)
</dt> </dl>

 

