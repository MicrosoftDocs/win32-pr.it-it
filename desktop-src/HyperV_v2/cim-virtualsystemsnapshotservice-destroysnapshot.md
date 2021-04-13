---
description: Elimina uno snapshot del sistema virtuale esistente. Questo metodo può essere un effetto collaterale per eliminare altri snapshot che dipendono dallo snapshot interessato.
ms.assetid: 69f60d0e-50ef-4a38-ad4b-88534b7fb3f8
title: Metodo DestroySnapshot della classe CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80d618374d2da4a12f2ce31284d7b3fa36ba65ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526773"
---
# <a name="destroysnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a>Metodo DestroySnapshot della classe CIM \_ VirtualSystemSnapshotService

Elimina uno snapshot del sistema virtuale esistente. Questo metodo può essere un effetto collaterale per eliminare altri snapshot che dipendono dallo snapshot interessato.

## <a name="syntax"></a>Sintassi


```mof
uint32 DestroySnapshot(
  [in]  CIM_VirtualSystemSettingData REF AffectedSnapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AffectedSnapshot* \[ in\]
</dt> <dd>

Riferimento [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) allo snapshot del sistema virtuale interessato.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Se l'operazione è a esecuzione prolungata, è possibile che venga restituito facoltativamente un [**\_ ConcreteJob CIM**](cim-concretejob.md) che rappresenta il processo.

> [!Note]  
> Questo parametro è di lettura/scrittura in Windows 8.1.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Non riuscito** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Parametro non valido** (4)
</dt> <dt>

**Stato non valido** (5)
</dt> <dt>

**Tipo non valido** (6)
</dt> <dt>

**DMTF riservato** (..)
</dt> <dt>

**Parametri del metodo controllati-processo avviato** (4096)
</dt> <dt>

**Metodo riservato** (4097.. 32767)
</dt> <dt>

**Specifico del fornitore** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_VIRTUALSYSTEMSNAPSHOTSERVICE CIM**](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




