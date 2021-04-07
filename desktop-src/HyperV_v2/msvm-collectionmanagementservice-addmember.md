---
description: Aggiunge l'elemento gestito specificato come membro dell'oggetto CollectionOfMSEs CIM specificato \_ .
ms.assetid: 6f23eecc-b445-4495-ae96-76b89652a1cb
title: Metodo AddMember della classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.AddMember
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6b885701086262fda48c5d50abd750eca6866c72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760499"
---
# <a name="addmember-method-of-the-msvm_collectionmanagementservice-class"></a>Metodo AddMember della classe MSVM \_ CollectionManagementService

Aggiunge l'elemento gestito specificato come membro dell'oggetto [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 AddMember(
  [in]  CIM_ManagedElement   REF Member,
  [in]  CIM_CollectionOfMSEs REF Collection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Membro* \[ di in\]
</dt> <dd>

Membro da aggiungere alla raccolta.

</dd> <dt>

*Raccolta* \[ di in\]
</dt> <dd>

Raccolta a cui aggiungere il membro.

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

 

 




