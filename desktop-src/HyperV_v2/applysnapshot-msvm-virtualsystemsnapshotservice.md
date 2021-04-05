---
description: Applica uno snapshot della macchina virtuale alla macchina virtuale dalla quale è stato creato.
ms.assetid: 45f1ec8f-aa96-4060-8f8c-0471d0ad4a21
title: Metodo ApplySnapshot della classe Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 735e827935689a0f0ede7fbac1d582ea40772ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881866"
---
# <a name="applysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a>Metodo ApplySnapshot della classe MSVM \_ VirtualSystemSnapshotService

Applica uno snapshot della macchina virtuale alla macchina virtuale dalla quale è stato creato.

## <a name="syntax"></a>Sintassi


```mof
uint32 ApplySnapshot(
  [in]  CIM_VirtualSystemSettingData REF Snapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Snapshot* \[ in\]
</dt> <dd>

Riferimento a una classe derivata da [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)) che rappresenta lo snapshot della macchina virtuale da applicare.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Questa operazione viene sempre eseguita in modo asincrono. Questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

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

**Accesso negato** (32769)
</dt> <dt>

**Parametro non valido** (32773)
</dt> <dt>

**Stato non valido** (32775)
</dt> <dt>

**Metodo riservato** (4097.. 32767)
</dt> <dt>

**Specifico del fornitore** (32768.. 65535)
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

[**\_VirtualSystemSnapshotService MSVM**](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[**ApplyVirtualSystemSnapshot (V1)**](/previous-versions/windows/desktop/virtual/applyvirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> <dt>

[**ApplyVirtualSystemSnapshotEx (V1)**](/previous-versions/windows/desktop/virtual/msvm-virtualsystemmanagementservice-applyvirtualsystemsnapshotex)
</dt> </dl>

 

