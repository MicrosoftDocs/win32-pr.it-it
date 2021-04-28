---
description: 'Metodo SetKeyProtector della classe Msvm_SecurityService: imposta la protezione della chiave per un sistema virtuale.'
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
ms.openlocfilehash: 3b5eca7ddcc506d158175782e3e13796e56de267
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111409"
---
# <a name="setkeyprotector-method-of-the-msvm_securityservice-class"></a>Metodo SetKeyProtector della classe Msvm \_ SecurityService

Imposta la protezione della chiave per un sistema virtuale.

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

*SecuritySettingData* \[ Pollici\]
</dt> <dd>

La stringa contiene un'istanza incorporata [**della classe Msvm \_ SecuritySettingData**](msvm-securitysettingdata.md) che rappresenta le impostazioni di sicurezza di un sistema virtuale.

</dd> <dt>

*KeyProtector* \[ Pollici\]
</dt> <dd>

Matrice di byte non elaborata che contiene la protezione della chiave da impostare.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Parametro facoltativo per il monitoraggio dello stato dell'operazione, che viene utilizzato se non è stato possibile eseguire il metodo in modo sincrono. Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce un valore 0 o 4096. In caso contrario, restituisce un errore.

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

 

 




