---
description: Questa classe rappresenta un processo dell'operazione di esportazione del punto di riferimento del sistema virtuale.
ms.assetid: 3d8e117c-4863-441a-9264-c33f05fbc5ef
title: Classe Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob
- Msvm_VirtualSystemReferencePointExportJob.Cancellable
- Msvm_VirtualSystemReferencePointExportJob.ErrorSummaryDescription
- Msvm_VirtualSystemReferencePointExportJob.ExportDirectory
- Msvm_VirtualSystemReferencePointExportJob.VirtualMachineId
- Msvm_VirtualSystemReferencePointExportJob.ReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.BaseReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.ExportedDisks
- Msvm_VirtualSystemReferencePointExportJob.ExportedLogFilePaths
- Msvm_VirtualSystemReferencePointExportJob.ExportedConfigFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedRuntimeFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedGuestStateFilePath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04b5d8f27efae4817062917541af9bb488cec32c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530451"
---
# <a name="msvm_virtualsystemreferencepointexportjob-class"></a>\_Classe MSVM VirtualSystemReferencePointExportJob

Questa classe rappresenta un processo dell'operazione di esportazione del punto di riferimento del sistema virtuale.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  ExportDirectory;
  string  VirtualMachineId;
  string  ReferencePointId;
  string  BaseReferencePointId;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePath;
  string  ExportedRuntimeFilePath;
  string  ExportedGuestStateFilePath;
};
```

## <a name="members"></a>Members

La **classe \_ VirtualSystemReferencePointExportJob di MSVM** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ VirtualSystemReferencePointExportJob di MSVM** dispone di questi metodi.



| Metodo                                                                                     | Descrizione                                        |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------|
| [**GetError**](msvm-virtualsystemreferencepointexportjob-geterror.md)                     | Recupera l'errore.<br/>                    |
| [**GetErrorEx**](msvm-virtualsystemreferencepointexportjob-geterrorex.md)                 | Recupera informazioni aggiuntive sull'errore.<br/> |
| [**RequestStateChange**](msvm-virtualsystemreferencepointexportjob-requeststatechange.md) | Richiede una modifica dello stato.<br/>                |



 

### <a name="properties"></a>Proprietà

La **classe \_ VirtualSystemReferencePointExportJob di MSVM** dispone di queste proprietà.

<dl> <dt>

**BaseReferencePointId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

GUID del punto di riferimento utilizzato come base nell'operazione di esportazione.

</dd> <dt>

**Annullabili**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il processo può essere annullato. Il valore di questa proprietà non garantisce che una richiesta di annullamento del processo avrà esito positivo.

</dd> <dt>

**ErrorSummaryDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ processo CIM**](cim-job.md).**ErrorCode**")
</dt> </dl>

Contiene una descrizione di riepilogo dell'errore.

</dd> <dt>

**ExportDirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso di esportazione.

</dd> <dt>

**ExportedConfigFilePath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso del file di configurazione esportato.

</dd> <dt>

**ExportedDisks**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

ID istanza dei dischi virtuali per i quali sono stati esportati i file di log.

</dd> <dt>

**ExportedGuestStateFilePath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso del file di stato Guest esportato.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> <dt>

**ExportedLogFilePaths**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorsi dei file di log esportati.

</dd> <dt>

**ExportedRuntimeFilePath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso del file di stato di runtime esportato.

</dd> <dt>

**ReferencePointId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

GUID del punto di riferimento che viene esportato.

</dd> <dt>

**VirtualMachineId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

GUID della macchina virtuale per cui sono stati esportati i file di log.

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

[**\_CONCRETEJOB CIM**](cim-concretejob.md)
</dt> </dl>

 

