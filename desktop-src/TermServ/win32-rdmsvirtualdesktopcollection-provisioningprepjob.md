---
title: Metodo ProvisioningPrepJob della classe Win32_RDMSVirtualDesktopCollection
description: Crea un processo di provisioning di desktop virtuali.
ms.assetid: 240D4BE6-95BD-4858-8F8F-A00C92042AEF
ms.tgt_platform: multiple
keywords:
- Metodo ProvisioningPrepJob Servizi Desktop remoto
- Metodo ProvisioningPrepJob Servizi Desktop remoto , Win32_RDMSVirtualDesktopCollection interfaccia
- Win32_RDMSVirtualDesktopCollection'interfaccia Servizi Desktop remoto, metodo ProvisioningPrepJob
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningPrepJob
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2dab9dcbd606dd32857f0d2dc4b2de3d8516e2b2da10e804fa36254679c1d2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422841"
---
# <a name="provisioningprepjob-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Metodo ProvisioningPrepJob della classe \_ WIN32 RDMSVirtualDesktopCollection

Crea un processo di provisioning di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 ProvisioningPrepJob(
  [in]  string  CollectionAlias,
  [in]  string  VMHostName,
  [in]  string  VMName,
  [in]  string  ExportToLocation,
  [in]  boolean bSysPrep,
  [in]  string  MachineName,
  [in]  string  UserName,
  [in]  string  Password,
  [out] string  JobGuid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CollectionAlias* \[ Pollici\]
</dt> <dd>

Alias della raccolta che ospita il desktop virtuale.

</dd> <dt>

*VMHostName* \[ Pollici\]
</dt> <dd>

Nome host della macchina virtuale.

</dd> <dt>

*VMName* \[ Pollici\]
</dt> <dd>

Nome della macchina virtuale.

</dd> <dt>

*ExportToLocation* \[ Pollici\]
</dt> <dd>

Percorso completo in cui esportare il processo di provisioning.

</dd> <dt>

*bSysPrep* \[ Pollici\]
</dt> <dd>

Indica se il processo di provisioning rappresenta una distribuzione Sysprep.

</dd> <dt>

*MachineName* \[ Pollici\]
</dt> <dd>

Nome del computer che ospita la macchina virtuale.

</dd> <dt>

*UserName* \[ Pollici\]
</dt> <dd>

Nome utente dell'amministratore della macchina virtuale.

</dd> <dt>

*Password* \[ Pollici\]
</dt> <dd>

Password dell'amministratore della macchina virtuale.

</dd> <dt>

*Guida al processo* \[ Cambio\]
</dt> <dd>

**GUID che** identifica in modo univoco il processo di provisioning.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                              |
| Spazio dei nomi<br/>                | Radice \\ cimv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktopCollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





