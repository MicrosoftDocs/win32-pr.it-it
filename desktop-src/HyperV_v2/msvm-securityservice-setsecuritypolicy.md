---
description: 'Metodo SetSecurityPolicy della classe Msvm_SecurityService: imposta la protezione della chiave per un sistema virtuale.'
ms.assetid: 22496fde-6298-4e9d-bd0c-135dcb4ea5a5
title: Metodo SetSecurityPolicy della classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.SetSecurityPolicy
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c3ce4e95fe99eca0616d886ca16fefcb771be50f1a8cc0a46e6780e0411a6ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147095"
---
# <a name="setsecuritypolicy-method-of-the-msvm_securityservice-class"></a>Metodo SetSecurityPolicy della classe Msvm \_ SecurityService

Imposta la protezione della chiave per un sistema virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetSecurityPolicy(
  [in]  string              SecuritySettingData,
  [in]  uint8               SecurityPolicy[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SecuritySettingData* \[ Pollici\]
</dt> <dd>

La stringa contiene un'istanza incorporata [**della classe Msvm \_ SecuritySettingData**](msvm-securitysettingdata.md) che rappresenta le impostazioni di sicurezza di un sistema virtuale.

</dd> <dt>

*SecurityPolicy* \[ Pollici\]
</dt> <dd>

Matrice di byte non elaborata che contiene i criteri di sicurezza da impostare.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Parametro facoltativo per il monitoraggio dello stato dell'operazione, che viene utilizzato se non è stato possibile eseguire il metodo in modo sincrono. Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

On, success, restituisce un valore 0. In caso contrario, restituisce un errore.

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
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1703 \[\]<br/>                                               |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ SecurityService**](msvm-securityservice.md)
</dt> </dl>

 

 




