---
description: Aggiorna le impostazioni per un disco rigido virtuale.
ms.assetid: 10f80313-bc78-447e-bdf2-5635d7354e3c
title: Metodo SetVirtualHardDiskSettingData della Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVirtualHardDiskSettingData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3fb107edc5227cd5a3ff1f96f0e68c038fb00817cfb945dd08fcaea5d2254229
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050471"
---
# <a name="setvirtualharddisksettingdata-method-of-the-msvm_imagemanagementservice-class"></a>Metodo SetVirtualHardDiskSettingData della classe Msvm \_ ImageManagementService

Aggiorna le impostazioni per un disco rigido virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetVirtualHardDiskSettingData(
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VirtualDiskSettingData* \[ Pollici\]
</dt> <dd>

Rappresentazione di stringa della [**classe Msvm \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) che specifica il disco rigido virtuale da aggiornare e che contiene i nuovi dati delle impostazioni. Solo le **proprietà ParentPath,** **PhysicalSectorSize** o **VirtualDiskId** possono essere aggiornate con questo metodo. Non è possibile aggiornare queste proprietà con una sola chiamata al metodo. È possibile aggiornare una sola di queste proprietà con una singola chiamata al metodo.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Parametri del metodo controllati - Processo avviato** (4096)
</dt> <dt>

**Operazione non** riuscita (32768)
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

**Sistema in uso** (32774)
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

## <a name="remarks"></a>Commenti

L'accesso alla [**classe Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md) potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

