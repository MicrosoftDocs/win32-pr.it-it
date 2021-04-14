---
description: Recupera la protezione con chiave per un sistema virtuale.
ms.assetid: fd827da8-b2fc-4c57-bb7d-7da46db8e8be
title: Metodo GetKeyProtector della classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.GetKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 49f2479660d0402c7b3d428c76f9fe454ecf64cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350651"
---
# <a name="getkeyprotector-method-of-the-msvm_securityservice-class"></a>Metodo GetKeyProtector della classe MSVM \_ SecurityService

Recupera la protezione con chiave per un sistema virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetKeyProtector(
  [in]  string SecuritySettingData,
  [out] uint8  KeyProtector[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SecuritySettingData* \[ in\]
</dt> <dd>

La stringa contiene un'istanza incorporata della classe [**\_ SecuritySettingData MSVM**](msvm-securitysettingdata.md) che rappresenta le impostazioni di sicurezza di un sistema virtuale.

</dd> <dt>

*Protector* \[ out\]
</dt> <dd>

Riceve la matrice di byte non elaborati che contiene la protezione con chiave attualmente in uso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione riesce, restituisce 0 o 4096. In caso contrario, restituisce un errore.

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

 

 




