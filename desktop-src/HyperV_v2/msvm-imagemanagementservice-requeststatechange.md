---
description: 'Metodo RequestStateChange della classe Msvm_ImageManagementService: richiede una modifica dello stato.'
ms.assetid: 005b34c7-51ed-4ef3-934c-a6a57a878b3b
title: Metodo RequestStateChange della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: cf059fa5f45db97f5f63abb12e68a443b8988c02
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111769"
---
# <a name="requeststatechange-method-of-the-msvm_imagemanagementservice-class"></a>Metodo RequestStateChange della classe Msvm \_ ImageManagementService

Richiede una modifica dello stato.

## <a name="syntax"></a>Sintassi


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RequestedState* \[ Pollici\]
</dt> <dd>

Nuovo stato. Le informazioni vengono inserite nella **proprietà RequestedState** dell'istanza se il codice restituito del **metodo RequestStateChange** è 0 o 4096. Per altre informazioni, vedere la descrizione delle **proprietà EnabledState** e **RequestedState** per l'elemento. Deve essere uno dei valori seguenti.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Abilitato** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Disabilitato** (3)


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

**Arresto** (4)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**Offline** (6)


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

**Test** (7)


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

**Rinvio** (8)


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

**Inattiva** (9)


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

**Riavvio** (10)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Reimpostazione** (11)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornitore riservato** (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Può contenere un riferimento a [**CIM \_ ConcreteJob**](cim-concretejob.md) creato per tenere traccia della transizione di stato avviata dalla chiamata al metodo.

</dd> <dt>

*TimeoutPeriod* \[ Pollici\]
</dt> <dd>

Periodo di timeout che specifica la quantità massima di tempo prevista dal client per la transizione al nuovo stato. Il formato dell'intervallo deve essere usato per specificare il periodo di timeout. Il valore 0 o **Null** indica che il client non ha requisiti di tempo per la transizione. Se questa proprietà non contiene 0 o **Null** e l'implementazione non supporta questo parametro, deve essere restituito un codice restituito 4098 (Utilizzo del parametro di **timeout** non supportato).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti:

<dl> <dt>

**Completata senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




