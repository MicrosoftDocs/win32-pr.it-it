---
description: Smonta il dispositivo PCI specificato in modo che possa essere assegnato.
ms.assetid: 8ea3bc27-93ba-4db8-a4aa-cdfea225eaa9
title: Metodo DismountAssignableDevice della classe Msvm_AssignableDeviceService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.DismountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 53036cd09113430d1045c8e9eae7a8d782b35960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314342"
---
# <a name="dismountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a>Metodo DismountAssignableDevice della classe MSVM \_ AssignableDeviceService

Smonta il dispositivo PCI specificato in modo che possa essere assegnato.

## <a name="syntax"></a>Sintassi


```mof
uint32 DismountAssignableDevice(
  [in]  string              DismountSettingData,
  [out] string              DismountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DismountSettingData* \[ in\]
</dt> <dd>

Istanza incorporata di un oggetto dati di impostazione che specifica il dispositivo PCI da smontare.

</dd> <dt>

*DismountedDeviceInstancePath* \[ out\]
</dt> <dd>

Stringa contenente il percorso dell'istanza del dispositivo per il dispositivo smontato.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Riferimento al processo (può essere null se l'attività è stata completata).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce 0 o 4096; in caso contrario, restituisce un errore.

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
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1703 \[\]<br/>                                               |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_AssignableDeviceService MSVM**](msvm-assignabledeviceservice.md)
</dt> </dl>

 

 




