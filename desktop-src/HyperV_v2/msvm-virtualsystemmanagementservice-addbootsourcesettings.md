---
description: Aggiunge origini di avvio a una configurazione del sistema virtuale quando viene applicata a un &\# 0034;stato&\# 0034; configurazione del sistema virtuale.
ms.assetid: 2d091554-73d4-47c6-a0c2-97644fc9abe9
title: Metodo AddBootSourceSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddBootSourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d52333f3118caa1cf437fabb536bb62f84b99dab01b3115e7f6a65c3f182a17e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148074"
---
# <a name="addbootsourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo AddBootSourceSettings della classe Msvm \_ VirtualSystemManagementService

Aggiunge origini di avvio a una configurazione del sistema virtuale quando viene applicata a una configurazione del sistema virtuale "stato".

## <a name="syntax"></a>Sintassi


```mof
uint32 AddBootSourceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           BootSourceSettings[],
  [out] CIM_SettingData              REF ResultingBootSourceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AffectedConfiguration* \[ Pollici\]
</dt> <dd>

Oggetto [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) contenente la configurazione interessata.

</dd> <dt>

*BootSourceSettings* \[ Pollici\]
</dt> <dd>

Matrice contenente le impostazioni dell'origine di avvio.

</dd> <dt>

*ResultingBootSourceSettings* \[ Cambio\]
</dt> <dd>

In caso di esito positivo, restituisce [**un oggetto CIM \_ SettingData**](cim-settingdata.md) con le impostazioni dell'origine di avvio risultanti.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce 0 o 4096. In caso contrario, restituisce un errore.

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

**DMTF riservato** (..)
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

 

