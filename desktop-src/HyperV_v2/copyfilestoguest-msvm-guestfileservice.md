---
description: Copia i file dall'host Hyper-V alla macchina virtuale.
ms.assetid: 76667557-13B2-4286-BC6B-E32FADE62A7A
title: Msvm_GuestFileService::CopyFilesToGuest
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
ms.openlocfilehash: e027d71faf8dda5769962d3c71d1fcfb5958c61c91993cf17fbf472d93aff50f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980481"
---
# <a name="msvm_guestfileservicecopyfilestoguest-method"></a>Metodo Msvm \_ GuestFileService::CopyFilesToGuest

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

*CopyFileToGuestSettings* \[ Pollici\]
</dt> <dd>

Matrice di istanze della [**classe Msvm \_ CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md) che rappresenta un processo operativo del servizio file guest.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Parametro facoltativo per il monitoraggio dello stato dell'operazione, che viene utilizzato se non è stato possibile eseguire il metodo in modo sincrono. Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.

> [!Note]  
> Questo parametro è stato aggiunto in Windows 10.

 

</dd> <dt>

*Pool padre* \[ out, facoltativo\]
</dt> <dd>

Matrice facoltativa di [**riferimenti Msvm \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md) usati per monitorare lo stato dell'operazione. **CopyFilesToGuest** usa *ParentPools* se non può essere eseguito in modo sincrono. Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.

> [!Note]  
> Questo parametro è stato rimosso in Windows 10.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce 0. In caso contrario, restituisce un valore di errore.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Parametri del metodo controllati - Processo avviato** (4096)
</dt> <dt>

**Operazione non** riuscita (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Lo stato è sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non** valido (32773)
</dt> <dt>

**Sistema in uso** (32774)
</dt> <dt>

**Stato non valido per questa operazione** (32775)
</dt> <dt>

**Tipo di dati non** corretto (32776)
</dt> <dt>

**Il sistema non è disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\\\Virtualizzazione \\ radice \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ GuestFileService**](msvm-guestfileservice.md)
</dt> </dl>

 

 




