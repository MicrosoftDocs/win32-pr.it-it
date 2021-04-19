---
description: Richiede che lo stato del componente dell'interfaccia del servizio Guest venga modificato nel valore specificato.
ms.assetid: D9F7CD03-0D86-4005-A600-5CC7082A5047
title: 'Metodo Msvm_GuestServiceInterfaceComponent:: RequestStateChange'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: de5689968d44277b01d6cb2256d41ddbbe573cd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311779"
---
# <a name="msvm_guestserviceinterfacecomponentrequeststatechange-method"></a>\_Metodo MSVM GuestServiceInterfaceComponent:: RequestStateChange

Richiede che lo stato del componente dell'interfaccia del servizio Guest venga modificato nel valore specificato.

## <a name="syntax"></a>Sintassi


```C++
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RequestedState* \[ in\]
</dt> <dd>

Tipo: **UInt16**

Nuovo stato. Le informazioni vengono inserite nella proprietà **RequestedState** dell'istanza se il codice restituito del metodo **RequestStateChange** è 0 o 4096. Per ulteriori informazioni, vedere la descrizione delle proprietà **EnabledState** e **RequestedState** per l'elemento. Deve essere uno dei valori seguenti.

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

**Rinvia** (8)


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

**Mettere in stato** (9)


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

**Riavvio** (10)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Reimposta** (11)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornitore riservato** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**

Riferimento facoltativo a un oggetto [**MSVM \_ ConcreteJob**](msvm-concretejob.md) restituito se l'operazione viene eseguita in modo asincrono. Se presente, il riferimento restituito può essere usato per monitorare lo stato di avanzamento e ottenere il risultato del metodo.

</dd> <dt>

*TimeoutPeriod* \[ in\]
</dt> <dd>

Tipo: **DateTime**

Periodo di timeout che specifica la quantità massima di tempo per cui il client prevede che la transizione al nuovo stato venga eseguita. Per specificare il periodo di timeout, è necessario utilizzare il formato intervallo. Il valore 0 o **null** indica che il client non dispone di requisiti temporali per la transizione. Se questa proprietà non contiene 0 o **null** e l'implementazione non supporta questo parametro, deve essere restituito un codice restituito 4098 (**utilizzo del parametro timeout non supportato**).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei valori seguenti.



| Codice/valore restituito                                                                                                                                                                       | Descrizione         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**Completato senza errori**</dt> <dt>0</dt> </dl>                           | Esito positivo.<br/> |
| <dl> <dt>**Non supportato**</dt> <dt>1</dt> </dl>                                     |                     |
| <dl> <dt>**Errore sconosciuto/non specificato**</dt> <dt>2</dt> </dl>                         |                     |
| <dl> <dt>**Non può essere completato entro il periodo di timeout**</dt> <dt>3</dt> </dl>            |                     |
| <dl> <dt>**Errore**</dt> <dt>4</dt> </dl>                                            |                     |
| <dl> <dt>**Parametro 5 non valido**</dt> <dt></dt> </dl>                                 |                     |
| <dl> <dt>**In uso**</dt> <dt>6</dt> </dl>                                            |                     |
| <dl> <dt>**DMTF riservato**</dt> <dt>..</dt> </dl>                                    |                     |
| <dl> <dt>**Parametri del metodo controllati-transizione avviata**</dt> <dt>4096</dt> </dl> |                     |
| <dl> <dt>**Transizione di stato non valida**</dt> <dt>4097</dt> </dl>                       |                     |
| <dl> <dt>**Uso del parametro timeout non supportato**</dt> <dt>4098</dt> </dl>         |                     |
| <dl> <dt>**Occupato**</dt> <dt>4099</dt> </dl>                                           |                     |
| <dl> <dt>**Metodo riservato**</dt> <dt>4100.. 32767</dt> </dl>                         |                     |
| <dl> 32768 <dt>**specifici del fornitore**</dt> <dt>.. 65535</dt> </dl>                        |                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\\\\\Virtualizzazione radice \\ v2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GuestServiceInterfaceComponent MSVM**](msvm-guestserviceinterfacecomponent.md)
</dt> </dl>

 

