---
description: Recupera l'errore.
ms.assetid: a30cb74a-4e41-4981-b355-6f46b4b75ce6
title: Metodo GetError della classe Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b26995171059389f7f7afb3fb90e3506b39affd5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104058428"
---
# <a name="geterror-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a>Metodo GetError della \_ classe VirtualSystemReferencePointExportJob di MSVM

Recupera l'errore.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Errore* \[ out\]
</dt> <dd>

Errore recuperato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce 0. in caso contrario, contiene un errore.

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

[**\_VirtualSystemReferencePointExportJob MSVM**](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




