---
description: Elimina una voce snapshot del disco rigido virtuale all'interno di un file di set di dischi rigidi virtuali.
ms.assetid: 37d55a5f-209d-42ce-8f69-8b494055e263
title: Metodo DeleteVHDSnapshot della Msvm_ImageManagementService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.DeleteVHDSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 45a15b03b3ca26375ef0a563981cb9405c4397f355735c173e105029959d8282
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119522661"
---
# <a name="deletevhdsnapshot-method-of-the-msvm_imagemanagementservice-class"></a>Metodo DeleteVHDSnapshot della classe Msvm \_ ImageManagementService

Elimina una voce snapshot del disco rigido virtuale all'interno di un file di set di dischi rigidi virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 DeleteVHDSnapshot(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotId,
  [in]  boolean             PersistReferenceSnapshot,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VHDSetPath* \[ Pollici\]
</dt> <dd>

Stringa contenente il percorso del file del set di dischi rigidi virtuali contenente lo snapshot in questione.

</dd> <dt>

*SnapshotId* \[ Pollici\]
</dt> <dd>

GUID che rappresenta l'ID snapshot per la voce dello snapshot del disco rigido virtuale da eliminare.

</dd> <dt>

*PersistReferenceSnapshot* \[ Pollici\]
</dt> <dd>

Indica se un record di snapshot di solo riferimento deve essere reso persistente dopo l'eliminazione dello snapshot.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Riferimento al processo (può essere Null se l'attività viene completata).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti:

<dl> <dt>

**Completata senza errori** (0)
</dt> <dt>

**Parametri del metodo verificati - Processo avviato** (4096)
</dt> <dt>

**Non riuscito** (32768)
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

**Il sistema è in uso** (32774)
</dt> <dt>

**Stato non valido per questa operazione** (32775)
</dt> <dt>

**Tipo di dati non** corretto (32776)
</dt> <dt>

**Il sistema non è disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> <dt>

**File non trovato** (32779)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




