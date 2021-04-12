---
description: Rimuove l'elemento gestito specificato come membro del \_ COLLECTIONOFMSES CIM con l'identificatore specificato. Questa operazione avrà esito positivo anche se l'oggetto con tale identificatore non è presente.
ms.assetid: 641535f0-ce71-4f57-a4e1-4775b3bb2374
title: Metodo RemoveMemberById della classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RemoveMemberById
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31c30d8698b16ac9bf128aa13ab80a64f09a40c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234203"
---
# <a name="removememberbyid-method-of-the-msvm_collectionmanagementservice-class"></a>Metodo RemoveMemberById della classe MSVM \_ CollectionManagementService

Rimuove l'elemento gestito specificato come membro del [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) con l'identificatore specificato. Questa operazione avrà esito positivo anche se l'oggetto con tale identificatore non è presente.

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoveMemberById(
  [in]  CIM_ManagedElement REF Member,
  [in]  string                 CollectionId,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Membro* \[ di in\]
</dt> <dd>

Membro da rimuovere.

</dd> <dt>

*CollectionId* \[ in\]
</dt> <dd>

ID della raccolta da cui rimuovere il membro.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Riferimento al processo (può essere null se l'attività è stata completata).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 se ha esito positivo oppure 4096 se il processo è stato avviato. in caso contrario, restituisce un errore.

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
</dt> <dt>

**File non trovato** (32779)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_CollectionManagementService MSVM**](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




