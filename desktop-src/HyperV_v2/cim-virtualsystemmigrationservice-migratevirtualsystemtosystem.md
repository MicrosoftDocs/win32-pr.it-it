---
description: Metodo per spostare, eseguire la migrazione o riposizionare un sistema virtuale in un sistema di destinazione.
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
ms.openlocfilehash: 7b60e691f2f873a26a52f59def32b35005d45914f7fe379af14b5260b02a0c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393419"
---
# <a name="migratevirtualsystemtosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a>Metodo MigrateVirtualSystemToSystem della classe CIM \_ VirtualSystemMigrationService

Metodo per spostare, eseguire la migrazione o riposizionare un sistema virtuale in un sistema di destinazione.

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

*ComputerSystem* \[ Pollici\]
</dt> <dd>

Sistema di computer virtuale di origine di cui eseguire la migrazione.

</dd> <dt>

*DestinationSystem* \[ Pollici\]
</dt> <dd>

Sistema host di destinazione in cui eseguire la migrazione del sistema virtuale.

</dd> <dt>

*MigrationSettingData* \[ Pollici\]
</dt> <dd>

Stringa contenente un'istanza incorporata della [**classe CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) che rappresenta le impostazioni di migrazione applicabili all'operazione di migrazione.

</dd> <dt>

*NewSystemSettingData* \[ Pollici\]
</dt> <dd>

Stringa contenente un'istanza incorporata della [**classe CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) che rappresenta le nuove proprietà applicabili al sistema virtuale dopo la migrazione.

</dd> <dt>

*NewResourceSettingData* \[ Pollici\]
</dt> <dd>

Matrice di stringhe ognuna delle quali contiene un'istanza incorporata della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che rappresenta le nuove proprietà applicabili alle risorse virtuali nell'ambito del sistema virtuale dopo la migrazione.

</dd> <dt>

*NewComputerSystem* \[ Cambio\]
</dt> <dd>

Riferimento a un'istanza della [**classe CIM \_ ComputerSystem**](cim-computersystem.md) che rappresenta il sistema di computer virtuali dopo la migrazione.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione è a esecuzione lunga, facoltativamente può essere restituito [**un processo CIM \_ ConcreteJob**](cim-concretejob.md) che rappresenta il processo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore 0 in esito positivo. In caso contrario, restituisce un errore.



| Codice/valore restituito                                                                                                                                                                | Descrizione                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Completata senza errori**</dt> <dt>0</dt> </dl>                    | È stata eseguita la migrazione del sistema virtuale.<br/>                                                                                                                                                                                                                                                                    |
| <dl> <dt>**Non supportato**</dt> <dt>1</dt> </dl>                              | Metodo non supportato dall'implementazione.<br/>                                                                                                                                                                                                                                                         |
| <dl> <dt>**Operazione**</dt> <dt>non riuscita 2</dt> </dl>                                     | La migrazione del sistema virtuale non è riuscita per motivi non specificato.<br/>                                                                                                                                                                                                                                        |
| <dl> <dt>**Timeout**</dt> <dt>3</dt> </dl>                                    | Timeout della migrazione del sistema virtuale. Lo stato del sistema virtuale è sconosciuto.<br/>                                                                                                                                                                                                                         |
| <dl> <dt>**Parametro 4**</dt> <dt>non valido</dt> </dl>                          | Uno o più parametri non sono formalmente validi. Ad esempio, il valore del parametro Destination System non contiene un percorso di oggetto valido.<br/>                                                                                                                                                    |
| <dl> <dt>**Stato non valido**</dt> <dt>5</dt> </dl>                              | Il sistema virtuale di origine, il sistema host di origine o il sistema host di destinazione sono in uno stato che consente l'avvio della migrazione del sistema virtuale richiesta. potrebbe trattarsi di una condizione temporanea.<br/>                                                                                             |
| <dl> <dt>**Parametri incompatibili**</dt> <dt>6</dt> </dl>                    | Uno o più parametri di input non sono compatibili come set o rispetto all'host di destinazione. Ad esempio, il valore del *parametro MigrationNewSettingData* contiene proprietà non supportate dal sistema host di destinazione identificato dal valore *del parametro DestinationSystem.*<br/> |
| <dl> <dt>**DMTF riservato.**</dt> <dt></dt> </dl>                             |                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**Parametri del metodo controllati - Processo avviato**</dt> <dt>4096</dt> </dl> |                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**Metodo riservato**</dt> <dt>4097..32767</dt> </dl>                  |                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**Specifico del**</dt> <dt>fornitore 32768..65535</dt> </dl>                 |                                                                                                                                                                                                                                                                                                            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




