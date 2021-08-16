---
description: Verifica la connettività di rete di una macchina virtuale in Windows di virtualizzazione di rete.
ms.assetid: 37d4c34d-406e-4c52-afce-b0eef754eeb3
title: Metodo TestNetworkConnection della Msvm_VirtualSystemManagementService classe
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
ms.openlocfilehash: 66988944b6c4f4a97a450f63964d57084fc5886716d109e655921d8744bba721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388380"
---
# <a name="testnetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo TestNetworkConnection della classe Msvm \_ VirtualSystemManagementService

Verifica la connettività di rete di una macchina virtuale in Windows di virtualizzazione di rete.

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

*TargetNetworkAdapter* \[ Pollici\]
</dt> <dd>

Riferimento a un oggetto [**Msvm \_ EthernetPortAllocationSettingData che**](msvm-ethernetportallocationsettingdata.md) descrive la scheda di rete di destinazione.

</dd> <dt>

*IsSender* \[ Pollici\]
</dt> <dd>

Indica se questo metodo viene richiamato al mittente o al destinatario.

</dd> <dt>

*SenderIP* \[ Pollici\]
</dt> <dd>

Indirizzo IP del mittente.

</dd> <dt>

*ReceiverIP* \[ Pollici\]
</dt> <dd>

Indirizzo Mac del mittente.

</dd> <dt>

*ReceiverMac* \[ Pollici\]
</dt> <dd>

Indirizzo Mac del mittente.

</dd> <dt>

*IsolationId* \[ Pollici\]
</dt> <dd>

ID di isolamento.

</dd> <dt>

*SequenceNumber* \[ Pollici\]
</dt> <dd>

ID di isolamento.

</dd> <dt>

*RoundTripTime* \[ Cambio\]
</dt> <dd>

Ora round trip corrente.

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

**Non supportato** (1)
</dt> <dt>

**Operazione non** riuscita (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Parametro non valido** (4)
</dt> <dt>

**DmTF Reserved** (..)
</dt> <dt>

**Parametri del metodo verificati - Processo avviato** (4096)
</dt> <dt>

**Metodo riservato** (4097..32767)
</dt> <dt>

**Specifico del** fornitore (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

