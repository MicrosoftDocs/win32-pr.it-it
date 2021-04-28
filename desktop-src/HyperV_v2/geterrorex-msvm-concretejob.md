---
description: 'Metodo GetErrorEx della Msvm_ConcreteJob: recupera gli oggetti errore per il processo, se presenti.'
ms.assetid: B4B4F60C-9221-4125-8D42-F0F1D32C3E79
title: Metodo GetErrorEx della classe Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 67abbd06fdaae9c23cca53f5516586f45216f20d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119349"
---
# <a name="geterrorex-method-of-the-msvm_concretejob-class"></a>Metodo GetErrorEx della classe Msvm \_ ConcreteJob

Recupera gli oggetti errore per il processo, se presenti. Quando il processo è in esecuzione o è terminato senza errori, questo metodo non restituisce alcuna [**istanza di Msvm \_ Error.**](msvm-error.md) Tuttavia, se il processo ha avuto esito negativo a causa di un problema interno o perché il processo è stato terminato da un client, vengono restituite una o più **istanze di Msvm \_ Error.**

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

Se lo stato operativo del processo non è 2 (OK), questo metodo restituisce una o più istanze incorporate della classe [**Msvm \_ Error,**](msvm-error.md) in formato CIM-XML, che rappresentano gli errori rilevati nel processo. Se lo stato operativo del processo è 2 (OK), viene **restituito Null.**

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

L'accesso alla [**classe Msvm \_ ConcreteJob**](msvm-concretejob.md) potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8 solo \[ app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2012 \[\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ ConcreteJob**](msvm-concretejob.md)
</dt> </dl>

 

