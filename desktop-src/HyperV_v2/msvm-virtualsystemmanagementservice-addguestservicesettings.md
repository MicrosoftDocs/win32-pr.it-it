---
description: Aggiunge le impostazioni del servizio guest a una configurazione del sistema virtuale.
ms.assetid: 2c8c2f2b-332a-470e-af7f-80c82e3e2caf
title: Metodo AddGuestServiceSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4f011a0bce545bbde57cbcc9c22861f492cbc27e71ddc717a379d82cbd27bc42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681141"
---
# <a name="addguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo AddGuestServiceSettings della classe Msvm \_ VirtualSystemManagementService

Aggiunge le impostazioni del servizio guest a una configurazione del sistema virtuale.

Se applicato a parti di una configurazione del sistema virtuale "corrente", come effetto collaterale i servizi guest del sistema virtuale attivo possono essere modificati.

## <a name="syntax"></a>Sintassi


```mof
uint32 AddGuestServiceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           GuestServiceSettings[],
  [out] CIM_SettingData              REF ResultingGuestServiceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AffectedConfiguration* \[ Pollici\]
</dt> <dd>

Riferimento a un [**oggetto CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) che descrive la configurazione interessata.

</dd> <dt>

*GuestServiceSettings* \[ Pollici\]
</dt> <dd>

Matrice contenente le impostazioni del servizio guest.

</dd> <dt>

*ResultingGuestServiceSettings* \[ Cambio\]
</dt> <dd>

In caso di esito positivo, contiene un riferimento a [**un oggetto CIM \_ SettingData**](cim-settingdata.md) che descrive le impostazioni del servizio guest risultanti.

</dd> <dt>

*Processo* \[ Cambio\]
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
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

