---
description: Modifica i dati delle impostazioni di merge del disco.
ms.assetid: 91775dc5-105a-4e38-a334-fb34dd4e59f8
title: Metodo ModifyDiskMergeSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyDiskMergeSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fe737c084b4c1c76a411ce1d2eba513554b40f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313862"
---
# <a name="modifydiskmergesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo ModifyDiskMergeSettings della classe MSVM \_ VirtualSystemManagementService

Modifica i dati delle impostazioni di merge del disco.

## <a name="syntax"></a>Sintassi


```mof
uint32 ModifyDiskMergeSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SettingData* \[ in\]
</dt> <dd>

Istanza incorporata della classe [**\_ DiskMergeSettingData MSVM**](msvm-diskmergesettingdata.md) che contiene i dati di impostazione modificati per la funzione di merge del disco.

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

[**\_VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

