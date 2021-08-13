---
description: Cancella lo stato di salvataggio da uno snapshot esistente.
ms.assetid: abb0ed4a-7f89-4d32-93d2-7491d2f2aa83
title: Metodo ClearSnapshotState della Msvm_VirtualSystemSnapshotService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ClearSnapshotState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a861cf1141532c7a780f4b886fd71a0868faf432c02db57bde505fbaa72f4ac0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118645863"
---
# <a name="clearsnapshotstate-method-of-the-msvm_virtualsystemsnapshotservice-class"></a>Metodo ClearSnapshotState della classe Msvm \_ VirtualSystemSnapshotService

Cancella lo stato di salvataggio da uno snapshot esistente.

## <a name="syntax"></a>Sintassi


```mof
uint32 ClearSnapshotState(
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SnapshotSettingData* \[ Pollici\]
</dt> <dd>

Riferimento [**all'istanza CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) che rappresenta lo snapshot il cui stato deve essere cancellato.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

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
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

