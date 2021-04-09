---
description: Importa i metadati del punto di riferimento del sistema virtuale.
ms.assetid: 8e32fded-cd84-4586-83c4-c23200d4698e
title: Metodo ImportReferencePointMetadata della classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ImportReferencePointMetadata
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c66a374247d324f5df192114d0b66adc3a17c5b0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968954"
---
# <a name="importreferencepointmetadata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Metodo ImportReferencePointMetadata della classe MSVM \_ VirtualSystemReferencePointService

Importa i metadati del punto di riferimento del sistema virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 ImportReferencePointMetadata(
  [in]  Msvm_ComputerSystem REF AffectedSystem,
  [in]  string                  ConfigFilePath,
  [in]  string                  RuntimeStateFilePath,
  [out] CIM_ConcreteJob     REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AffectedSystem* \[ in\]
</dt> <dd>

Riferimento a un [**\_ ComputerSystem MSVM**](msvm-computersystem.md) che descrive il sistema interessato.

</dd> <dt>

*ConfigFilePath* \[ in\]
</dt> <dd>

Percorso completo del file di configurazione da cui verranno importati i metadati del punto di riferimento.

</dd> <dt>

*RuntimeStateFilePath* \[ in\]
</dt> <dd>

Percorso completo del file di stato di runtime da cui verranno importati i metadati del punto di riferimento.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Parametro facoltativo per il monitoraggio dello stato di avanzamento dell'operazione, che viene utilizzato se non è stato possibile eseguire in modo sincrono il metodo. Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 (nessun errore) o uno dei messaggi di errore seguenti:

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
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1703 \[\]<br/>                                               |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_VirtualSystemReferencePointService MSVM**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




