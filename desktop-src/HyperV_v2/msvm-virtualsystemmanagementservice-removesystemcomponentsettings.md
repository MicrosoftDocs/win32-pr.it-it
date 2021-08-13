---
description: Rimuove le impostazioni dei componenti generici da una configurazione del sistema virtuale.
ms.assetid: 54ddb960-65b7-409d-ad80-f3685562a1a1
title: Metodo RemoveSystemComponentSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveSystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bf8a4c25c01af62b22108d239e344dec9d3087021c3ec4962e7a30d578c7082e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644677"
---
# <a name="removesystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo RemoveSystemComponentSettings della classe Msvm \_ VirtualSystemManagementService

Rimuove le impostazioni dei componenti generici da una configurazione del sistema virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoveSystemComponentSettings(
  [in]  Msvm_SystemComponentSettingData REF ComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ComponentSettings* \[ Pollici\]
</dt> <dd>

Matrice di [**Msvm \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) che fanno riferimento alle impostazioni del componente da rimuovere.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 o 4096 in un esito positivo. In caso contrario, restituisce un errore.

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

**Stato non valido** (5)
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
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1703 \[\]<br/>                                               |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

