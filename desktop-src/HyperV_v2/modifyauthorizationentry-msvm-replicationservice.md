---
description: Modifica una voce di autorizzazione per un server di ripristino.
ms.assetid: fbdf3ecd-42de-49a8-85b8-51fc9c9fcf26
title: Metodo ModifyAuthorizationEntry della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 17f5ff1a0e4e1cca95dc5f7764d2f8e2bf9d2c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315499"
---
# <a name="modifyauthorizationentry-method-of-the-msvm_replicationservice-class"></a>Metodo ModifyAuthorizationEntry della classe MSVM \_ ReplicationService

Modifica una voce di autorizzazione per un server di ripristino.

## <a name="syntax"></a>Sintassi


```mof
uint32 ModifyAuthorizationEntry(
  [in]  string              AuthorizationEntry,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AuthorizationEntry* \[ in\]
</dt> <dd>

Rappresentazione di stringa di un'istanza della classe [**MSVM \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) che definisce la voce di autorizzazione da modificare.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

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

**Sistema in uso** (32774)
</dt> <dt>

**Stato non valido per l'operazione** (32775)
</dt> <dt>

**Tipo di dati non corretto** (32776)
</dt> <dt>

**Sistema non disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> <dt>

**File non trovato** (32779)
</dt> </dl>

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

[**AddAuthorizationEntry**](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[**RemoveAuthorizationEntry**](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[**SetAuthorizationEntry**](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[**\_ReplicationService MSVM**](msvm-replicationservice.md)
</dt> </dl>

 

