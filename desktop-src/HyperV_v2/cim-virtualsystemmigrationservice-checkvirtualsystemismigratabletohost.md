---
description: Metodo per eseguire un controllo preliminare per determinare se è probabile che la migrazione di un sistema virtuale a un host di destinazione specificato da un nome di rete o da un indirizzo IP sia stata completata correttamente.
ms.assetid: bfcd4063-30fe-4d18-9df9-7b84a680814c
title: Metodo CheckVirtualSystemIsMigratableToHost della CIM_VirtualSystemMigrationService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 061cf41d2c509a1fb670f2fc8fb5d56c98d54e3619bfddae59857c2cf9cc51b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980521"
---
# <a name="checkvirtualsystemismigratabletohost-method-of-the-cim_virtualsystemmigrationservice-class"></a>Metodo CheckVirtualSystemIsMigratableToHost della classe \_ CIM VirtualSystemMigrationService

Metodo per eseguire un controllo preliminare per determinare se è probabile che la migrazione di un sistema virtuale a un host di destinazione specificato da un nome di rete o da un indirizzo IP sia stata completata correttamente. Questo metodo non garantisce che una migrazione successiva avrà sempre esito positivo, a causa della disponibilità dinamica delle risorse.

Descrizione del codice restituito:

Nota: questo metodo è inteso come soluzione di transizione solo fino a quando non è disponibile la modellazione del supporto del cluster.

## <a name="syntax"></a>Sintassi


```mof
uint32 CheckVirtualSystemIsMigratableToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
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

Riferimento [**CiM \_ ComputerSystem**](cim-computersystem.md) al sistema di computer virtuale di origine di cui eseguire la migrazione.

</dd> <dt>

*Host di destinazione* \[ Pollici\]
</dt> <dd>

Sistema host di destinazione per la migrazione.

I formati accettabili per questo parametro vengono trasmessi tramite i valori degli elementi della proprietà di matrice **DestinationHostFormatsSupported** nell'istanza di \[ \] [**CIM \_ VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md) associata tramite l'associazione [**\_ ElementCapabilities CIM.**](cim-elementcapabilities.md)

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



| Codice/valore restituito                                                                                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Completata senza errori**</dt> <dt>0</dt> </dl>    | Controllo eseguito; risultato restituito tramite il valore \[ del parametro Out \] *IsMigratable.*<br/>                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**Non supportato**</dt> <dt>1</dt> </dl>              | Metodo non supportato dall'implementazione. Nessun risultato segnalato tramite il valore \[ del parametro Out \] *IsMigratable.*<br/>                                                                                                                                                                                                                                                       |
| <dl> <dt>**Errore**</dt> <dt>2</dt> </dl>                     | Controllo non riuscito per motivi non specificato. Nessun risultato segnalato tramite il valore \[ del parametro Out \] *IsMigratable.*<br/>                                                                                                                                                                                                                                                         |
| <dl> <dt>**Timeout**</dt> <dt>3</dt> </dl>                    | Timeout del controllo. Nessun risultato segnalato tramite il valore \[ del parametro Out \] *IsMigratable.*<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**Parametro 4**</dt> <dt>non valido</dt> </dl>          | Uno o più parametri non sono formalmente validi. Ad esempio, il valore del *parametro DestinationHost* potrebbe essere stato specificato in un formato non supportato. Nessun risultato segnalato tramite il valore \[ del parametro Out \] *IsMigratable.*<br/>                                                                                                                                    |
| <dl> <dt>**Stato non valido**</dt> <dt>5</dt> </dl>              | Il sistema virtuale di origine, il sistema host di origine o il sistema host di destinazione sono in uno stato che consente l'avvio della migrazione del sistema virtuale richiesta. Potrebbe trattarsi di una condizione temporanea. Nessun risultato segnalato tramite il valore \[ del parametro Out \] *IsMigratable.*<br/>                                                                                           |
| <dl> <dt>**Parametri incompatibili**</dt> <dt>6</dt> </dl>    | Uno o più parametri di input non sono compatibili come set o rispetto all'host di destinazione. Ad esempio, il valore del *parametro MigrationNewSettingData* contiene proprietà non supportate dal sistema host di destinazione identificato dal valore *del parametro DestinationHost.* Nessun risultato segnalato tramite il valore \[ del parametro Out \] *IsMigratable.*<br/> |
| <dl> <dt>**DmTF Reserved**</dt> <dt>.</dt> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**Metodo riservato**</dt> <dt>4097..32767</dt> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**Specifico del**</dt> <dt>fornitore 32768..65535</dt> </dl> |                                                                                                                                                                                                                                                                                                                                                                                        |



 

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

 

 




