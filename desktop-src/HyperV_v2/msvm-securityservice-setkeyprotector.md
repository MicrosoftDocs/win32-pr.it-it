---
description: Imposta la protezione con chiave per un sistema virtuale.
ms.assetid: 84c114cb-a3a0-44f2-b862-38b05b96bd46
title: Metodo SetKeyProtector della classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.SetKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 404baf0a529a6e96869fbcd355a81308f5d1e966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308211"
---
# <a name="setkeyprotector-method-of-the-msvm_securityservice-class"></a>Metodo SetKeyProtector della classe MSVM \_ SecurityService

Imposta la protezione con chiave per un sistema virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetKeyProtector(
  [in]  string              SecuritySettingData,
  [in]  uint8               KeyProtector[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SecuritySettingData* \[ in\]
</dt> <dd>

La stringa contiene un'istanza incorporata della classe [**\_ SecuritySettingData MSVM**](msvm-securitysettingdata.md) che rappresenta le impostazioni di sicurezza di un sistema virtuale.

</dd> <dt>

*Protector* \[ in\]
</dt> <dd>

Matrice di byte non elaborata contenente la protezione con chiave da impostare.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Parametro facoltativo per il monitoraggio dello stato di avanzamento dell'operazione, che viene utilizzato se non è stato possibile eseguire in modo sincrono il metodo. Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.

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

[**\_SecurityService MSVM**](msvm-securityservice.md)
</dt> </dl>

 

 




