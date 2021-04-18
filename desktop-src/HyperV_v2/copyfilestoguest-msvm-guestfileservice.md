---
description: Copia i file dall'host Hyper-V alla macchina virtuale.
ms.assetid: 76667557-13B2-4286-BC6B-E32FADE62A7A
title: 'Metodo Msvm_GuestFileService:: CopyFilesToGuest'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService.CopyFilesToGuest
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9424dee6d28e0bd9cd6ac43c15ad27cdebdb7017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314354"
---
# <a name="msvm_guestfileservicecopyfilestoguest-method"></a>\_Metodo MSVM GuestFileService:: CopyFilesToGuest

Copia i file dall'host Hyper-V alla macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
uint32 CopyFilesToGuest(
  [in]            string                  CopyFileToGuestSettings[],
  [out]           CIM_ConcreteJob     Job,
  [out, optional] Msvm_CopyFileToGuestJob ParentPools[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CopyFileToGuestSettings* \[ in\]
</dt> <dd>

Matrice di istanze della classe [**\_ CopyFileToGuestSettingData MSVM**](msvm-copyfiletoguestsettingdata.md) che rappresenta un processo di operazione del servizio file Guest.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Parametro facoltativo per il monitoraggio dello stato di avanzamento dell'operazione, che viene utilizzato se non è stato possibile eseguire in modo sincrono il metodo. Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.

> [!Note]  
> Questo parametro è stato aggiunto in Windows 10.

 

</dd> <dt>

*ParentPools* \[ out, facoltativo\]
</dt> <dd>

Matrice facoltativa di riferimenti [**MSVM \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md) utilizzati per il monitoraggio dello stato di avanzamento dell'operazione. **CopyFilesToGuest** utilizza *ParentPools* se non può essere eseguito in modo sincrono. Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.

> [!Note]  
> Questo parametro è stato rimosso in Windows 10.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce 0; in caso contrario, restituisce un valore di errore.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Parametri del metodo controllati-processo avviato** (4096)
</dt> <dt>

**Non riuscito** (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Stato sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non valido** (32773)
</dt> <dt>

Il **sistema è in uso** (32774)
</dt> <dt>

**Stato non valido per l'operazione** (32775)
</dt> <dt>

**Tipo di dati non corretto** (32776)
</dt> <dt>

**Sistema non disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\\\\\Virtualizzazione radice \\ v2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GuestFileService MSVM**](msvm-guestfileservice.md)
</dt> </dl>

 

 




