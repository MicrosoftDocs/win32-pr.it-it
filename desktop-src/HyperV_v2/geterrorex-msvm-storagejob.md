---
description: Quando il processo è in esecuzione o è terminato senza errori, questo metodo non restituisce alcuna istanza di Msvm \_ Error.
ms.assetid: 119E7EFD-78C9-46F1-8A53-C51A7A34B32E
title: Metodo GetErrorEx della classe Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 383b1bdd5fdff36b1f29c7d80a5ecee245aaeeba5db190965370754310ffc14d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532401"
---
# <a name="geterrorex-method-of-the-msvm_storagejob-class"></a>Metodo GetErrorEx della classe Msvm \_ StorageJob

Quando il processo è in esecuzione o è terminato senza errori, questo metodo non restituisce alcuna [**istanza di Msvm \_ Error.**](msvm-error.md) Tuttavia, se il processo ha avuto esito negativo a causa di un problema interno o perché il processo è stato terminato da un client, vengono restituite una o più **istanze di Msvm \_ Error.**

## <a name="syntax"></a>Sintassi


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Errori* \[ Cambio\]
</dt> <dd>

Tipo: **\[ \] stringa**

Se lo stato operativo del processo non è "OK", questo metodo restituisce una matrice di [**istanze di Msvm \_ Error.**](msvm-error.md) In caso contrario, se il processo è "OK", **viene restituito Null.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
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

## <a name="remarks"></a>Commenti

L'accesso alla [**classe Msvm \_ StorageJob**](msvm-storagejob.md) potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Processo di \_ archiviazione Msvm**](msvm-storagejob.md)
</dt> </dl>

 

