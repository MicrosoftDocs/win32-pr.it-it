---
description: Metodo per spostare, migrare o rilocare un sistema virtuale in un sistema di destinazione.
ms.assetid: 210d31f1-093f-4fd5-afd7-5f028b4cb343
title: Metodo MigrateVirtualSystemToSystem della classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1459d80785725914cbaa5dda5b81e8d2fabad5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881218"
---
# <a name="migratevirtualsystemtosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a>Metodo MigrateVirtualSystemToSystem della classe CIM \_ VirtualSystemMigrationService

Metodo per spostare, migrare o rilocare un sistema virtuale in un sistema di destinazione.

Descrizione del codice restituito:

## <a name="syntax"></a>Sintassi


```mof
uint32 MigrateVirtualSystemToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ComputerSystem REF NewComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ComputerSystem* \[ in\]
</dt> <dd>

Sistema del computer virtuale di origine da migrare.

</dd> <dt>

*DestinationSystem* \[ in\]
</dt> <dd>

Messere di sistema host di destinazione migrare il sistema virtuale.

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

*NewComputerSystem* \[ out\]
</dt> <dd>

Riferimento a un'istanza della classe [**CIM \_ ComputerSystem**](cim-computersystem.md) che rappresenta il sistema di computer virtuale dopo la migrazione.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Se l'operazione è a esecuzione prolungata, è possibile che venga restituito facoltativamente un [**\_ ConcreteJob CIM**](cim-concretejob.md) che rappresenta il processo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.



| Codice/valore restituito                                                                                                                                                                | Descrizione                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Completato senza errori**</dt> <dt>0</dt> </dl>                    | Migrazione del sistema virtuale completata.<br/>                                                                                                                                                                                                                                                                    |
| <dl> <dt>**Non supportato**</dt> <dt>1</dt> </dl>                              | Metodo non supportato dall'implementazione di.<br/>                                                                                                                                                                                                                                                         |
| <dl> <dt>**Operazione non riuscita**</dt> <dt>2</dt> </dl>                                     | La migrazione del sistema virtuale non è riuscita per motivi non specificati.<br/>                                                                                                                                                                                                                                        |
| <dl> <dt>**Timeout**</dt> <dt>3</dt> </dl>                                    | Timeout della migrazione del sistema virtuale; lo stato del sistema virtuale è sconosciuto.<br/>                                                                                                                                                                                                                         |
| <dl> <dt>**Parametro 4 non valido**</dt> <dt></dt> </dl>                          | Uno o più parametri non sono formalmente validi, ad esempio, il valore del parametro di sistema di destinazione non contiene un percorso di oggetto valido.<br/>                                                                                                                                                    |
| <dl> <dt>**Stato non valido**</dt> <dt>5</dt> </dl>                              | Il sistema virtuale di origine, il sistema host di origine o il sistema host di destinazione si trovano in uno stato che consente l'avvio della migrazione del sistema virtuale richiesta. potrebbe trattarsi di una condizione temporanea.<br/>                                                                                             |
| <dl> <dt>**Parametri incompatibili**</dt> <dt>6</dt> </dl>                    | Uno o più parametri di input sono incompatibili come set o per quanto riguarda l'host di destinazione. Il valore del parametro *MigrationNewSettingData* , ad esempio, contiene proprietà che non sono supportate dal sistema host di destinazione identificato dal valore del parametro *DestinationSystem* .<br/> |
| <dl> <dt>**DMTF riservato**</dt> <dt>..</dt> </dl>                             |                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**Parametri del metodo controllati-processo avviato**</dt> <dt>4096</dt> </dl> |                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**Metodo riservato**</dt> <dt>4097.. 32767</dt> </dl>                  |                                                                                                                                                                                                                                                                                                            |
| <dl> 32768 <dt>**specifici del fornitore**</dt> <dt>.. 65535</dt> </dl>                 |                                                                                                                                                                                                                                                                                                            |



 

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

 

 




