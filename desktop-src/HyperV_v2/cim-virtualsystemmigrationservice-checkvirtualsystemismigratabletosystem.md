---
description: 'Altre informazioni su: Metodo CheckVirtualSystemIsMigratableToSystem della classe CIM_VirtualSystemMigrationService'
ms.assetid: d3f7c926-804f-4c7c-8964-a8e464155417
title: Metodo CheckVirtualSystemIsMigratableToSystem della CIM_VirtualSystemMigrationService classe
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
ms.openlocfilehash: 4f2f543cff29464d76f1b2729efa9bca1a0c677d3cd7173975f59d2007aafb7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682712"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a>Metodo CheckVirtualSystemIsMigratableToSystem della classe CIM \_ VirtualSystemMigrationService

Metodo per eseguire un controllo preliminare per determinare se è probabile che la migrazione di un sistema virtuale a un sistema di destinazione sia stata completata correttamente. Questo metodo non garantisce che una migrazione successiva avrà sempre esito positivo, a causa della disponibilità dinamica delle risorse. Descrizione del codice restituito:

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

*ComputerSystem* \[ Pollici\]
</dt> <dd>

[**CIM \_ Istanza ComputerSystem**](cim-computersystem.md) che fa riferimento al sistema di computer virtuale di origine di cui eseguire la migrazione.

</dd> <dt>

*DestinationSystem* \[ Pollici\]
</dt> <dd>

[**CIM \_ Istanza**](cim-system.md) di sistema che fa riferimento al sistema di destinazione in cui eseguire la migrazione del sistema virtuale.

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

Matrice di stringhe contenente ognuna un'istanza incorporata della classe [**\_ CIM ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che rappresenta le nuove proprietà applicabili alle risorse virtuali nell'ambito del sistema virtuale dopo la migrazione.

</dd> <dt>

*IsMigratable* \[ Cambio\]
</dt> <dd>

Risultato del controllo della migrazione che indica se è possibile eseguire correttamente la migrazione del sistema virtuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore 0 se l'operazione ha esito positivo. In caso contrario, restituisce un errore.



| Codice/valore restituito                                                                                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Completata senza errori**</dt> <dt>0</dt> </dl>    | Controllo eseguito; risultato restituito tramite il valore \[ del parametro Out \] *IsMigratable.*<br/>                                                                                                                                                                                                                                                                          |
| <dl> <dt>**Non supportato**</dt> <dt>1</dt> </dl>              | Metodo non supportato dall'implementazione. Nessun risultato segnalato tramite il valore \[ del parametro Out \] *IsMigratable.*<br/>                                                                                                                                                                                                                                                |
| <dl> <dt>**Errore**</dt> <dt>2</dt> </dl>                     | Controllo non riuscito per motivi non specificato. Nessun risultato segnalato tramite il valore \[ del parametro Out \] *IsMigratable.*<br/>                                                                                                                                                                                                                                                  |
| <dl> <dt>**Timeout**</dt> <dt>3</dt> </dl>                    | Timeout del controllo. Nessun risultato segnalato tramite il valore \[ del parametro Out \] *IsMigratable.*<br/>                                                                                                                                                                                                                                                                       |
| <dl> <dt>**Parametro 4**</dt> <dt>non valido</dt> </dl>          | Uno o più parametri non sono formalmente validi. Ad esempio, il valore del *parametro DestinationSystem* non include un percorso di oggetto valido. Nessun risultato segnalato tramite il valore \[ del parametro Out \] *IsMigratable.*<br/>                                                                                                                                        |
| <dl> <dt>**Stato non valido**</dt> <dt>5</dt> </dl>              | Il sistema virtuale di origine, il sistema host di origine o il sistema host di destinazione sono in uno stato che consente l'avvio della migrazione del sistema virtuale richiesta. Potrebbe trattarsi di una condizione temporanea. Nessun risultato segnalato tramite il valore \[ del parametro Out \] *IsMigratable.*<br/>                                                                                    |
| <dl> <dt>**Parametri incompatibili**</dt> <dt>6</dt> </dl>    | Uno o più parametri di input non sono compatibili come set o rispetto all'host di destinazione. Ad esempio, il valore del *parametro NewSettingData* contiene proprietà non supportate dal sistema host di destinazione identificato dal valore del *parametro DestinationSystem.* Nessun risultato segnalato tramite il valore \[ del parametro Out \] *IsMigratable.*<br/> |
| <dl> <dt>**DmTF Reserved**</dt> <dt>.</dt> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**Metodo riservato**</dt> <dt>4097..32767</dt> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**Specifico del**</dt> <dt>fornitore 32768..65535</dt> </dl> |                                                                                                                                                                                                                                                                                                                                                                                 |



 

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

 

 




