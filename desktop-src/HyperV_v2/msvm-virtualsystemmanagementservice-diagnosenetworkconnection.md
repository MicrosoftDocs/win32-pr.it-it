---
description: Diagnostica la connettività di rete di una macchina virtuale in un Windows di virtualizzazione di rete.
ms.assetid: c18f48bf-1f57-4a23-a495-462afad42750
title: Metodo DiagnoseNetworkConnection della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DiagnoseNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9c82f72a9c2a2b16ad991940fcb378c41e75fdf31e9e6f8b74f23f9d115cab93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681130"
---
# <a name="diagnosenetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo DiagnoseNetworkConnection della classe Msvm \_ VirtualSystemManagementService

Diagnostica la connettività di rete di una macchina virtuale in un Windows di virtualizzazione di rete.

## <a name="syntax"></a>Sintassi


```mof
uint32 DiagnoseNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  string                                     DiagnosticSettings,
  [out] string                                     DiagnosticInformation,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TargetNetworkAdapter* \[ Pollici\]
</dt> <dd>

Riferimento a [**un oggetto Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) che descrive la scheda di rete di destinazione.

</dd> <dt>

*DiagnosticSettings* \[ Pollici\]
</dt> <dd>

Impostazioni di diagnostica da usare.

</dd> <dt>

*DiagnosticInformation* \[ Cambio\]
</dt> <dd>

In caso di esito positivo, restituisce le informazioni di diagnostica.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore 0 o 4096 in esito positivo. In caso contrario, restituisce un errore.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Operazione non** riuscita (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Parametro non** valido (4)
</dt> <dt>

**DmTF riservato** (..)
</dt> <dt>

**Parametri del metodo controllati - Processo avviato** (4096)
</dt> <dt>

**Metodo riservato** (4097..32767)
</dt> <dt>

**Specifico del** fornitore (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1703 \[\]<br/>                                               |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

