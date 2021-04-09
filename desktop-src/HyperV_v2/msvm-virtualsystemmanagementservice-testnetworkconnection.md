---
description: Verifica la connettività di rete di una macchina virtuale in un ambiente di virtualizzazione rete Windows.
ms.assetid: 37d4c34d-406e-4c52-afce-b0eef754eeb3
title: Metodo TestNetworkConnection della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.TestNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e8f15faacb1b8ad683b1ea9abfa9b91f5c376dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128399"
---
# <a name="testnetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo TestNetworkConnection della classe MSVM \_ VirtualSystemManagementService

Verifica la connettività di rete di una macchina virtuale in un ambiente di virtualizzazione rete Windows.

## <a name="syntax"></a>Sintassi


```mof
uint32 TestNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  boolean                                    IsSender,
  [in]  string                                     SenderIP,
  [in]  string                                     ReceiverIP,
  [in]  string                                     ReceiverMac,
  [in]  uint32                                     IsolationId,
  [in]  uint32                                     SequenceNumber,
  [out] uint32                                     RoundTripTime,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TargetNetworkAdapter* \[ in\]
</dt> <dd>

Riferimento a un [**\_ EthernetPortAllocationSettingData MSVM**](msvm-ethernetportallocationsettingdata.md) che descrive la scheda di rete di destinazione.

</dd> <dt>

Il *mittenti* \[ in\]
</dt> <dd>

Indica se questo metodo viene richiamato al mittente o al ricevitore.

</dd> <dt>

*SenderIP* \[ in\]
</dt> <dd>

Indirizzo IP del mittente.

</dd> <dt>

*ReceiverIP* \[ in\]
</dt> <dd>

Indirizzo MAC del mittente.

</dd> <dt>

*ReceiverMac* \[ in\]
</dt> <dd>

Indirizzo MAC del mittente.

</dd> <dt>

*IsolationId* \[ in\]
</dt> <dd>

ID isolamento.

</dd> <dt>

*SequenceNumber* \[ in\]
</dt> <dd>

ID isolamento.

</dd> <dt>

*RoundtripTime* \[ out\]
</dt> <dd>

Round trip tempo.

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
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

