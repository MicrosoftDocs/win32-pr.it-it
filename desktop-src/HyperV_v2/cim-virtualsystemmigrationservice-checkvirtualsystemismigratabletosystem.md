---
description: 'Altre informazioni su: Metodo CheckVirtualSystemIsMigratableToSystem della classe CIM_VirtualSystemMigrationService'
ms.assetid: d3f7c926-804f-4c7c-8964-a8e464155417
title: Metodo CheckVirtualSystemIsMigratableToSystem della classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: be85c51cb507fea3cea14f1706ffa8f67af06c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311139"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a>Metodo CheckVirtualSystemIsMigratableToSystem della classe CIM \_ VirtualSystemMigrationService

Metodo per eseguire un controllo preliminare per determinare se è probabile che un sistema virtuale venga migrato correttamente a un sistema di destinazione. Questo metodo non garantisce che una migrazione successiva avrà sempre esito positivo, a causa della disponibilità dinamica delle risorse. Descrizione del codice restituito:

## <a name="syntax"></a>Sintassi


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] boolean                IsMigratable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ComputerSystem* \[ in\]
</dt> <dd>

[**CIM \_**](cim-computersystem.md) Istanza di ComputerSystem che fa riferimento al sistema del computer virtuale di origine da migrare.

</dd> <dt>

*DestinationSystem* \[ in\]
</dt> <dd>

[**CIM \_**](cim-system.md) Istanza di sistema che fa riferimento al sistema di destinazione su cui eseguire la migrazione del sistema virtuale.

</dd> <dt>

*MigrationSettingData* \[ in\]
</dt> <dd>

Stringa contenente un'istanza incorporata della classe [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) che rappresenta le impostazioni di migrazione applicabili all'operazione di migrazione.

</dd> <dt>

*NewSystemSettingData* \[ in\]
</dt> <dd>

Stringa contenente un'istanza incorporata della classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) che rappresenta le nuove proprietà applicabili al sistema virtuale dopo la migrazione.

</dd> <dt>

*NewResourceSettingData* \[ in\]
</dt> <dd>

Matrice di stringhe, ognuna delle quali contiene un'istanza incorporata della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che rappresenta le nuove proprietà applicabili alle risorse virtuali nell'ambito del sistema virtuale dopo la migrazione.

</dd> <dt>

*IsMigratable* \[ out\]
</dt> <dd>

Risultato del controllo della migrazione che indica se è possibile eseguire la migrazione del sistema virtuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.



| Codice/valore restituito                                                                                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Completato senza errori**</dt> <dt>0</dt> </dl>    | Controllo eseguito; risultato restituito tramite il valore del \[ parametro out \] *IsMigratable* .<br/>                                                                                                                                                                                                                                                                          |
| <dl> <dt>**Non supportato**</dt> <dt>1</dt> </dl>              | Metodo non supportato dall'implementazione di. Nessun risultato segnalato tramite il valore del \[ parametro out \] *IsMigratable* .<br/>                                                                                                                                                                                                                                                |
| <dl> <dt>**Operazione non riuscita**</dt> <dt>2</dt> </dl>                     | Controllo non riuscito per motivi non specificati. Nessun risultato segnalato tramite il valore del \[ parametro out \] *IsMigratable* .<br/>                                                                                                                                                                                                                                                  |
| <dl> <dt>**Timeout**</dt> <dt>3</dt> </dl>                    | Timeout del controllo. Nessun risultato segnalato tramite il valore del \[ parametro out \] *IsMigratable* .<br/>                                                                                                                                                                                                                                                                       |
| <dl> <dt>**Parametro 4 non valido**</dt> <dt></dt> </dl>          | Uno o più parametri non sono formalmente validi. Il valore del parametro *DestinationSystem* , ad esempio, non è costituito da un percorso di oggetto valido. Nessun risultato segnalato tramite il valore del \[ parametro out \] *IsMigratable* .<br/>                                                                                                                                        |
| <dl> <dt>**Stato non valido**</dt> <dt>5</dt> </dl>              | Il sistema virtuale di origine, il sistema host di origine o il sistema host di destinazione si trovano in uno stato che consente l'avvio della migrazione del sistema virtuale richiesta. potrebbe trattarsi di una condizione temporanea. Nessun risultato segnalato tramite il valore del \[ parametro out \] *IsMigratable* .<br/>                                                                                    |
| <dl> <dt>**Parametri incompatibili**</dt> <dt>6</dt> </dl>    | Uno o più parametri di input sono incompatibili come set o per quanto riguarda l'host di destinazione. Il valore del parametro *NewSettingData* , ad esempio, contiene proprietà che non sono supportate dal sistema host di destinazione identificato dal valore del parametro *DestinationSystem* . Nessun risultato segnalato tramite il valore del \[ parametro out \] *IsMigratable* .<br/> |
| <dl> <dt>**DMTF riservato**</dt> <dt>..</dt> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**Metodo riservato**</dt> <dt>4097.. 32767</dt> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> 32768 <dt>**specifici del fornitore**</dt> <dt>.. 65535</dt> </dl> |                                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_VIRTUALSYSTEMMIGRATIONSERVICE CIM**](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




