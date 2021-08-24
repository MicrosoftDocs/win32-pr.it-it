---
description: Aggiunge subnet di rete di migrazione per il servizio di migrazione del sistema virtuale.
ms.assetid: b0e0f187-beeb-4fdf-a91c-f6c5500f0f6d
title: Metodo AddNetworkSettings della classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.AddNetworkSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0a46faa340bfe53e7db2afd0dd909d1adb9fcfd9621742451604ae0e25e71936
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765711"
---
# <a name="addnetworksettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Metodo AddNetworkSettings della classe Msvm \_ VirtualSystemMigrationService

Aggiunge subnet di rete di migrazione per il servizio di migrazione del sistema virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 AddNetworkSettings(
  [in]  string              NetworkSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NetworkSettings* \[ Pollici\]
</dt> <dd>

Matrice di istanze incorporate della [**classe Msvm \_ VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) che contengono le impostazioni di rete di migrazione.

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
</dt> </dl>

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

[**ModifyNetworkSettings**](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[**RemoveNetworkSettings**](removenetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

