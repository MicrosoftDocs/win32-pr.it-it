---
description: Recupera gli oggetti Error per il processo, se presenti.
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
ms.openlocfilehash: e938d41afad430051bebb08fc77d6edf6da44691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307743"
---
# <a name="geterrorex-method-of-the-msvm_concretejob-class"></a>Metodo GetErrorEx della classe MSVM \_ ConcreteJob

Recupera gli oggetti Error per il processo, se presenti. Quando il processo è in esecuzione o è terminato senza errori, questo metodo non restituisce alcuna istanza di [**\_ errore MSVM**](msvm-error.md) . Tuttavia, se il processo non è riuscito a causa di un problema interno o perché il processo è stato terminato da un client, vengono restituite una o più istanze di **\_ errore MSVM** .

## <a name="syntax"></a>Sintassi


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Errori* \[ di out\]
</dt> <dd>

Tipo: **stringa \[ \]**

Se lo stato operativo del processo non è 2 (OK), questo metodo restituisce una o più istanze incorporate della classe [**di \_ errore MSVM**](msvm-error.md) , in formato CIM-XML, che rappresentano gli errori rilevati nel processo. Se lo stato operativo del processo è 2 (OK), viene restituito **null** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
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

**Sistema in uso** (32774)
</dt> <dt>

**Stato non valido per l'operazione** (32775)
</dt> <dt>

**Tipo di dati non corretto** (32776)
</dt> <dt>

**Sistema non disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla [**classe \_ ConcreteJob di MSVM**](msvm-concretejob.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ConcreteJob MSVM**](msvm-concretejob.md)
</dt> </dl>

 

