---
description: Diagnostica la connettività di rete di una macchina virtuale in un ambiente di virtualizzazione rete Windows.
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
ms.openlocfilehash: 70760f771e3908265a4ac70ebc1cbdf957d652c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306009"
---
# <a name="diagnosenetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo DiagnoseNetworkConnection della classe MSVM \_ VirtualSystemManagementService

Diagnostica la connettività di rete di una macchina virtuale in un ambiente di virtualizzazione rete Windows.

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

*TargetNetworkAdapter* \[ in\]
</dt> <dd>

Riferimento a un [**\_ EthernetPortAllocationSettingData MSVM**](msvm-ethernetportallocationsettingdata.md) che descrive la scheda di rete di destinazione.

</dd> <dt>

*DiagnosticSettings* \[ in\]
</dt> <dd>

Impostazioni di diagnostica da utilizzare.

</dd> <dt>

*DiagnosticInformation* \[ out\]
</dt> <dd>

Se l'operazione riesce, restituisce le informazioni di diagnostica.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 o 4096 in caso di esito positivo. in caso contrario, restituisce un errore.

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
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1703 \[\]<br/>                                               |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

